## Index

- **Background & Miscellaneous**
  - RAID
  - SSL certificate
  - CIDR
  - 1/2/3 tier architecture 
  - DNS
  - Anycast
  - UDP vs TCP
  - Server name indication (SNI)
  - Shared responsibility model for security
  - Durability vs availability
  - Stateful vs stateless in networking
  - Global service, regional service and AZ service lists
  - Common service limits and default values lists
  - Disaster recovery architecture
    - Backup & Restore vs Warm Standby vs Multi site vs Pilot Light
    - RTO & RPO
- **Compute**
  - ***EC2***
    - Operational & efficiency
      - Default instance# limits -- 20 instances per region
      - ParallelCluster 
      - Public addressing
      - Reserved instance vs dedicated instance
      - Scheduled reserved instances
      - HVM(hardware-assisted) AMI vs PV(paravirtual) AMI and their enhanced networking option
      - Placement group -- cluster vs partition vs spread
      - Aws ec2 describe-instances
      - Automation of EC2 configuration tasks
      - Workflow 
        - Normal instance stop behaviours
        - Spot instance interruption behaviours
        - Reserved instance early decommission
        - Instance store-backed instance status
      - Elastic fabric adapter (EFA)
        - Vs elastic network adapter
      - Auto Scaling Group
        - Scaling policy
        - Pre-built AMIs and cross region replication
        - EC2 scale-in: which instance to terminate first?
        - Cool down period
        - Lifecycle hooks
        - Vs AWS auto scaling
    - Security 
      - Key pairs
      - Prerequisite to successfully log into an EC2 instance from CLI/SDK
      - Security group 
        - SSH use port 22 and TCP 
        - Source and destination of rules can be IDs of other security groups
    - Cost
      - Cost to transfer data from EC2 to storage service
      - Billing for different EC2 status
      - Pricing for spot instance
      - Pricing for on-demand instance
      - Cost of EIP
  - ***Lambda***
    - Operational & efficiency
      - Invocation types
        - Integration with AWS services
      - Event source mappings
      - Asynchronous invocation and dead letter queue
      - Lambda@edge 
      - Traffic shifting config
      - Timeout per request: default 3 seconds / maximum 15 minutes
    - Reliability
      - Cloudwatch metrics
    - Security 
      - Encrypt environment variables
    - Comparison
      - Vs EC2
  - ***Elastic Beanstalk***
    - Vs CodeDeploy
  - ***Lightsail***


- **Storage**
  - ***S3***
    - Operational & efficiency
      - Object key & value and data consistency
      - Event notification feature
      - Static website hosting with integration of Route53
      - Object data limit, upload limit and multipart upload
      - Transfer ownership of S3 object to another AWS account
      - Glacier 
        - 3 ways to upload data to Glacier
        - Standard/Expedited/bulk retrieval and provisioned capacity for Glacier
      - Lifecycle policy
        - Waterfall model
        - Constraints
    - Security
      - S3 security measures
      - Cross-origin resource sharing (CORS) in S3 bucket
      - Pre-signed urls 
      - Glacier vault lock policy and vault access policy
      - Server-side encryption
      - Client-side encryption
        - KMS-managed customer master key
        - Client-side master key
      - Comparison
        - EFS vs EBS vs S3
        - S3 select vs Redshift Spectrum vs Athena
  - ***EBS***
    - Operational & efficiency
      - IOPS rate & queue length selection for optimal performance
    - Security 
      - EBS encryption
    - Reliability
      - Auto-replication, attachment to EC2 and live configuration
      - How to automatically back up EBS volumes? 
    - Comparison
      - EBS types: SSD vs HDD
      - frequent/infrequent access for large & sequential operations
      - Instance store vs EBS
      - Vs EFS vs S3
      - Snapshots vs RAID 1
  - ***EFS***
    - vs EBS vs S3
  - ***FSx***
    - FSx for windows file server
    - FSx for Lustre
    - Vs EFS
  - ***DataSync***
  - ***Instance store***
  - ***Storage Gateway***
  - ***Snowball edge***





Database 
RDS
Operational & efficiency
RDS cloudwatch metrics & enhanced monitoring metrics 
How to access the OS of a DB?
Parameter groups
MySQL engines: InnoDB vs MyISAM
Security 
IAM DB authentication
SSL is Available for in-transit encryption between server and DB 
Reliability 
Multi-AZ Deployment
Vs read replica
Aurora vs other RDS(MySQL etc) multi-AZ architecture
Comparison
Vs DynamoDB
Aurora
Serverless mechanism 
Serverless DB cluster vs provisioned DB cluster
Aurora Cluster: Read/write roles and endpoints
Parallel query
Failover of primary instance
DynamoDB
Vs RDS
Serverless: on-demand mode vs provisioned capacity vs auto scaling
Partition keys
DynamoDB Accelerator (DAX)
DynamoDB stream
Integration with Lambda
Integration with Kinesis Adapter
Redshift
Vs RDS
Spectrum vs Athena vs S3 select
Enhanced VPC routing
Redshift and Business intelligence
ElastiCache
Redis AUTH





Networking & Content Delivery
VPC
Route Table
A basic architecture of a 2-tiers web app
VPC peering and invalid config
Elastic Network Interface (ENI) and attach/detach mechanism
Bastion host
Vs NAT
NAT Gateway
Vs NAT instance
Vs egress-only internet  gateway
NACL
Default and custom NACL
NACL rules evaluation
Connect AWS service to VPC
VPC endpoints
Interface endpoints
Gateway endpoints
Custom VPC endpoint service
EC2/RDS instance → internet gateway → AWS service
Connect on-premise to VPC
Direct Connect
Mechanism 
Virtual interfaces: private, public and transit
VPN
Direct Connect vs VPN
Private virtual gateway vs Direct Connect gateway vs transit gateway
CloudFront
Signed URLs and signed cookies
Origin failover
Origin Access Identity (OAI) 
Vs Global Accelerator
Route53
BYOIP: Bring your own IP
Alias 
Routing policy: Geo-Proximity vs geolocation 
Vs ELB
Active-active failover vs active-passive failover
ELB
Network LB vs Application LB vs Classic LB
Routing algorithms 
Weighted target Group for Application LB
Vs Route53
Cross-zone load balancing
Connection draining
Sticky sessions
HTTP use port 80, HTTPS use port 443
API Gateway
How to protect the backend from traffic spikes?
Use X-ray to trace and analyze detailed API calls
Protocol endpoints exposure
App Mesh 
Cloud Map 







Management & Governance
CloudWatch
CloudTrail vs CloudWatch vs X-Ray 
Cloudwatch logs vs CloudTrail vs VPC flow logs
Metrics 
EC2 metrics and detailed monitoring
Lambda metrics
Cloudwatch agent
CloudWatch alarm actions
Vs Cloudwatch Events
Cloudwatch events 
vs cloudtrail
CloudTrail
Event history vs trail
Event types
Monitoring of global service 
System manager
Session manager
Run command 
Vs Opswork 
Vs Appconfig
Vs AWS config
AWS Organizations
Vs resource access manager
Service control policy (SCP) vs IAM policy
AWS Control Tower
Vs organizations
OpsWorks
Vs CloudFormation
CloudFormation
CreationPolicy and cfn-signal
Template structure
Trusted advisor





Analytics 
Elasticsearch Service
Data pipeline
Athena
EMR vs Athena vs Neptune
Vs Redshift Spectrum vs S3 select
EMR
EMR vs Athena vs Neptune
Common use cases
Kinesis
Kinesis data stream architecture
Kinesis data/videos stream + lambda
Reshard operation
Kinesis data firehose





Security, Identity & Compliance
IAM
IAM DB authentication
Access keys
Console sign-in for additional IAM users
Transfer ownership of S3 object to another AWS account 
Cross-account access 
IAM certificate store to manage certificates in regions that do not support ACM
Vs Organizations
STS
How to connect to AWS using login credentials of on-premise networks?
Web identity federation vs SAML-based federation
Vs Cognito vs SSO
Cognito (AWS identity provider)
Identity Pool vs user pool
How to provide temporary aws credentials to third party users by Cognito?
Vs STS vs SSO
WAF
Vs security groups vs NACL
WAF behaviour
Vs GuardDuty
vs Firewall manager vs shield 
Resource access manager (RAM)
Vs aws organizations
Macie 
vs GuardDuty vs Amazon Inspector
vs Rekognition
AWS Shield 
How to defend DDos attacks?
Directory Service
Active directory
Secret manager
CloudHSM
Containers
ECS
Store sensitive data in containers






Application Integration
SNS
SQS
Short polling vs long polling
Standard queue and FIFO queue
MQ vs SQS
Message constraints -- retention period & visibility timeout
SWF
Each workflow execution can run for a maximum of 1 year by default
Step functions vs SWF




AWS Cost Management
AWS Budgets vs Cost Explorer


Mobile
AppSync
Amplify/MobileHub




Developer tools 
CodeDeploy
 Traffic shifting
Vs Beanstalk



End user computing 
Amazon workspaces 




Migration & Transfer
Database migration service

  
  
  
#### EC2 instance connect as an alternative to SSH 
- A browser based terminal 
- Where to access?
  - In AWS console, select an EC2 instance → select ‘Connect’ blue button at the top tabs → select connect with ‘EC2 instance connect’
- Only available for Amazon Linux 2 AMI

[ go back ](#index)
