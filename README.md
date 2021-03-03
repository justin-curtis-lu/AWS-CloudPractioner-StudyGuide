# AWS-CloudPractioner-StudyGuide
Study Guide for AWS Cloud Practioner Exam

4 Main Sections: Billing and Pricing, Cloud Concepts, Technology, and Security

# Billing and Pricing

### AWS Reports = AWS Cost and Usage Reports [Overview]

- composite overview of costs and usage
- provides comprehensive billing data
- most granular
- per hour on a specific date

### AWS Cost Explorer [Trends]
- Identifies areas that need further inquiry
- Provides trends you can use to understand costs
- provide usage based forecasts of estimated months
- visualize, understand

### AWS Cost allocation tags

- help save money at a detailed level

### AWS Budgets

- lets you set custom alerts when usage exceeded

### AWS Bills

- For history of bills and payment

### AWS Pricing Calculator [Estimation]

- create estimated usage costs for all resources on AWS

### Consolidated Billing

- combine usage to receive volume discounts
- Used through AWS organizations
- multiple accounts recieve one bill

### AWS Migration

- Ability to pay as you go
- No upfront costs
- Discount on upfront payments
- cheaper variable and upfront costs

### AWS Organizations

- used to manage multiple accounts
- can create groups of accounts
- can group accounts into organizational units (OU)
- Service Control Policies
    - control permissions for accounts
    - can apply to a OU or an indivual account

### Support Plans

- Basic
    - limited selection of Trusted advisor checks
    - 0
- Developer
    - limited selection of Trusted advisor checks
    - 20
- Business
    - All checks
    - 100
    - Eg: includes all AWS Trusted advisor checks at lowest cost
- Enterprise
    - all checks
    - Concierge
    - TAM
    - 15,000

### Support Center

- create help case

### Cost of an EC2 Instance

- never pay fees when terminating instance
- Instance Type
- AMI Type
- Region

### Service Types

- On demand
    - short term, irregular workloads that cannot be interrupted
    - no termination fees
    - pay no upfront costs
    - charged per second on hourly basis
    - pay as much as you use
    - Eg: One day without interruption, 3 months without interruption
- Reserved instances
    - billing discount applied to on demand instances
    - Eg: 90-100 percent usage, hosting EC2 instance where utilization is guaranteed to be consistent for long
    - do not require commitment
    - standard and convertible
    - highest savings : 3 year standard
- spot instances
    - flexible
    - can withstand interruptions
    - short time
    - do not require contracts or commitment
    - Eg: A few days with interruption allowed
- dedicated hosts
    - physical servers with EC2 instances
    - existing server bound licenses
    - fully dedicated to your use, most expensive
- Savings Plan
    - commit to 1 or 3 year plan

### AWS Landing Zone

- provides baseline environment to get started with multi account architecture
- AWS account vending machine  (AVM)
    - provisions and configures new accounts

### Cost Benefits of going cloud

- Reduced Total Cost of Ownership (TCO).
    - Power consumption of the data center
    - Labor costs to replace old servers
    - TCO Calculator used to do cost benefit analysis of moving to the cloud
- Reduced operational expenditure (opex).
- pay for what you use
- pay less when you reserve
- pay less with volume based discounts

### AWS Free tier

- some services always free - lambda
- some free for 12 months
- some trials

### AWS Billing Dashboard

- pay your AWS bill

# Cloud Concepts

### Cloud computing

- on demand delivery of IT resources and applications through the internet
- **increased speed and agility**:  Decreased acquisition time for new compute resources
- **stop spending money on running data centers**
- only pay when you consume the resources ( **trade capital expense for variable expense** )
- **Massive economies of scale**
- **Don't need to guess capacity** → Can scale up or down accordingly
- Launches rapidly instead of waiting weeks for IT to implement
- **global in minutes** ( multiple regions )
- Use loosely coupled components.
    - that way if one service fails, everything else is still good
- assume everything will fail
- Implement elasticity
    - this means we "create systems that scale to required capacity on changes in demand"
    - this does NOT mean that we spread the load across regions
    - this does NOT mean that we divert to instances with higher capacity
- Design for scalability
- using API, allows cloud resources to be managed progammatically

### Deployment Models

**On-Premise Deployment**

- private cloud deployment
- resources deployed on premise by using virtualization
- Eg: Banks

**Cloud**

- fully utilize cloud computing
- run, migrate, design entirely for the cloud
- Eg: Startups

**Hybrid**

- using both cloud and on-premise
- Eg: Company

### Cloud Benefits

- Stop spending money on running and maintaining data centers
- Benefit from massive economies of scale
- Go global in minutes
- aggregated cloud usage from large number of customers saves money

### AWS Global infrastructure 

- 69 AZs
- 22 geographic zones
- Compliance with data and legal requirements
- Proximity to your customers
- Available services within a region
- Pricing

### AWS Well-Architected Framework [ 5 Pillars ]

- Performance Efficiency Pillar
    - emphasis on making informed decisions on backdrop of data
    - using computational resources to efficiently meet system requirements
    - designing systems to go global in minutes
- Operational Excellence
    - responsiveness, operational standards, automated process
    - run workloads effectively, gain insights
    - run systems to deliver business value, performing operations as code
- Reliability
    - workload to consistently and correctly perform its intended functions
    - recover from disruptions
    - dynamically acquire computing resources
    - Eg: consistently perform intended functions
- Security
    - protecting data, systems, and assets
    - automate security
- Cost Optimization
    - ability to run systems at lowers cost

### AWS Cloud Adoption Framework

- Business
    - move from model w/ business and IT into business that integrates IT
    - create strong business case for cloud adoption
    - Eg: Business manager
- Governance
    - how to update staff skills and organizational process
    - align IT with business
    - EG: Program managers
- People
    - helps HR prepare people for cloud adoption
    - organization wide management strategy for cloud adoption
    - helps prioritize training, staffing
    - Eg: HR, Staffing, peoples managers
- Operations
    - recovering IT workloads to meet requirements of business stakeholders
    - Eg: IT operations managers
- Secuirty
    - identify areas of non compliance
    - meets security objectives
    - Eg: CISO, It security
- Platform
    - patterns and principles for implementing new solutions on cloud
    - Eg: IT managers, CTO
    - Eg: Design, implement, and optimize AWS based on business goals and perspective

Meta Data vs User Data

- Metadata is parameters and attributes for instance configuration, user data is info passed to instance OS during execution

AWS CLI

- safest way if PC w/o console
- run scripts
- used in a programmatic manner

AWS SDK

- use AWS through API designed for your platform
- call AWS through programming languages

AWS Console

- web face interface

AWS Personal Health Dashboard [User side]

- user specific view on availability and performance of AWS services
- service that prompts users w/ alerts and notifications on AWS activities, issues, changes
- provides a customized view of the health of specific AWS services that power a customer's workloads running on AWS

AWS Service Health Dashboard [AWS side]

- AWS Service availability

### Application Migration (6 Rs)

Refactoring

- migration strategy which changes how application is architected and developed typically by using cloud-native features

Repurchasing

- replacing existing application with cloud based version (AWS Marketplace)
- move from traditional license to software as a service
- migrate from customer relationship management to Salesforce
- Eg: move to a different product

Rehosting

- move app to cloud
- move applications without change
- lift and shift

Replatforming

- optimizing aspects, w/o changing core architecture
- lift tinker and shift
- alter a little

Retaining

- keep applications critical in source environment

Retire

- turn off useless

Subnet

- section of VPC
- range of IP addresses
- private
    - only you have access
    - for storage
    - Eg: isolate databases containing personal info
- public
    - public has access
    - for your website
    - Eg: Support customer facing website

VPC

- You set the rules, you define
- no cost
- can configure endpoints and subnets
- establish boundaries on your AWS resources
- isolated section of the cloud where you can launch your resources in a virtual network
- Security group
    - controls inbound and outbound traffic, virtual firewall, denies all inbound, allows outbound by default
    - stateful packet filtering
    - remember previous decisions for previous packets
- NACL
    - controls traffic at subnet level
    - stateless packet filtering , remember nothing
    - by default allow all inbound and outbound

    **AWS Direct Connect**

    - enables connection between data center and VPC
    - Eg: Dedicated connection between VPC and on - premise data center

    **Virtual Private Gateway**

    - VPC and private network
    - Eg: VPC and internal cooperate network

    **Internet Gateway**

    - connection between VPC and internet

AZ

- isolated portion of AWS infrastructure
- w/in a region
- single data center / group of data centers w/in a region
- deploying in multiple zones, elastic load balancer, regions = "design for failure"

Region

- separate geographical location w/ multiple locations
- 2 or more AZS
- data not replicated outside of a region unless you configure it
- isolated from other regions
- factors
    - Compliance with data governance and legal requirements
    - proximity to customers
- If a company wants maximal uptime, they should deploy their application across multiple regions

Edge location

- cache copies of content for faster delivery
- Used by CloudFront for caching
- don't spread the load among multiple resources

Cloud Computing models

- Infrastructure as a service
- Platform as a service
    - Amazon Lightsail
- Software as a service

Vertical scaling

- upgrade server with larger hard drive

Horizontal scaling

- add more hard drives

# Technology

Amazon EC2 Instance

- You manage almost everything about your EC2 instance
- General Purpose
    - all around
    - Eg: Application, gaming servers
- Memory Optimized
    - large datasets in memory
    - Eg: High performance databases
- Compute Optimized
    - batch processing workload
    - high performance processors
- Storage Optimized
    - large datasets on local storage
    - suitable for data warehousing
- Accelerated Computing
    - use hardware accelerators
- Pay for instance type, region, AMI

### EC2 Storage Concepts

Elastic Block Store (EBS)

- mounted onto an EC2 instance, provides persistent block storage volumes
- store data in **single AZ**
- thus we replicate the volume in the same AZ
- if EC2 instance terminates, REMAINS (PERSISTENT)
- retention
- create snapshots in another region
- create snapshots to ensure data is left safe

Elastic File system (EFS)

- mounted onto an EC2 instance, provide filesystem
- stores data across **multiple AZs**
- shared file folders
- useful when lots of services and resources need to access same data

Instance Store (TEMP)

- block level storage volumes, behave like hard drives
- terminates WITH instance
- ideal for temp data
- store data in attached resource
- not long term

### Auto Scaling Concepts

Elastic Load Balancing

- distributes traffic amongst multiple EC2 instances
- Might spread requests to three instances so not all one instance has to deal with the entire workload

Auto-Scaling Group

- monitors applications and scales up or down w/ instances accordingly
- Dynamic scaling
- predictive scaling

Auto Scaling + Load Balancing

- Auto scaling will create 5 instances for traffic
- Load balancing will distribute the requests among the 5 instances

AMI

- launch snapshot of an EC2 instance

AWS CodePipline

- automate deployment

### AWS Snow

AWS Snowcone

- 2cpus , 4gb memory, 8tb

AWS Snowball

- transfer large amounts of data
- edge storage optimized
    - optimal for large scale data migrations
    - 80 tb , 40vcpu
- edge compute optimized
    - optimal for machine learning, local computing , etc.
    - 42 tb, 52 vcpu

AWS Snowmobile

- 100 PB of data, shipping container, physical

### Database / Storage Tech

Amazon Neptune

- Graph database service

**Amazon DynamoDB**

- key-value database service = NO SQL (ITEMS NOT OBJECTS)
- no SQL
- fast and reliable
- server less
- do not need to manage underlying infrastructure
- automatically scales for you hence ^
- Eg: Server less, key-value, scaling scaling 10 trillion request per day
- Amazon DynamoDB Accelerator
    - in-memory cache for DynamoDB
    - improves response times

**Amazon RDS**

- Has database engines such as : Aurora, PostgreSQL, etc.
- sql
- can do Microsoft
- read/write
- simplifies relational database admin tasks
- automatically scales
- multi - AZ
- read replicas = offloading reads of the database
- EG: Using SQL, storing data in amazon aurora
- Db2 is not supported

**Amazon Aurora**

- sql
- enterprise-class relational database
- 5 times faster than MYSQL 3 times faster than POSTGRESQL
- reduce database cost by reducing unnecessary input operations
- HIGH AVAILABILITY + BACKUPS
- high availability, continuously backs up to s3
- **MySQL or PostgreSQL**

Amazon DocumentDB

- MongoDB

Amazon **Redshift**

- data warehousing for big data analytics

Amazon ElasticCache

- adds caching layers on top of your database to help improve requests
- Redis and Memcached

Amazon QLDB

- ledger database service
- complete history

Hosing database on Ec2 instance

- self managed
- we host the database on a EC2 instance when you want as much control as possible over it

Amazon Managed Blockchain

- create and manage block chain networks

AWS Database Migration Service

- simplify the migration of a database to AWS
- can use to test applications, combine several databases into one
- Eg: Oracle migrates database to AWS Cloud

Amazon S3

- **object level storage: data, metadata, and a key**
- can be backup files, media files, documents, etc.
- OBJECTS ( as key value )
- Unlimited storage, max file size is 5 TB
    - standard
        - frequent accessed data, stored in 3 AZS
    - standard infrequent access 1-A
        - infrequently accessed data,
        - lower storage price higher retrieval price
        - still immediately avaliable
    - standard one zone infrequent access 1-A
        - 1 AZ, cheap on storage, easily reproduce data if AZ fails
    - S3 Intelligent
        - 30 consecutive days
        - moves between standard and standard infrequent 1-A
    - Glacier
        - low-cost storage, ideal for data archiving, retrieval in few minutes to few hours
        - data can be stored onto glacier using → AWS Glacier API, AWS Glacier SDK, AWS S3 Lifecycle policies
    - Glacier Deep Archive
        - same as glacier but retrieval within 12 hours
- accessed via url
- can not be attached to EC2 instances
- can serve a static website
- lowest cost
- very durable
- pay for storage, requests/data retrievals, data transfer, and management and replication

Storage Gateway

- pay for total storage, storage class
- hybrid cloud storage with local caching

### Docker concepts

Amazon EKS

- run containerized applications on AWS
- runs Kubernetes

Amazon ECS

- docker as a service, highly scalable, high performance, container orchestration service that supports Docker containers

Fargate

- server less compute engine, works with ECS and EKS
- microservices where you don't worry about infrastructure, pay for resources required to run on container
- do not need to provision or manage servers
- manages server infrastructure for you

### Machine Learning Tech

Amazon Textract

- ML service which extracts text and data from scanned documents

Amazon Sagemaker

- service that enables you to quickly build, train ML models
- SageMaker enables developers to create, train, and deploy machine-learning models in the cloud.

Amazon Kendra

- Amazon Kendra is an intelligent search service powered by machine learning

AWS Comprehend

- natural language processing service uses ML

AWS DeepRacer

- test reinforcement models

### Artificial Intelligence Tech

Amazon Augmented AI

- human review ML workflows

Amazon Transcribe

- convert text to speech

Amazon Lex

- service which enables you to build conversational interfaces using voice and text

Amazon Fraud Detector

- identify fraudulent online activities

### Messaging

Amazon SQS [Most common]

- send store and receive messages

SNS vs SQS ( mails vs queue)

- Simple notification service [**SUBSCRIPTION**] → sends notifications to subscribers via multiple protocols ( HTTP, email, etc.), webhooks, plain text emails Eg: PubSub
- Simple Queue Service → Queue up messages, good for delayed tasks, queueing up emails
    - with SQS, we do not have message subscription
    - helps decouple resources in the cloud

SNS vs SES (emails)

- SNS does not allow HTML ( practical and internal ), plain text emails, most services trigger SNS not SES (for example billing alarm)
- SES allows html (professional, marketing, and emails)

### Serverless

- AWS Step Functions
- Amazon DynamoDB
- Amazon SNS
- Lambda

### Global Services

- Amazon Route 53
- Amazon CloudFront
- IAM

### Other Services

### AWS CodeStar [User-interface]

- provides a unified user interface, enabling easy management of software development activities in one place

Elastic Transcoder 

- transcodes videos to streaming formats ( old )

AWS Elemental media convert

- overlay images, insert video clips, robust UI, etc. more things

Amazon Global Accelerator

- optimize user to application path

AWS Batch

- executes batch computing workloads across AWS services

Amazon Elastic Map Reduce

- do not need to manage underlying infrastructure

AWS X-Ray

- helps developers analyze and debug production

AWS Lambda

- server less code
- only pay for compute time

AWS Cloud9

- IDE to run test and debug code for lambda functions

AWS Marketplace

- digital catalog for software

Amazon CLI

- automate scripts
- use AWS services

Amazon Route 53

- domain handling
- Connect user requests to infrastructure in and out of AWS
- takes 24 to 48 hours due to DNS resolvers TTL
- can serve different versions of website for global content
- transfer domain name to a IP Address
- most useful for disaster recovery

AWS Quickstarts

- automate deployment of workloads into your AWS environment

AWS Elastic Beanstalk

- automatically handles deployment details, load balancing, etc.
    - adjust capacity
    - load balancing
    - automatic scaling
    - application health monitoring
- Eg: .Net and Java

AWS Outposts

- run infrastructure in hybrid cloud approach
- extend AWS infrastructure to your on-premise data center

Amazon Cognito

- add user sign up and access control to your web application

Amazon systems manager

- automate operational tasks across aws resources

Transfer Acceleration

- fast and easy transfer of files over long distances between client and s3 bucket using edge locations

Amazon EMR

- process vast amounts of data

Amazon Kinesis

- streaming data

Amazon Firehose

- load streaming data, near real time analytics

AWS Glue

- move data between storage

### Cloud (Tech)

AWS **CloudFront [important]**

- content delivery service
- utilizes edge locations to deliver content to customers
- can also help prevent a Ddos attack

**CloudFormation**

- *infrastructure as JSON*
- can launch a database using
- instead of manually using the console to configure settings, write the code in Json and AWS will automatically set up the needed infrastructure

### Business Centric Services

- Amazon Connect
    - call center
- Workspaces
    - Virtual remote desktop
- WorkDocs
    - content collaboration service
- Chime
    - online meetings video confrencing
- WorkMail
    - business emails
- Pinpoint
    - targeted emailing, SMS
- SES
    - marketing notifications
- Quicksight
    - data source no programming knowledge needed

# Security

**Amazon CloudWatch** [general metrics system wide] [ utilization ]

- provides data to monitor applications and respond to system wide changes
- monitor utilization and performance
- access metrics from a single dashboard
- configure alarms for your metrics
- Eg: Monitor AWS infrastructure, view metrics and graphs, configure automatic actions

**Aws CloudTrail** [unusual activity all across]

- complete history of API calls
- "trail" , know who to blame
- detect unusual activity
- Eg: track user activities and API requests, filter logs to assist with operational analysis

**Amazon Inspector** [Focus on instance] [security focused ]

- checks applications for security vulnerabilities
- prove an EC2 instance is hardened
- runs a security benchmark against EC2 instances
- can perform both network and host assessments
- installs the AWS agent on your EC2 instance
- CIS (popular security benchmark)
- audits a single EC2 instance , gives a report

**AWS Trusted advisor** [real time guidance]

- online tool that inspects your AWS environment and provides real time guidance
- EG: Review security of S3 Bucket
- performance
    - checks for service limits and overutilized instances
- cost optimization
    - checks for idle resources
- fault tolerance
    - improve applications availability and redundancy
    - Eg: Deploy application across multiple AZs
- security
    - review permissions and roles
    - 
### AWS Artifact

- access AWS security and compliance reports
- audit or inspection needed
- AWS Artifact Agreements
    - sign agreement with AWS
- AWS Artifact Reports
    - info on AWS

TAM

- guidance, communication with company (human)

AWS Support

- answer questions

AWS Shared Responsibility Model

- both
    - awareness and training
    - config + patch management
- AWS
    - Configuring AWS infrastructure devices
    - Maintaining virtualization infrastructure
    - physical repairs, security, etc.
    - disk disposal
    - AWS is responsible for security of the cloud
    - Regions, AZs, Edge locations
    - Eg: Maintain network infrastructure, implementing physical security controls at data centers, maintaining servers that run EC2 Instances
- Customer
    - Creating IAM users and groups
    - customer data
    - platform, applications, identity and access management
    - network traffic protectiong
    - client and server side encryption
    - Training company employees how to use AWS
    - Configuring Security groups
    - Ensure data is encrypted at rest
    - security and patching of guest OS
    - Configuring Network Access Control Lists
    - EG: Patching software on EC2 Instance, Setting permission for S3 objects

AWS Compliance Programs

- set of internal policies and procedures for a company to comply with laws, rules, etc.
- Health insurance portability and accountability act
- payment card industry data security standard
- range of compliance programs

EC2 Security Group

- control access to EC2 instances

AWS IAM

- manage access to AWS services and resources
- policy
    - grants or denies permissions to AWS resources
    - A policy might not allow you to do ____ on an EC2 instance whereas the security group prohibits entire accessibility to an instance
    - Eg: Use only 1 S3 bucket, not all
- role
    - temp access or permissions
- User
    - identity you can create
    - name and credentials
- Group
    - collection of users
    - assign policy to a group
- root
    - master
    - do not use for everyday tasks

Principle of Least Privledge

- give the most minimal privileges

AWS MFA

- provides an additional layer of security
- system administrator add an additional layer of login security to a user's AWS
Management Console

AWS KMS

- create, manage, and use cryptographic keys

Amazon Shield

- DDOS protection
- Standard
    - protects all AWS customers at no cost
- Advanced
    - paid, provides detailed diagnostics, ability to detect and mitigate Ddos attacks

Amazon Guarduty

- provides intelligent threat detection

AWS WAF

- monitor network requests
- Web application firewall
- walls allow or deny traffic
- can purchase rules from other partners (rule sets)
- OWASP TOP 10 (SQL Injection, etc.)

PenTesting

- authorized simulated cyberattack on a computer system
- 8 services permitted ( EC2, Elastic Beanstalk, etc.)
- Prohibited : flooding, DDOS
- BALLRACE
- Request and wait for approval from the customer's internal security team, and then conduct testing.

Amazon Macie [S3]

- fully managed service which manages S3 activity for anomalies
- Uses ML to analyze logs
- information loss
- ransomware
- credential loss

AWS VPN

AWS Certificate Manager

- keep track of expiry dates of SSL/TLS certificates

AWS Customer Compliance Center

- AWS answers to compliance questions
- overview of AWS risk and compliance
- auditing security checklist

APN consulting partners

Disaster recovery

- warm stand by = fastest
- backup and restore - longest
