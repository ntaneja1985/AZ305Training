# AZ 305 Training (Designing Azure Infrastructure)
## Basic Concepts
- ![alt text](image.png)
- ![alt text](image-1.png)

## Designing solutions for Logging and Monitoring
- ![alt text](image-2.png)
- ![alt text](image-3.png)
- Azure Monitor combines all the monitoring activities across all of Azure in a single space.
- ![alt text](image-4.png)
- Metrics are numeric values and we can build charts off that data
- ![alt text](image-5.png)
- ![alt text](image-6.png)
- ![alt text](image-7.png)
- Azure Monitor is free but for storing analytics data, it will cost us money
- In Windows, we used to use PerfMon to gather metrics data, Azure Monitor greatly improves on that.
- ![alt text](image-8.png)
- ![alt text](image-9.png)
- We need to know how we will get our log information into the Log Analytics Workspace. For this purpose we will use Data Collection Rules in Azure Monitor
- ![alt text](image-10.png)
- ![alt text](image-11.png)
- ![alt text](image-12.png)
- ![alt text](image-13.png)
- ![alt text](image-14.png)
- ![alt text](image-15.png)
- ![alt text](image-16.png)
- We can also put Resource Locks on our Log Analytics Workspace.

### Setting up Alerts in Azure Monitor
- ![alt text](image-17.png)
- Signals are conditions for which we want to generate an alert
- ![alt text](image-18.png)
- We can then create action groups
- ![alt text](image-19.png)
- ![alt text](image-20.png)
- ![alt text](image-21.png)
- ![alt text](image-22.png)
- ![alt text](image-23.png)

### Azure Advisor
- ![alt text](image-24.png)
- We can see a list of cost recommendations
- ![alt text](image-25.png)

### Using Azure DDoS protection
- ![alt text](image-26.png)
- ![alt text](image-27.png)
- ![alt text](image-28.png)
- ![alt text](image-29.png)
- ![alt text](image-30.png)

## Designing Authentication and Authorization Solutions
- ![alt text](image-31.png)
- ![alt text](image-32.png)
- ![alt text](image-33.png)
- ![alt text](image-34.png)
- RBAC allows an administrator to give privileges to other users/administrators control over the environment.
- Roles allow us to see what privileges the users are getting.
- ![alt text](image-35.png)
- Global Administrator is the highest role in Azure
- PIM means we can give role access temporarily.
- Users can also request permissions for a short period of time.
- ![alt text](image-36.png)
- ![alt text](image-37.png)
- ![alt text](image-38.png)
- ![alt text](image-39.png)
- ![alt text](image-40.png)
- ![alt text](image-41.png)
- ![alt text](image-42.png)
- We can create custom roles as well
- ![alt text](image-43.png)
- ![alt text](image-44.png)
- ![alt text](image-45.png)
- ![alt text](image-46.png)
- ![alt text](image-47.png)
- We can apply Scopes in a hierarchy
- ![alt text](image-48.png)
- Management Group is used to group together subscriptions
- ![alt text](image-49.png)
- ![alt text](image-50.png)
- PIM(Privileged Identity Management) is a technology that allows us to manage, control and monitor access to resources in the organization. These resources can be inside Microsoft Entra ID, Azure or other Microsoft Online Services such as Microsoft 365 or Microsoft Intune.
- One example of PIM is to give access to resources for a short period of time(Remember SAS tokens)
- ![alt text](image-51.png)
- ![alt text](image-52.png)
- We can conduct Access Reviews to ensure users still need roles.
- Using PIM, we can enforce Multi-Factor Authentication.
- Users who can manage PIMs include Privileged Role Admin or Global Admins
- ![alt text](image-53.png)
- Remember JIT Access
- ![alt text](image-54.png)
- ![alt text](image-55.png)
- ![alt text](image-56.png)
- We can set the date and time to start and end the role assignment
- ![alt text](image-57.png)
- ![alt text](image-58.png)
- ![alt text](image-59.png)
- ![alt text](image-60.png)

### Access Reviews
- ![alt text](image-61.png)
- ![alt text](image-62.png)
- ![alt text](image-63.png)
- ![alt text](image-64.png)
- ![alt text](image-65.png)
- ![alt text](image-66.png)
- ![alt text](image-67.png)
- ![alt text](image-68.png)
- ![alt text](image-69.png)

## Design Governance
- Management group is a root hierarchial system that allows us to separate our different subscriptions
- Subscription allows us to purchase Azure resources.
- Even free resources need to be associated with a subscription
- ![alt text](image-71.png)
- ![alt text](image-74.png)
- Resource Groups cannot be nested
- ![alt text](image-75.png)
- We can have a root management group and then have sub management groups below it
- Each management group can have subscriptions associated with it.
- ![alt text](image-76.png)

### Administrative Units
- In Active Directory, we used to have Organization Units(OU)
- We used to put users inside of an OU and then we could delegate control over resources in that unit.
- Administrative Units(AU) are similar in concept but with some differences.
- AU help us to categorize our objects together and then we can delegate control over those objects to certain administrators.
- ![alt text](image-77.png)
- ![alt text](image-78.png)
- We need Azure AD Premium 1 license to create administrative units
- ![alt text](image-79.png)
- ![alt text](image-80.png)
- ![alt text](image-81.png)
- ![alt text](image-82.png)
- ![alt text](image-83.png)
- In OU, 1 user can be member of one OU only. In AU, a user can be member of several AUs.
- ![alt text](image-84.png)
- ![alt text](image-85.png)
- ![alt text](image-86.png)
- Microsoft Defender for Cloud gives us an overview of the security requirements for our cloud infrastructure.
- We need to pay close attention to security recommendations
- ![alt text](image-87.png)
- ![alt text](image-88.png)

## Design Identities and Access for Applications
- ![alt text](image-89.png)
- Use principle of least privilege
- In Zero Trust Model, we follow JIT Model
- For this we use PIM
- In Azure we have Conditional Access Policies and Compliance Access Policies.
- Zero trust model is all about verifying everything

### Azure Key Vault
- ![alt text](image-90.png)
- ![alt text](image-91.png)
- ![alt text](image-92.png)
- In Azure Key vault we can setup permission model either to be a Vault Access Policy or Azure RBAC.
- ![alt text](image-93.png)
- In Vault access policy we can decide who can do what inside the key vault like whether we can create a key, certificate etc.
- Access Control(IAM) blade allows us to control who has access to these access policies and whether he/she can change the access policy.
- Azure Key Vault is a way to allow tenants or users in Azure to manage their encryptions like encryption keys.
- ![alt text](image-94.png)
- ![alt text](image-95.png)
- ![alt text](image-96.png)
- We can also rotate our keys inside the Azure Key Vault
- ![alt text](image-97.png)
- ![alt text](image-98.png)
- ![alt text](image-99.png)
- We can also do a soft delete of a key


### Application Access Registration(App Registrations) in Azure AD
- Suppose a web app is hosted on-prem on a webserver.
- We want that application to be tied to Azure AD and allow Azure AD to authenticate users and provide a token and control who gets access to that application.
- We want to use Azure AD to authenticate our users on that web app.
- Azure AD has a concept of App Registration and we can generate an access token which is passed to the web-server.
- ![alt text](image-100.png)
- ![alt text](image-101.png)
- This will generate an access token and it will be passed to the web app and the developer needs to use it accordingly
- ![alt text](image-102.png)
- ![alt text](image-103.png)
- ![alt text](image-104.png)
- We have a bunch of endpoints associated with it which the developer needs to use to authenticate the token
- ![alt text](image-105.png)

### Azure AD Application Proxy
- It is a feature of Azure AD that enables users to access on-premise web applications from a remote client.
- Application proxy includes both the Application Proxy service which runs in the cloud and the Application Proxy connector which runs on an on-premises server.
- Think of it as an alternative to Reverse Proxy.
- Azure AD, Application Proxy and Application Proxy connector work together to securely pass the user sign-on token from Azure AD to the web application.
- ![alt text](image-106.png)
- This way we can host an application inside of our own private network and Application Proxy will act as a middleman between our web application hosted in house and the regular internet users.
- ![alt text](image-107.png)
- ![alt text](image-108.png)
- Application proxy ensures that we dont have to open any inbound connections to our firewall
- ![alt text](image-109.png)
- ![alt text](image-110.png)
- ![alt text](image-111.png)
- ![alt text](image-112.png)
- We can download and install the agent on our on-prem server.
- ![alt text](image-113.png)
- ![alt text](image-114.png)
- ![alt text](image-115.png)
- ![alt text](image-116.png)
- ![alt text](image-117.png)
- Http Only cookie prevents against XSS attacks, cross site scripting attacks
- Persistent cookies donot expire when browser is closed.
  
## Designing Data Storage Solution for Relational Data.
- ![alt text](image-118.png)
- ![alt text](image-119.png)
- ![alt text](image-120.png)
- ![alt text](image-121.png)
- ![alt text](image-122.png)
- ![alt text](image-123.png)
- ![alt text](image-124.png)
- ![alt text](image-125.png)
- ![alt text](image-126.png)
- ![alt text](image-127.png)
- ![alt text](image-128.png)
- ![alt text](image-129.png)
- For traffic routing we can use Microsoft Network routing or Internet Routing. 
- Microsoft Network routing is more secure and fast but costs more money.
- ![alt text](image-130.png)
- ![alt text](image-131.png)
- ![alt text](image-132.png)
- ![alt text](image-133.png)
- ![alt text](image-134.png)
- We can add role assignment conditions also
- ![alt text](image-135.png)
- ![alt text](image-136.png)
- We most commonly interact with storage account through web applications hosted on web servers.
- Storage Accounts store blobs which are great for storing music/video/images etc.
- To access storage account data, we have storage access keys.
- ![alt text](image-137.png)
- We can also rotate the keys
- For temporary access we use SAS tokens
- ![alt text](image-138.png)
- ![alt text](image-139.png)
- ![alt text](image-140.png)
- ![alt text](image-141.png)
- The signature part of the SAS token ensures that the parameters of the SAS token are not manipulated with.


### Stored Access Policies
- ![alt text](image-142.png)
- ![alt text](image-143.png)
- ![alt text](image-144.png)
- We can associate SAS tokens to the shared access policy
- ![alt text](image-145.png)
- We can edit the stored access policy also

### Storage Redundancy in Azure
- ![alt text](image-146.png)
- We have synchronous and asynchronous replication of data.
- ![alt text](image-147.png)
- Each region usually has 3 zones.
- ![alt text](image-148.png)
- ![alt text](image-149.png)
- ![alt text](image-150.png)
- ![alt text](image-151.png)
- ![alt text](image-152.png)
- ![alt text](image-153.png)
- ![alt text](image-154.png)
- ![alt text](image-155.png)

### Object Replication
- Here we can have data inside a storage account replicate to another storage account
- ![alt text](image-156.png)
- ![alt text](image-157.png)
- ![alt text](image-158.png)

### FileShare Storage
- Traditionally we would set up a file server which would follow the SMB protocol
- ![alt text](image-159.png)
- ![alt text](image-160.png)
- ![alt text](image-161.png)
- Premium File Shares are supported only with Premium Storage Accounts
- We also have ability of Soft Delete for FileShares
- ![alt text](image-162.png)
- ![alt text](image-163.png)
- Earlier port 445 used to be used by hackers a lot. So lot of ISP's block that port. For this purpose we may need to setup site to site or point to site VPN or ExpressRoute to tunnel traffic directly over port 445.
- ![alt text](image-164.png)

### Working with Blob Storage Management
- Blob storage is geared towards webservices.
- It support HTTPS, REST
- ![alt text](image-165.png)

### Blob Lifecycle Management
- ![alt text](image-166.png)
- ![alt text](image-167.png)
- ![alt text](image-168.png)
- ![alt text](image-169.png)
- ![alt text](image-170.png)
- Restoring from Archive tier can take more than 2 hours

### Relational Databases
- ![alt text](image-171.png)
- ![alt text](image-172.png)
- ![alt text](image-173.png)
- ![alt text](image-174.png)

### Service Tiers for Azure SQL
- ![alt text](image-175.png)


## Designing for Data Integration
- Creating an Azure VM with SQL as a relational data storage solution
- ![alt text](image-176.png)
- ![alt text](image-177.png)
- ![alt text](image-178.png)
- ![alt text](image-179.png)
- We can assign a DNS name to our SQL Server VM
- ![alt text](image-180.png)
- ![alt text](image-181.png)
- We can create an Azure SQL Database also
- ![alt text](image-182.png)
- ![alt text](image-183.png)
- ![alt text](image-184.png)
- ![alt text](image-185.png)
- ![alt text](image-186.png)

## Recommend a data storage solution
- Azure offers a choice of SQL and NoSQL databases
- ![alt text](image-187.png)
- ![alt text](image-188.png)
- ![alt text](image-189.png)
- ![alt text](image-190.png)
- ![alt text](image-191.png)
- ![alt text](image-192.png)
- ![alt text](image-193.png)
- ![alt text](image-194.png)
- ![alt text](image-195.png)
- ![alt text](image-196.png)


## Design a data storage solution for non-relational data
- ![alt text](image-197.png)
- ![alt text](image-198.png)
- ![alt text](image-199.png)
- ![alt text](image-200.png)
- ![alt text](image-201.png)
- ![alt text](image-202.png)
- ![alt text](image-203.png)
- ![alt text](image-204.png)

### Capacity Planning
- ![alt text](image-205.png)
- Provisioned throughput does support autoscaling

### Using Cosmos DB
- ![alt text](image-206.png)
- ![alt text](image-207.png)
- ![alt text](image-208.png)
- ![alt text](image-209.png)
- ![alt text](image-210.png)
- ![alt text](image-212.png)

### Data Lake Storage
- ![alt text](image-213.png)
- ![alt text](image-214.png)
- ![alt text](image-215.png)
- ![alt text](image-216.png)
- ![alt text](image-217.png)
- ![alt text](image-218.png)
- ![alt text](image-219.png)
- To create data lake storage, we need to select a premium storage account and must select Block Blobs
- ![alt text](image-220.png)
- This will enable us to enable a hierarchial namespace.
- Hierarchial namespace is required for data lakes storage
- ![alt text](image-221.png)

### Understanding Azure Databricks Storage
- ![alt text](image-222.png)
- ![alt text](image-223.png)
- ![alt text](image-224.png)
- ![alt text](image-225.png)
- ![alt text](image-226.png)

### Using Azure Synapse(Analytics System that integrates with Azure Datalakes and Azure Databricks)
- ![alt text](image-227.png)
- Azure Synapse can help us with Azure Machine Learning and Power BI and Intelligence.
- Synapse must be added as a resource provider in Azure
- ![alt text](image-228.png)
- ![alt text](image-229.png)
- We need to create a SQL database and server that can work with Azure Synapse.
- ![alt text](image-230.png)
- ![alt text](image-231.png)
- ![alt text](image-232.png)
- ![alt text](image-233.png)
- Synapse analytics requires a SQL pool.
- ![alt text](image-234.png)
- Azure Databricks: Primarily geared toward data preparation, big data processing, and machine learning model development. It excels in handling large-scale data with Apache Spark, building ETL pipelines, and managing the full ML lifecycle (using MLflow). It’s ideal for data engineers and data scientists focused on creating and deploying ML models, such as demand forecasting or anomaly detection in your supply chain use case.
- Azure Synapse Analytics: Geared toward end-to-end analytics, including data warehousing, visualization, and key insights. It combines Spark for big data processing with high-performance SQL pools for enterprise-grade querying and reporting, making it a strong choice for business intelligence (BI) and actionable insights via tools like Power BI. It’s better suited for scenarios where SQL-based analytics and dashboards are critical for decision-makers.
- Key Nuance:
- Databricks can support visualization (e.g., via notebooks or integration with BI tools), but it’s less optimized for enterprise data warehousing and SQL-heavy reporting compared to Synapse.
- Synapse can handle ML tasks (via Azure Machine Learning or Spark), but it’s not as streamlined for ML lifecycle management as Databricks.
- For your supply chain use case, choose Databricks if your focus is on building ML-driven solutions (e.g., predictive models) or Synapse if you need robust data warehousing and BI visualizations for stakeholders. You could also use both together: Databricks for data prep and ML, Synapse for storage and reporting.
- ![alt text](image-235.png)
- ![alt text](image-236.png)
- ![alt text](image-237.png)

### Understanding Azure Data Factory
- ![alt text](image-238.png)
- ![alt text](image-239.png)
- ![alt text](image-240.png)
- ![alt text](image-241.png)
- ![alt text](image-242.png)
- ![alt text](image-243.png)
- ![alt text](image-244.png)
- ![alt text](image-245.png)
- ![alt text](image-246.png)
- ![alt text](image-247.png)
- ![alt text](image-248.png)
- ![alt text](image-249.png)
- - ADF serves as the glue that connects and coordinates data flows between systems, including Azure Databricks and Azure Synapse Analytics. It ensures data is ingested, transformed, and delivered to the right platforms for processing, analysis, or visualization.
- Problem: Supply chain data resides in multiple sources (e.g., on-premises ERP systems like SAP, cloud-based CRMs like Salesforce, IoT devices, supplier APIs, or external data like weather APIs), making it hard to consolidate.
- Solution: ADF connects to a wide range of sources via built-in connectors (over 100+ supported data stores, including SQL Server, Oracle, REST APIs, and Azure services). It ingests raw data into a centralized storage like Azure Data Lake Storage, which can then be accessed by Databricks or Synapse.
- How It Helps: Automates the extraction of scattered data, ensuring a steady flow of fresh data for real-time or batch processing in your analytics pipeline.
- Developer Task: Create ADF pipelines using the drag-and-drop UI in ADF Studio to connect to sources, schedule data ingestion, and copy data to Azure Data Lake.
- Problem: Preparing data for analysis or ML requires complex transformations (e.g., cleaning, aggregating, joining sales and inventory data), which must be coordinated across tools.
- Solution: ADF orchestrates ETL (Extract-Transform-Load) or ELT (Extract-Load-Transform) workflows. It triggers data transformations in Databricks (e.g., using Spark notebooks for ML prep) or Synapse (e.g., using Data Flows or SQL scripts) and loads the processed data into target systems (e.g., Synapse SQL pools for reporting).
- How It Helps: Ensures seamless data movement and transformation across your analytics stack, reducing manual effort and errors.
- Developer Task: Use ADF’s Mapping Data Flows for lightweight transformations or trigger Databricks notebooks/Synapse pipelines within ADF workflows. Define dependencies and schedules to automate the process.
- Role in the Pipeline: ADF is the orchestrator that feeds data into Databricks and Synapse, triggers their processing jobs, and moves results to downstream systems. It doesn’t perform heavy data processing or analytics itself but coordinates the workflow.
- With Databricks: ADF ingests raw data into Azure Data Lake, triggers Databricks notebooks for data prep or ML model training (e.g., demand forecasting), and moves processed data (e.g., Delta Lake tables) to Synapse or other stores.
- With Synapse: ADF is embedded in Synapse Studio, allowing seamless orchestration of Synapse’s Data Flows, SQL scripts, or Spark jobs. It also loads processed data into Synapse’s SQL pools for BI reporting or Power BI dashboards.
- Example Workflow:
- ADF ingests sales, inventory, and supplier data into Azure Data Lake.
- ADF triggers a Databricks notebook to preprocess data and train an ML model for demand forecasting.
- ADF moves the processed data and model predictions to Synapse’s SQL pool.
- Synapse generates reports, and ADF triggers Power BI refresh for stakeholder dashboards.

### Using Azure Data Factory for copying data into Azure Synapse Analytics
- ![alt text](image-250.png)
- ![alt text](image-251.png)
- ![alt text](image-252.png)
- ![alt text](image-253.png)
- ![alt text](image-254.png)
- ![alt text](image-255.png)
- ![alt text](image-256.png)
- ![alt text](image-257.png)
- ![alt text](image-258.png)

## Design a solution for backup and disaster recovery
- ![alt text](image-260.png)

### Using Recovery Services Vault
- ![alt text](image-261.png)
- It has 2 main sections: Backup and Site Recovery
- ![alt text](image-262.png)
- ![alt text](image-263.png)
- ![alt text](image-264.png)
- In Azure Site Recovery, we can setup VM replication

### Backup policies for RTO and RPO
- ![alt text](image-265.png)
- We can create our custom backup policies
- ![alt text](image-266.png)
- ![alt text](image-267.png)

### Implementing Azure Backup for storage and compute resources
- There are 2 ways of doing backups: snapshots and backup
- ![alt text](image-268.png)
- ![alt text](image-269.png)
- We have more options in Recovery Services Vault
- ![alt text](image-270.png)
- ![alt text](image-271.png)
- ![alt text](image-272.png)
- For VMs we can backup like this
- ![alt text](image-273.png)
- ![alt text](image-274.png)
- We can view the backup logs like this
- ![alt text](image-275.png)
- ![alt text](image-276.png)
- ![alt text](image-277.png)
- We can also view the backup jobs like this
- ![alt text](image-278.png)
- Similarly we can look at Site Recovery Jobs


## Design for High Availability
- We can make use of availability zones
- Each availability zone has its own power, networking and cooling
- Availability zones have very fast replication
- Synchronous replication is possible
- ![alt text](image-279.png)
- ![alt text](image-280.png)
- Availability zones protect us from data center outage not from regional outage

### Azure Site Recovery
- ![alt text](image-281.png)
- ![alt text](image-282.png)
- ![alt text](image-283.png)
- ![alt text](image-284.png)
- ![alt text](image-285.png)
- ![alt text](image-286.png)
- ![alt text](image-287.png)
- ![alt text](image-288.png)
- ![alt text](image-289.png)
- We can create recovery plans inside azure site recovery
- ![alt text](image-290.png)
- ![alt text](image-291.png)
- ![alt text](image-292.png)
- One example of recovery plan is like this
- ![alt text](image-293.png)
- ![alt text](image-294.png)
- We can enable replication of VMs
- ![alt text](image-295.png)
- ![alt text](image-296.png)
- ![alt text](image-297.png)
- ![alt text](image-298.png)
- ![alt text](image-299.png)

### Replicating Data Storage to provide high availability
- We have option of object replication to replicate data between storage accounts
- ![alt text](image-300.png)
- ![alt text](image-301.png)
- ![alt text](image-302.png)

## Design compute solutions
