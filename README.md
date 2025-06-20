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
  