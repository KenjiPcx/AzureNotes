# Describe cloud concepts (25–30%)

## Describe cloud computing

- Cloud computing is the delivery of computing services such as compute, storage, networking, software and analytics over the internet

### Define cloud computing

### Describe the shared responsibility model

- Cloud provider is responsible for the underlying physical hardware
- Customer always retains responsibility for the data, end user devices, accounts and access management

### Define cloud models, including public, private, and hybrid

#### Public

- Deploy without managing the underlying hardware

#### Private

- Need IT

#### Hybrid

- On premise
- Need some CapEx for on-premise
- Hybrid benefit
  - Use preexisting license to save cost

#### Identify appropriate use cases for each cloud model

### Describe the consumption-based model

## Compare cloud pricing models

### Azure reservations

- Fixed
- Commit to multi year plan
- Reduction in pay as you go prices

## Describe the benefits of using cloud services

### Describe the benefits of high availability and scalability in the cloud

- Scalability
  - Manually increasing or decreasing resources
- Elasticity
  - Automatically increasing or decreasing resources
- Agility
  - Speed and flexibility in allocation and deallocation of resources
- High availability
  - Keeps resources and services functioning for a long period of time

### Describe the benefits of reliability and predictability in the cloud

### Describe the benefits of security and governance in the cloud

### Describe the benefits of manageability in the cloud

## Describe cloud service types

### Describe infrastructure as a service (IaaS)

- Subscribers are responsible for
  - Applications
  - Data
  - Runtime
  - Middleware
  - OS
- Service provider responsible for
  - Virtualization
  - Servers
  - Storage
  - Physical networking
- Network, compute and storage is provided
- Resources can be allocated on a pay as you go basis
- Transition an on premis to cloud with minimum impact

### Describe platform as a service (PaaS)

- Azure provides and manages container orchestrators
- Customers responsible for
  - Applications
  - Data

### Describe software as a service (SaaS)

- Make productivity applications available to all employees
- Pay as you go basis

### Identify appropriate use cases for each cloud service (IaaS, PaaS, SaaS)

#### Azure Virtual Machine

- Migrate a workload from an on premise Hyper V host to azure while retaining full control over the OS

#### Azure Dedicated Hosts

- A provided physical server is dedicated to your organization's workload only
- Single tenant, cannot share provided physical servers across multiple Azure subscriptions
- Charged per dedicated host

#### Azure App Service

- Deploy a web app using a PaaS for scalability and security
- Enables you to perform automated deployments from Azure DevOps

#### Azure Functions

- Event driven solution

# Describe Azure architecture and services (35–40%)

## Describe the core architectural components of Azure

### Describe Azure regional, regional pairs, and sovereign regions

### Describe availability zones

### Describe Azure datacenters

### Describe Azure resources and resource groups

- Serves as a container for Azure resources like VMs and web apps
- Locking parent locks all children
- Can contain resources from different regions
- Can add or remove as long as not locked
- Can interact with other resources in a different resource group
- Quotas for resource groups are per region

### Describe subscriptions

- A single Azure account can have multiple subscriptions
- One for each bill
- User can be given access to multiple subscriptions
- Can have multiple licenses
- An organization can own multiple subscriptions
- Can contain more than one resource groups

#### Free

- 6 months
- Includes 200 credit for 30 days

#### Students

- For students only

#### Pay as you go

- 18 months

#### Enterprise

- Licenses

### Describe management groups

### Describe the hierarchy of resource groups, subscriptions, and management groups

#### AD tenant

- An organization't top level hierarchy
- Organization will have one tenant and multiple subscriptions

#### Management group

- Organize multiple subscriptions as a single management entity

#### Resource groups

- Group together resources

## Separate availability zones

- High available access
- Separate fault and update zones
- Minimal latency

## Separate availability sets

- Deploy to same datacenter

## Separate resource group

- Define logical resource group for management purposes

## Separate region in regional pair

- Separate fault and update
- Does not minimize latency

## Describe Azure compute and networking services

### Compare compute types, including container instances, virtual machines (VMs), and functions

### Describe VM options, including Azure Virtual Machines, Azure Virtual Machine Scale Sets, availability sets, and Azure Virtual Desktop

#### Spot

- Provides access to discounted compute resources
- Doesn't use standard SLA
- Can set maximum price to pay

#### Scale sets

- Group of identical, autoscaling VMs in the cloud
- Provision VMs automatically

#### Azure virtual desktop

- Supports MacOS and iOS
- Not charged on a monthly basis by active users
- Can use with existing 365 license, charged for the virtual machines where AVD runs
- Exist in the same AD linked to Azure AD

### Describe resources required for virtual machines

### Describe application hosting options, including the Web Apps feature of Azure App Service, containers, and virtual machines

#### Container

- Used to create highly portable, scalable app instances that only include the binaries and libraries required to run
- Can be accessed over the Internet by IP address
- Can run on Windows and Linux
- Can scale out as needed
- Represents a single app and its dependencies

### Describe virtual networking, including the purpose of Azure Virtual Networks, Azure virtual subnets, peering, Azure DNS, Azure VPN Gateway, and Azure ExpressRoute

#### VNet

- Created within scope of a region
- Connect VNets through
  - Peering
  - VPN gateways

#### Peering

- Can be used to connect virtual networks within or across regions
- Can be used to transfer data between Azure AD tenants
- Does not require any downtime when peering
- Provides logically isolated, private networks in the cloud
- All resources can communicate with the Internet
- Supports inbound connects using public IP address
- Routed through Microsoft backbone infrastructure

#### ExpressRoute

- Private network connection between organization and cloud services
- More secure, reliable and predictable way to connect than with Internet

### Define public and private endpoints

#### Azure Private Link

- Creates a private endpoint
- Private endpoints use a private IP address from yout VNet

## Describe Azure storage services

- Encryption is enabled by default and cannot be disabled

### Compare Azure storage services

#### Azure Archive

- Stores stuff that is rarely accessed

#### Azure Blob

- Stores a large amount of unstructured data

#### Azure Files

- Supports persistent storage for containers

#### Azure Disk

- Is a virtual hard disk that is available to VM

#### Azure SQL Database

- Serverless
- Intermittent usage pattern and a low compute utilization

### Describe storage tiers

#### Hot

- Highest performance and lowest latency
- Expensive
- Used for frequent access

#### Cool

- For infrequent access
- Must be stored for at least 30 days
- Incurs penalties for data deleted within 30 days

#### Archive

- Rarely accessed
- Not available at account level, configured on the blob
- Incurs highest rehydration cost

### Describe redundancy options

#### Local (LRS)

- Replicates in one datacenter

#### Zonal (ZRS)

- Replocates data among three availability zones

#### Geo (GRS)

- Stores three copies of data in each of two regions

#### RA-GRS

- Provides read access

### Describe storage account options and storage types

#### Standard general purpose v2

- Supports Blob, Queue, and Table Storage

#### Premium block blob

- Only supports blob storage
- Highly unstructured

#### Premium file share

- Only supports file shares

#### Premium page blob

- Only supports page blob storage
- Continuous stream of bytes

### Identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure File Sync

### Transfer on premise VHD to Azure

- AzCopy
  - CLI tool that can be used to upload or download data to and from Azure Blob
- Azure Storage Explorer
  - GUI tool to manage storage resources

### Azure Files

- Accessed using
  - Server Message Block (SMB)
  - Network File System (NFS)
- Shared access signature (SAS) is not required
- Can be used to periodically migrate data

### Describe migration options, including Azure Migrate and Azure Data Box

#### Azure data box gateway

- Migrate data periodically using SMB
- Securely transfer large amounts of data to and from Azure data box
- Is a virtual appliace you run on premises which presents an SMB endpoint

#### Azure data box heavy

- Cannot periodically transfer data
- Is a physical data transfer service that transfers up to 100TB
- Data is transferred to box and shipped to datacenter

#### Azure data share

- Cloud based storage service that allows users to share data across multiple devices

## Describe Azure identity, access, and security

### Describe directory services in Azure, including Azure Active Directory (Azure AD) and Azure Active Directory Domain Services (Azure AD DS)

#### Azure AD

- Does not require integration with an on premises AD
- Web apps must be registered with Azure AD to support services
- Supports authZ through RBAC
- Transfer
  - All subscriptions will lose access
  - System assigned managed identities are not automatically reenabled
  - A subscription that owns an AKS cluster will lose functionality

##### Plans

- Free
  - Synchronize on premise directory
  - Supports SSO
- Premium P1
  - Supports RBAC and conditional access
- P2
  - Supports Identity protection, self service entitlement management and privileged identity management
- Premium
  - Azure AD Application Proxy
    - Publish on premise web apps
  - Ablility to reset passwords

### Describe authentication methods in Azure, including single sign-on (SSO , multifactor authentication, and passwordless

#### Multifactor authentication server

- Required for auth when supporting users located on premises Active Directory only

#### Multifactor authentication service (Cloud)

- Required for auth when users located on Azure AD only
- Recommended for federated users

#### Supported types

- Password
- SMS
- Voice call
- App password (MFA)
- Security questions (SSPR)
- Email (SSPR)

### Describe external identities and guest access in Azure

### Describe Azure AD Conditional Access

### Describe Azure role-based access control (RBAC)

### Describe the concept of Zero Trust

- Least privelage

### Describe the purpose of the defense in depth model

- Is a strategy to implement multiple layers of security to slow down an attack and provide early alert telemetry

### Describe the purpose of Microsoft Defender for Cloud

- Supports monitoring, security recommendations, and advanced threat protection for cloud and on premis VMs
- Native integration with Defender Antivirus
- Not limited to Windows
- Can automatically discover and assess security for new Azure resources
- Designed to help protect Azure cloud, non-Azure cloud and hybrid computing resources
- Protect against threats

#### Dashboard

- Overall compliance score
- Number of passing and failing assignments

### Azure Information Protection (AIP)

- Provides a way to classify and organize documents and files through labels

### Azure Advanced Threat Protection (ATP)

- Uses information from on premis AD signals to identify, detect and investigate advanced threats

### Mircosoft Sentinel

- Build a baseline behavioral profile of organizational entities to identify anomalous activity
- Is a security information and event manager platform thet can analyze data using ML to identify threats

### Network security group (NSG)

- Allow or denies inbound traffic to a specific VM from specific IP address or ports
- Does not allow to create a policy that restricts network traffic
- Can only protect resources in a single subscription

### Application security group (ASG)

- Allows you to organize similar server to easily define and implement security policies
- Provides the possibility to group network interfaces of VMs per service tier and give them human readable labels
- More meaningful than NSG
- Apply to servers only

### User defined routes (UDR)

- Custom routing tables that are used to override and supplement the default routing tables

### DDos protection

- Prevent a malicious flood of HTTP traffic
- Basic is enabled automatically, standard is not setup automatically
- Can link multiple VNets to same protection plan

### Azure firewall

- Create a rule that restricts network traffic across subscriptions

### Application gateway

- Load balancing solution that uses routing

### Traffic manager

- Allows users to access Azure resources from a datacenter nearest to them using DNS

# Describe Azure management and governance (30–35%)

## Describe cost management in Azure

### Describe factors that can affect costs in Azure

#### Compare the Pricing calculator and the Total Cost of Ownership (TCO) calculator

##### Azure pricing calculator

- Estimate the monthly cost of a cloud solution
- Linux is cheaper than windows
- Factors
  - Instance type
  - Number of instances
  - Operating system
  - Region
  - Tier

##### Total cost of ownership calculator

- Compare the difference in cost between current on premises and cloud
- Define server, database, storage and networking workload

### Describe the Azure Cost Management and Billing tool

- Monitor, allocate and optimize cloud spend
- Gives breakdown of the usage and cost of Azure resource

#### Billing zone

- A geographical grouping of Azure regions used to determine billing based on data transfers

### Describe the purpose of tags

- Key value pairs
- Can be use to understand the data in a cost report
- Not inherited
- Cannot be applied to classic resources that exist before ARM

## Describe features and tools in Azure for governance and compliance

### Describe the purpose of Azure Blueprints

- When blueprint is updated and published, assignments of the blueprint are not updated automatically
- When unassigned, all of the resources remain in place but resource locking is removed
- When deleted, any assigned version of blueprint remain in place, a blueprint must be unassigned before deleted

#### Blueprint operator

- Can assign existing published blueprints

#### Contributor

- Can create and delete blueprints

#### Blueprint contributor

- Can manage blueprints

### Describe the purpose of Azure Policy

- A JSON file that is assigned to a scope (resource group or subscription)
- Defines the rules that are to be taken
- Used to meet internal compliance goals and that Azure resources are compliant with company standard

#### Initiative

- A collelction of policies, which are grouped with the aim of achieving a single goal
- When an initiative assignment is evaluated, all of the policies are evaluated
- Can only contain policies that are located in the same subscription

### Describe the purpose of resource locks

#### Locks

- Prevents deletion
- Prevents new resources from being added
- Locks always take orecedence
- Locks can only be applied in the context of scope
- When multiple locks are applied, the most restrictive inherited lock applies
- A lock in a scope is applied to all new resources added to scope

### Describe the purpose of the Service Trust Portal

## Describe features and tools for managing and deploying Azure resources

### Describe the Azure portal

#### UI

- Dashboard
  - Collection of customizable tiles
- Blade
  - Panel that slides out in a navigation sequence

### Describe Azure Cloud Shell, including Azure CLI and Azure PowerShell

#### Azure PowerShell

- Windows cmd
- Connect-AzAccount
- Commands work the same on Mac, Linux and Windows
- Command execution supported in Azure Cloud Shell
- Executes commands in an interactive environment
- Does not support a GUI
- Can be used to create scripts
- Not limited to Windows VM only

#### Azure CLI

- Linux terminal
- az login
- Commands work the same on Mac, Linux and Windows
- Command execution supported in Azure Cloud Shell
- Executes commands in an interactive environment
- Does not support a GUI

#### Azure Cloud Shell

- Browser cmd
- New-AzVm
- Needs a storage account
- Supports command execution of Azure CLI or PowerShell by choosing Bash/PowerShell
- Timeouts after 20 mins
- Provides a way to run CLI and powershell on mobile

### Describe the purpose of Azure Arc

### Describe Azure Resource Manager and Azure Resource Manager templates (ARM templates)

- Increase default limits on how many select resources of each type can be provisioned
- Uses JSON
- Get template
  - Export from resource
  - Export from resource group

## Describe monitoring tools in Azure

### Describe the purpose of Azure Advisor

- Analyzes resource configurations and help optimize deployments
- Makes recommendations on performance
- Makes shutdown recommendation based on CPU and outbound network utilization

### Describe Azure Service Health

- Provides information about planned maintenance and advisories such as deprecated offerings
- Provided through global level and individual service level
- Use to verify planned maintenance
- Use cases
  - Health advisory
    - Notified if App Service exceeds the usage quota
    - View features that are planned to be deprecated
  - Reports planned maintenance
  - Implement webhook to display health incidents
  - Health history
    - Check how many times app has been unavailable
  - Health alerts
    - Receive a text message when maintenance is planned

### Describe Azure Monitor, including Log Analytics, Azure Monitor alerts, and Application Insights

#### Azure Monitor

- Collects resource on applications, guest OSs, resource operations, tenant level services, and information about the health and operation of Azure
- Locations
  - Azure Log analytics workspace
  - Azure storage account
- Need diagnostic enabled -> Event logs, performance counters, crash dumps
- Can use autoscale to add or remove resources
- Begins collecting data as soon as you add a resource

##### Application insights

- Visually analyze telemetry data
- Enables developers to improve app performance and usability

## Cloud bursting

- Resources are provisioned when on-premise servers reach 100% resource capacity

## Cloud Adoption Framework (CAF)

### Define strategy

- Define the business justifications and the expected outcome of adoption

### Plan

- Align actionable adoption plans with business outcomes

### Ready

- Prepare the cloud environment for planned changes

### Innovate

- Develop new cloud native or hybrid solutions
