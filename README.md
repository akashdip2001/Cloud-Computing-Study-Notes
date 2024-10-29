# Cloud Computing

- [1. Introduction to Cloud Computing](#introduction-to-cloud-computing)
- [2. Cloud Service Models](#cloud-service-models)
    - [IaaS (Infrastructure as a Service)](#iaas-infrastructure-as-a-service)
    - [PaaS (Platform as a Service)](#paas-platform-as-a-service)
    - [SaaS (Software as a Service)](#saas-software-as-a-service)
- [3. Cloud Deployment Models](#cloud-deployment-models)
    - [Public Cloud](#public-cloud)
    - [Private Cloud](#private-cloud)
    - [Hybrid Cloud](#hybrid-cloud)
- [4. Virtualization](#virtualization)
    - [Types of Virtualization](#types-of-virtualization)
    - [Hypervisors](#hypervisors)
- [5. Cloud Providers](#cloud-providers)
- [6. Basic Cloud Services](#basic-cloud-services)
- [**7. EXAM**](#EXAM)

---

## 1. Introduction to Cloud Computing

**Cloud Computing** is the delivery of computing services over the internet (“the cloud”) to offer faster innovation, flexible resources, and economies of scale. These services include servers, storage, databases, networking, software, analytics, and more.

### Key Characteristics:
- **On-Demand Self-Service**: Users can access services as needed.
- **Broad Network Access**: Services available over the internet.
- **Resource Pooling**: Shared resources for multiple users.
- **Scalability**: Quickly scale up or down based on demand.
- **Measured Service**: Pay-as-you-go based on usage.

### Example:
Think of streaming platforms like Netflix; you don’t need to store all movies or set up a server to watch them. Cloud computing works similarly for business applications and services.

---

## 2. Cloud Service Models

### IaaS (Infrastructure as a Service)
Provides virtualized computing resources over the internet. Examples include virtual machines, storage, and networks.

- **Examples**: Amazon Web Services EC2, Google Cloud Compute Engine, Microsoft Azure VM.
- **Syntax Example** (for provisioning a VM in AWS using CLI):
  ```bash
  aws ec2 run-instances --image-id ami-0abcdef1234567890 --count 1 --instance-type t2.micro --key-name MyKeyPair
  ```
- **Output**: A virtual machine instance running on AWS.

### PaaS (Platform as a Service)
Provides hardware and software tools over the internet, typically for application development. 

- **Examples**: Google App Engine, Heroku, AWS Elastic Beanstalk.
- **Syntax Example** (Deploying a web app in Google App Engine):
  ```yaml
  runtime: python37
  entrypoint: python main.py
  ```
- **Output**: A fully managed platform that runs the web app without worrying about server maintenance.

### SaaS (Software as a Service)
Delivers software applications over the internet on a subscription basis.

- **Examples**: Google Workspace, Microsoft Office 365, Salesforce.
- **Syntax Example**: Often SaaS platforms use APIs; for example, using Google Sheets API to read data.
  ```python
  from googleapiclient.discovery import build
  service = build('sheets', 'v4', credentials=creds)
  result = service.spreadsheets().values().get(spreadsheetId=SPREADSHEET_ID, range=RANGE_NAME).execute()
  ```
- **Output**: Data fetched from a Google Sheet.

---

## 3. Cloud Deployment Models

### Public Cloud
Third-party providers offer resources and services to the public over the internet.

- **Examples**: AWS, Microsoft Azure, Google Cloud Platform.
  
### Private Cloud
Dedicated resources used by a single organization, either managed internally or by a third-party.

- **Examples**: VMware Private Cloud, IBM Cloud Private.

### Hybrid Cloud
A combination of private and public clouds that allow data and applications to move between them.

- **Examples**: AWS Outposts, Azure Arc.

---

## 4. Virtualization

**Virtualization** is the creation of virtual versions of physical components, such as servers, storage devices, and networks. It allows multiple virtual systems to run on a single physical system.

### Types of Virtualization
- **Server Virtualization**: Divides a physical server into multiple virtual servers.
- **Storage Virtualization**: Pools physical storage from multiple devices.
- **Network Virtualization**: Combines network resources by splitting available bandwidth.

### Hypervisors
Hypervisors are software that creates and manages virtual machines. There are two types:

- **Type 1 (Bare Metal)**: Runs directly on hardware, e.g., VMware ESXi, Microsoft Hyper-V.
- **Type 2 (Hosted)**: Runs on an operating system, e.g., Oracle VirtualBox, VMware Workstation.

**Syntax Example** (Creating a VM using VirtualBox CLI):
```bash
VBoxManage createvm --name "my_vm" --register
VBoxManage modifyvm "my_vm" --memory 1024 --cpus 2
```

---

## 5. Cloud Providers

### Major Providers
- **Amazon Web Services (AWS)**: A leading provider with services like EC2, S3, Lambda.
- **Microsoft Azure**: Known for integration with Microsoft products; services include Azure VM, Azure Functions.
- **Google Cloud Platform (GCP)**: Focused on AI and ML, with services like Compute Engine and BigQuery.
- **IBM Cloud**: Known for enterprise-level security and IBM Watson AI.

---

## 6. Basic Cloud Services

### Compute Services
Enable users to create, configure, and manage virtual servers.

- **Example**: AWS EC2, Google Compute Engine, Azure VM.
- **Syntax Example** (Launching an EC2 instance in AWS CLI):
  ```bash
  aws ec2 run-instances --image-id ami-12345 --instance-type t2.micro --key-name MyKeyPair
  ```

### Storage Services
Allow users to store and manage data on cloud servers.

- **Example**: AWS S3, Google Cloud Storage, Azure Blob Storage.
- **Syntax Example** (Creating an S3 bucket):
  ```bash
  aws s3 mb s3://my-bucket-name
  ```

### Networking Services
These services manage network resources and control access.

- **Example**: AWS VPC, Google Virtual Private Cloud, Azure Virtual Network.
- **Syntax Example** (Creating a VPC in AWS CLI):
  ```bash
  aws ec2 create-vpc --cidr-block 10.0.0.0/16
  ```

### Database Services
Provide scalable database solutions.

- **Example**: AWS RDS, Google Cloud SQL, Azure SQL Database.
- **Syntax Example** (Creating a database in AWS RDS):
  ```bash
  aws rds create-db-instance --db-instance-identifier mydb --db-instance-class db.t2.micro --engine mysql
  ```

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# EXAM:

### Question 1:
**Question:** Assume that an IT administrator needs to manage a large number of virtual machines efficiently. Which tool can help automate and streamline this process?

**Answer:** Hypervisor Management

---
### Question 2:
**Question:** What technology enables automatic scaling of resources based on demand, ensuring optimal performance and cost-efficiency?

**Answer:** Cloud Orchestration and Auto-scaling

---
### Question 3:
**Question:** What key metric is used to measure the reliability and availability of cloud services?

**Answer:** Service Uptime

---
### Question 4:
**Question:** Which cloud computing technique distributes incoming traffic across multiple servers to prevent overloading and improve performance?

**Answer:** Elastic Load Balancing

---
### Question 5:
**Question:** What practice helps organizations monitor and control cloud spending to optimize resource utilization and reduce costs?

**Answer:** Cost Monitoring

---
### Question 6:
**Question:** What approach involves managing infrastructure through code, enabling automation and version control?

**Answer:** Infrastructure as Code (IaC)

---
### Question 7:
**Question:** What tools and platforms facilitate collaboration among development teams, enabling efficient communication and knowledge sharing?

**Answer:** Collaboration Platforms

---
### Question 8:
**Question:** What cloud computing feature automatically adjusts resource allocation to meet fluctuating demand, ensuring optimal performance and cost-effectiveness?

**Answer:** Auto-scaling

---
### Question 9:
**Question:** What agreement defines the specific service levels and performance metrics that a cloud service provider must meet?

**Answer:** SLA

---
### Question 10:
**Question:** What tools and resources are essential for developers to build, test, and deploy cloud applications efficiently?

**Answer:** Developer Tools

