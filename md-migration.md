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


  
  
  
#### EC2 instance connect as an alternative to SSH 
- A browser based terminal 
- Where to access?
  - In AWS console, select an EC2 instance → select ‘Connect’ blue button at the top tabs → select connect with ‘EC2 instance connect’
- Only available for Amazon Linux 2 AMI

[ go back ](#index)
