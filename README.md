
# Microsoft Exchange-Server-2019

<img width="800" alt="Drawing5" src="https://user-images.githubusercontent.com/86381942/212575902-7ce17e25-3f77-4811-a42e-ba7ed285b87c.png">



</head>
  <body>
    <h1>Project Journey</h1>
    <nav>
      <ul>
        <li><a href="#introduction">Introduction</a></li>
        <li><a href="https://github.com/MrAAGO/Exchange-server-2019-Installation-and-configuration">Installation and Configuration</a></li>
        <li><a href="#mailbox">Create User Mailbox</a></li>
         <li><a href="#database">Rename and Move a Mailbox Database</a></li>
        <li><a href="#databasenew">Create a New Mailbox Database</a></li>
        <li><a href="#resource">Create Resource Mailboxes</a></li>
        <li><a href="#distribution">Create Distribution Group</a></li>
        <li><a href="#dynamic">Create Dynamic Distribution Group</a></li>
        <li><a href="#shared">Create a Shared Mailbox </a></li>
        <li><a href="#policy">Create a Email Address Policy </a></li>
        <li><a href="#domain">Configure Accepted Domain </a></li>
        <li><a href="#address"> Create Custom Address List </a></li>
        <li><a href="#custom"> Create Custom Global Address List </a></li>
        <li><a href="#offline"> Create Offline Address Book </a></li>
        <li><a href="#url"> Configure Internal and External URLs</a></li>
        <li><a href="#pop3"> Configure POP3 Services</li>
        <li><a href="#outlook">Configure Outlook Anywhere</li>
        <li><a href="#restrict">Configure Message Delivery Restrictions for a Mailbox></li>
        <li><a href="#attach">How to Increase File Attachment Size</li>
         <li><a href="#offaccess">Enable Offline Access in Outlook</li>  
         <li><a href="#emailfor">Configure Email Forwarding</li>  
         <li><a href="#mailtip">Configure Custom MailTips for Recipients</li> 
         <li><a href="#quota">Configure Storage Quota for a Mailbox</li>   
         <li><a href="#limit">Configure Mailbox Database Limits</li>    
      </ul>
    </nav>
    <section id="introduction">
      <h2>Introduction</h2>
      <p>Microsoft Exchange Server 2019 is a popular email and calendar server software from Microsoft. It provides a host of features that make it an ideal choice for businesses of all sizes.

One of the key features of Exchange Server 2019 is its scalability. It is designed to handle large amounts of email and calendar data, making it a great option for businesses with a high volume of email traffic.

Another important feature of Exchange Server 2019 is its security. It includes built-in protection against spam and malware, as well as advanced security features like data loss prevention and multi-factor authentication.

Exchange Server 2019 also offers robust calendar and scheduling capabilities. Businesses can easily schedule meetings and appointments, and share calendars with colleagues and clients.

In addition to these features, Exchange Server 2019 also offers a number of other capabilities such as support for mobile devices, integration with other Microsoft products like SharePoint and Skype for Business, and support for various mail clients like Outlook, Apple Mail, etc.

Overall, Microsoft Exchange Server 2019 is a powerful and versatile email and calendar server software that can meet the needs of businesses of all sizes. With its scalability, security, and robust calendar and scheduling capabilities, it is an excellent choice for businesses that rely heavily on email and calendar functionality .</p>

<p><b>In This project i am going to Configure several key settings of Microsoft Exchange Server

  
<li>Network Configuration: This includes configuring the server's IP address, DNS settings, and domain name.</li>

<li>Mailbox Database Configuration: This includes creating and configuring mailbox databases, as well as setting up mailbox storage quotas.</li>

<li>Transport Configuration: This includes configuring the server's message routing and transport settings, such as setting up connectors and transport rules.</li>

<li>Anti-Spam and Anti-Malware Configuration: This includes configuring the server's built-in spam and malware protection, as well as setting up additional security measures like data loss prevention and multi-factor authentication.</li>

<li>Client Access Configuration: This includes configuring the server's client access settings, such as setting up Outlook Web Access and Exchange ActiveSync.</li>

<li>High Availability Configuration: This includes configuring the server's high availability features, such as setting up database availability groups and load balancing.</li>

<li>Backup and Disaster Recovery Configuration: This includes configuring the server's backup and disaster recovery settings, such as setting up backup schedules and creating recovery plans.</li>

<li>Monitoring and Reporting Configuration: This includes configuring the server's monitoring and reporting settings, such as setting up performance counters and creating custom reports...</p></b>
    </section>
    
 <section id="mailbox">
      <h2>Create Users Mailbox</h2>
  
  <p>
  A user mailbox in Exchange Server is a mailbox that is associated with a specific user. It is the primary mailbox for an individual user and is used to store and manage their email messages, calendar items, contacts, tasks, and other data. A user mailbox is created when a new user is added to an organization's Exchange Server and is typically accessed through a client such as Outlook or Outlook Web Access (OWA).
  
To create a user mailbox in Exchange Server 2019, you can use the Exchange Management Shell (EMS) to run the following command:

  ![carbon](https://user-images.githubusercontent.com/86381942/212557957-f7f20266-70fe-471d-bb6d-b96a833ca51c.png)

  This command creates a new mailbox for a user named John Smith, with the alias "jsmith" and the email address "jsmith@example.com". The user's first name is "John" and last name is "Smith". The password for the mailbox is "Pa$$w0rd", which is passed as a secure string. The mailbox is created on the database "Mailbox Database".</p>
 
  You can also use the Exchange Admin Center (EAC) in the GUI to create a mailbox:
 
  <li>Log in to the EAC.</li>
  
  <li>Go to recipients>mailboxes.</li>
  
   <li>Click the + button.</li>

   <li>Select user mailbox.</li>
        
   <li>Fill out the form with the required information, including the user's name, email address, and password.</li>
    
 <li>Select the mailbox database where you want to create the mailbox..</li
    
 <li>Click save</li>

![3](https://user-images.githubusercontent.com/86381942/212559581-7a0d188d-5583-48a5-8521-dd2fb65695db.png)


<li>You can also create Mailbox Through Existing Users ,just browse and save the new users mailbox.</li>
  
  ![2](https://user-images.githubusercontent.com/86381942/212558906-2cb5a7f1-92c4-4698-adfb-b5ed56ed196c.png)

<section id="database">
      <h2>Rename and Move a Mailbox Database</h2>
  
  <b>To rename and move a mailbox database in Exchange Server 2019, you can use the Exchange Management Shell (EMS) to perform the following steps:</b>

<li>Rename the mailbox database: Use the following command to rename the mailbox database:</li>
  
`Rename-MailboxDatabase -Identity "OldName" -NewName "NewName"`
  
<li>Move the mailbox database: Use the following command to move the mailbox database to a new location::</li>

`Move-MailboxDatabase -Identity "NewName" -EdbFilePath "D:\NewLocation\NewName.edb`
 
  You need to change the path of the edb file to the location you want to move the mailbox database to.

<li>You need to change the path of the edb file to the location you want to move the mailbox database to.

Mount the mailbox database: Use the following command to mount the mailbox database in its new location:</li>
`Mount-Database "NewName`

 It's important to note that you should schedule a maintenance window and make sure that there are no active users on the mailbox database when you are renaming and moving it, and also that you should have the necessary permissions to perform this task.

You can also use the Exchange Admin Center (EAC) in the GUI to rename and move a mailbox database:

  <li>Go to servers, then databases</li>
<li>Select the database you want to move and click on more</li>
<li>then choose move database path.</li>
<li>Fill out the form with the new path</li>
<li>Click on move</li>
<li>You should also be logged in as a member of the Organization Management role group or the Recipient Management role group to perform this task.</li>
 
  ![4](https://user-images.githubusercontent.com/86381942/212560490-e47e6064-959b-4a0c-b868-9051745d31ea.png)

<section id="databasenew">
      <h2>Create a New Mailbox Database in Exchange 2019</h2>
<b>To create a new mailbox database in Exchange Server 2019, you can use the Exchange Management Shell (EMS) to run the following command:</b>
  
![carbon (1)](https://user-images.githubusercontent.com/86381942/212561080-864bb6b6-8af9-44e9-9867-6db838cfdb61.png)
 
  `New-MailboxDatabase -Name "NewMailboxDatabase" -Server "ServerName" -EdbFilePath "D:\MailboxDatabases\NewMailboxDatabase.edb" -LogFolderPath "D:\MailboxDatabases\NewMailboxDatabase`
  
  This command creates a new mailbox database named "NewMailboxDatabase" on the server "ServerName". The mailbox database's .edb file is stored in the "D:\MailboxDatabases" folder and the log files are stored in the "D:\MailboxDatabases\NewMailboxDatabase" folder.

You can also use the Exchange Admin Center (EAC) in the GUI to create a new mailbox database:

  <li>Go to servers, then databases</li>
  
<li>Click the + button.</li>
  
<li>Fill out the form with the required information, including the name of the new mailbox database, the server it will be located on, and the path for the .edb file and the log files.</li>
  
<li>Click save.</li>
  
It's important to note that you should schedule a maintenance window and make sure that there are no active users on the mailbox database when you are creating it, and also that you should have the necessary permissions to perform this task.
You should also be logged in as a member of the Organization Management role group or the Recipient Management role group to perform this task.

You can also specify other parameters such as the maximum size of the database, the retention policy, the mailbox database replication, and more.

It's also worth noting that the folder path for the edb and log files should exist before the creation of the mailbox database, and that the folder should have the proper permission to the service account running the mailbox role.
  
  ![5](https://user-images.githubusercontent.com/86381942/212561516-fdbf7af6-882f-4d07-9af0-32c84ec48dd4.png)
  
<section id="resource">
      <h2>Create Resource Mailboxes in Exchange 2019</h2> 
  Resource mailboxes in Exchange Server 2019 are used to manage and schedule resources such as conference rooms, equipment, or other shared resources. Here are the steps to create a resource mailbox in Exchange Server 2019:

<li><b>Open the Exchange Management Shell: Open the Exchange Management Shell on the Exchange server.</li></b>

<li><b>Create the resource mailbox: Use the following command to create the resource mailbox:</li></b>

  `New-Mailbox -Name ConfRoom1 -DisplayName "Conference Room 1" -Room`
  
 This command creates a new resource mailbox named "Conference Room 1" with the alias "confroom1" and the email address "confroom1@example.com". -Room switch specifies that it is a room mailbox.
  
<li><b>Specify the resource capacity: Use the following command to set the capacity of the conference room:</li></b>
  
`Set-CalendarProcessing -Identity "confroomA" -ResourceCapacity 10`
  
This command sets the capacity of the conference room to 10, meaning that it can accommodate up to 10 people.
  
<li><b>Add additional settings: Use the following command to add additional settings to the resource mailbox, such as the booking window, the automatic reply message, and more:</li></b>

  `Set-CalendarProcessing -Identity "confroomA" -AddOrganizerToSubject $True -AllowConflicts $False -DeleteComments $True`
  
 You can also use the Exchange Admin Center (EAC) in the GUI to create a resource mailbox:

<li>Go to recipients > resources.</li>
<li>Click the + button.</li>
<li>Select room mailbox</li>
<li>Fill out the form with the required information, including the name of the new resource mailbox and its email address.</li>
<li>Select the calendar processing tab and set the resource capacity and other settings.</li>
<li>Click save.</li>
It's important to note that you should have the necessary permissions to perform this task and also that you should be logged in as a member of the Organization Management role group or the Recipient Management role group.

You can also manage and schedule resource mailboxes through the Outlook client or Outlook Web Access (OWA) by users with the correct permissions. 
  
![6](https://user-images.githubusercontent.com/86381942/212562255-4e31fc34-c04e-4e72-872d-6ed83f13e8ac.png)

![7](https://user-images.githubusercontent.com/86381942/212562259-38ed7b8c-287f-40c2-b710-f1a7b5e4a60c.png)

<section id="distribution">
      <h2>Create Distribution Group in Exchange 2019</h2>
      
A distribution group, also known as a distribution list, is a feature in Exchange Server that allows you to send an email to a group of people without having to add each recipient individually.

Distribution groups are used to create email addresses that represent a group of people, such as a department, project team, or group of external partners. Once the distribution group is created, you can add members to it, and then use the group's email address to send emails to all members of the group at once  

**There are two types of Distribution groups**

Distribution Group: This group is used for sending emails to the group members and it doesn't have a mailbox.
  
Mail-Enabled Distribution Group: This group is used for sending emails to the group members and it also has a mailbox.

To create a distribution group in Exchange 2019 using PowerShell, you can use the New-DistributionGroup cmdlet. Here are the steps:

<li>Open the Exchange Management Shell on your Exchange Server.
<li>Type the following command to create a new distribution group:

```powershell
New-DistributionGroup -Name "Marketing Team" -Type "Distribution" -PrimarySmtpAddress "marketing@yourdomain.com" -OrganizationalUnit "OU=Marketing,DC=yourdomain,DC=com"
```
![8](https://user-images.githubusercontent.com/86381942/212593061-db39c7e4-4891-459b-abd5-2733631f71c3.png)

![9](https://user-images.githubusercontent.com/86381942/212593154-b1afb2c6-f45d-4314-8b24-86aef348e60b.png)

  
This will create the distribution group "Marketing Team" in the "Marketing" OU. If the specified OU does not exist, the cmdlet will throw an error.

You can also use the -OrganizationalUnit parameter to move an existing distribution group to a different OU by using the Move-DistributionGroup cmdlet
  
```powershell
  Move-DistributionGroup -Identity "Marketing Team" -OrganizationalUnit "OU=NewMarketing,DC=yourdomain,DC=com"
```
This will move the "Marketing Team" distribution group to the "NewMarketing" OU.
  
 While creating a distribution group using the New-DistributionGroup cmdlet in PowerShell, you can specify additional properties such as -OrganizationalUnit, -ManagedBy, -DisplayName, -Notes, etc.

-OrganizationalUnit: Specifies the OU where the distribution group should be created.
-ManagedBy: Specifies the user or group that will manage the distribution group.
-DisplayName: Specifies a display name for the distribution group.
-Notes: Specifies notes or comments about the distribution group.

Here is an example of how to create a distribution group with additional properties: 
  
```powershell
  New-DistributionGroup -Name "Marketing Team" -Type "Distribution" -PrimarySmtpAddress "marketing@yourdomain.com" -OrganizationalUnit "OU=Marketing,DC=yourdomain,DC=com" -ManagedBy "JohnDoe" -DisplayName "Marketing Department" -Notes "This is the Marketing Team distribution group"
```
This will create a distribution group called "Marketing Team" with the email address "marketing@yourdomain.com", located in the "Marketing" OU, managed by user "JohnDoe", with a display name of "Marketing Department" and a note of "This is the Marketing Team distribution group".
Please note that some of the properties may not be editable after the group has been created.
  
##**Managing a Distribution Group with powershell**##
**PowerShell to manage distribution groups in Exchange 2019. Here are some examples of how to perform common management tasks:**

  - Adding members to a group:
 ```powershell
  Add-DistributionGroupMember -Identity "GroupName" -Member "User1","User2"
```
  - Removing members from a group:
  ```powershell
  Remove-DistributionGroupMember -Identity "GroupName" -Member "User1","User2"
```
- Modifying Group properties:
```powershell
  Set-DistributionGroup -Identity "GroupName" -PropertyName "PropertyValue"
```
For example: 
```powershell
  Set-DistributionGroup -Identity "Marketing Team" -DisplayName "Marketing Department" -Notes "This is the Marketing Team distribution group"
```
-Deleting a group
```powershell
Remove-DistributionGroup -Identity "GroupName"
  ```
- Listing the members of a group
```powershell
Get-DistributionGroupMember -Identity "GroupName"
  ```
  
-Listing all Distribution groups
```powershell
Get-DistributionGroup
  ```
- Moving Distribution group to different organizational unit
```powershell
Move-DistributionGroup -Identity "GroupName" -OrganizationalUnit "OU=NewMarketing,DC=yourdomain,DC=com"  
```
##**Creating a Distribution Group**##
  
Using the Exchange Admin Center (EAC):

- Log in to the EAC.
- Navigate to recipients > groups.
- Click the plus icon to create a new group.
- Fill in the required information, such as the group name, email address, and membership.
- Click save.
  
  ![10](https://user-images.githubusercontent.com/86381942/212593915-295e410f-f73c-46ab-b5e3-bd1800a3109f.png)

  <section id="dynamic">
      <h2>Dynamic Distribution Group in Exchange Server</h2>
  
    A Dynamic Distribution Group in Exchange Server is a type of distribution group that automatically includes members based on specific criteria, rather than having to manually add or remove members.

Dynamic Distribution Groups are created using the Exchange Management Shell (EMS) and are based on a query that is run against Active Directory to determine group membership. This query can include criteria such as organizational unit, department, office, and other attributes. The group membership is automatically updated when changes to Active Directory are made, such as when a new user is created or an existing user's attributes are modified.
    
![12](https://user-images.githubusercontent.com/86381942/212610029-e286fcc5-dbd4-45b1-addf-e5fb32315244.png)

    

   `New-DynamicDistributionGroup -Name "HR Team" -OrganizationalUnit "OU=HR,OU=Employes,DC=yourdomain,DC=com" -RecipientFilter {((Department -eq "HR") -and (RecipientType -eq 'UserMailbox'))}`

   
    This command creates a dynamic distribution group called "HR Team" that includes all users in the "HR" OU. 



  - You can use the Set-DynamicDistributionGroup cmdlet in PowerShell to add a designated manager to an existing dynamic distribution group.
    

    `Set-DynamicDistributionGroup -Identity "HR Team" -ManagedBy "JohnDoe"` 

  
   
    - You can also use the -ManagedBy parameter to add multiple managers to the dynamic distribution group.  
   

    `Set-DynamicDistributionGroup -Identity "HR Team" -ManagedBy "JohnDoe","JaneDoe"`

    
   
    - You can use the Get-DynamicDistributionGroup cmdlet in PowerShell to view the properties of an existing dynamic distribution group in Exchange Server.
   

    `Get-DynamicDistributionGroup -Identity "HR Team"`

  
    - You can also use the -Identity parameter to specify multiple dynamic distribution groups, separated by a comma.
    

    `Get-DynamicDistributionGroup -Identity "HR Team","Marketing Team"`

 
    - Removing a dynamic distribution group:
    
    `Remove-DynamicDistributionGroup -Identity "Marketing Team"`

   
    - Listing the members of a dynamic distribution group:
    
   `Get-DynamicDistributionGroup -Identity "Marketing Team" | Get-Recipient | Select-Object -ExpandProperty PrimarySmtpAddress` 

 - Here is an example of how to create a dynamic distribution group that includes all users in the "Marketing" OU, with a designated owner, and a membership rule that excludes disabled user accounts:
    
   `New-DynamicDistributionGroup -Name "Marketing Team" -OrganizationalUnit "OU=Marketing,DC=yourdomain,DC=com" -ManagedBy "JohnDoe" -RecipientFilter {((OrganizationalUnit -eq "OU=Marketing,DC=yourdomain,DC=com") -and (RecipientType -eq 'UserMailbox') -and (Enabled -eq $True))}`


    - You can also use other attributes to filter the dynamic distribution group, like the department, the title, the location, the company, etc.
    

 `New-DynamicDistributionGroup -Name "Marketing Team" -OrganizationalUnit "OU=Marketing,DC=yourdomain,DC=com" -ManagedBy "JohnDoe" -RecipientFilter {((OrganizationalUnit -eq "OU=Marketing,DC=yourdomain,DC=com") -and (Department -eq "Marketing") -and (RecipientType -eq 'UserMailbox') -and (Enabled -eq $True))}`

 
    - This command creates a dynamic distribution group called "Marketing Team" that includes all enabled users in the "Marketing" department and in the "Marketing" OU, with "JohnDoe" as the designated owner.   
    
  - You can also use the -Notes parameter to add a note to the distribution group.
    
   
    `New-DynamicDistributionGroup -Name "Marketing Team" -OrganizationalUnit "OU=Marketing,DC=yourdomain,DC=com" -ManagedBy "JohnDoe" -RecipientFilter {((OrganizationalUnit -eq "OU=Marketing,DC=yourdomain,DC=com") -and (Department -eq "Marketing") -and (RecipientType -eq 'UserMailbox') -and (Enabled -eq $True))} -Notes "Marketing Team distribution group` 
   

    *Create a dynamic distribution group in ECP**   
- Log in to the ECP using your administrator credentials.

- In the ECP, navigate to the Recipients section and click on the Distribution Groups tab.

- Click on the + (Plus) sign button to create a new distribution group.

- Select Dynamic Distribution Group from the list of group types.

- Enter a name for the group, and a display name and email address for the group.

- In the Recipient filter section, you can define the criteria that will be used to determine group membership, you can use the + (Plus) sign button to add new filters.

- In the Managed by section, you can specify the manager of the group.

- Click on save to create the dynamic distribution group.    
    
    ![11](https://user-images.githubusercontent.com/86381942/212609696-9a0b1872-9122-401f-b8cc-1880f568c614.png)

  <section id="shared">
      <h2>Create a Shared Mailbox </h2>
      
     A shared mailbox in Exchange Server is a mailbox that multiple users can access and use to send and receive email. Shared mailboxes are typically used for shared email accounts such as info@, support@, or sales@. Shared mailboxes allow teams to collaborate and manage shared email accounts without having to share login credentials or access to personal email accounts. They can also be used to store emails that are sent to a specific department or team, allowing multiple people to view and respond to them. Shared mailboxes can be accessed via Outlook, OWA (Outlook Web App), or other email clients that support the use of shared mailboxes
 
 - To create a shared mailbox in Exchange 2019 using PowerShell, you will need to use the Exchange Management Shell (EMS). Here are the steps:

- Open the Exchange Management Shell (EMS) on the Exchange server.

- Use the following command to create the shared mailbox:

```powershell
New-Mailbox -Shared -Name "Shared Mailbox Name" -DisplayName "Shared Mailbox Display Name" -Alias "sharedalias"
```
- Note: Replace "Shared Mailbox Name" and "Shared Mailbox Display Name" with the desired name and display name for the shared mailbox and "sharedalias" with the desired email address

![14](https://user-images.githubusercontent.com/86381942/212821835-a2143a0a-6a1a-4e6b-8436-16bbf23b83f1.png)

- Use the following command to give permissions to specific user or group to access the shared mailbox:

```powershell
Add-MailboxPermission -Identity "sharedalias" -User "user1" -AccessRights FullAccess
```
- Note: Replace "user1" with the user or group you want to give access to the shared mailbox.

![16](https://user-images.githubusercontent.com/86381942/212821968-9aab46ab-2903-49e9-b725-a29d9ddc6418.png)

- Use the following command to set a password for the shared mailbox:

```powershell
Set-Mailbox -Identity "sharedalias" -Password (ConvertTo-SecureString "password" -AsPlainText -Force)
```
- Once the mailbox is created, users with the appropriate permissions will be able to access it in Outlook or OWA (Outlook Web App).

**To create a shared mailbox from EAC, follow these steps**

- Open the Exchange Admin Center (EAC) by navigating to https://<your-server-name>/ecp.

- In the EAC, navigate to Recipients > Shared.

- Click the "+" button to create a new shared mailbox.

- Enter a name and email address for the shared mailbox and click "Save".

- Assign permissions to the mailbox by clicking the "Permissions" tab and adding users or groups as necessary.

- Once the mailbox is created, users with the appropriate permissions will be able to access it in Outlook or OWA (Outlook Web App).

![15](https://user-images.githubusercontent.com/86381942/212822232-88d3a80c-b729-45e5-8e5b-5d94bb92dceb.png)


<section id="policy">
      <h2>Create a Email Address Policy</h2>
  
An email address policy in Exchange Server is a set of rules that automatically assigns email addresses to recipients, such as users and groups, based on specific conditions. These policies can be used to add prefixes, suffixes, or custom domains to email addresses, making it easier to identify the recipient's department, group, or location. Email address policies can also be used to ensure that all email addresses follow a specific format and meet compliance requirements. Once an email address policy is configured, it will automatically apply to all new and existing recipients that meet the specified conditions. This means that administrators don't need to manually update email addresses for each recipient. Email address policies can be managed and configured using the Exchange Management Shell (EMS) or the Exchange Admin Center (EAC).
  
  **To create an email address policy from the Exchange Admin Center (EAC) in Exchange 2019, follow these steps:**

- Open the Exchange Admin Center (EAC) by navigating to https://<your-server-name>/ecp.

- In the EAC, navigate to Mail Flow > Email address policies.

- Click the "+" button to create a new email address policy.

- Fill in the following fields:

- Name: Enter a name for the email address policy
- Included recipients: Select the recipients that this policy will apply to. (Users, Groups, All, etc)
- Apply this policy: Select the conditions that will trigger the policy to apply, such as a specific department or group.
- Email address format: Select the format of the email address that the policy will assign.
- Email address: Type the email address format that you want to use.
- Click Save to create the email address policy.

- To apply the email address policy, select the policy and click the "Apply" button

- To verify that the policy was applied, navigate to Recipients > Mailboxes and check the email addresses of the users that the policy should have applied to.

![17](https://user-images.githubusercontent.com/86381942/212825556-b799333a-6848-4ed0-8eaa-137b8b73f5f2.png)

  **To configure an email address policy in Exchange 2019, you will need to use the Exchange Management Shell (EMS). Here are the steps**

-Open the Exchange Management Shell (EMS) on the Exchange server.

-Use the following command to create a new email address policy:

  - To create an email address policy that adds a prefix to all email addresses in a specific department:
  
  ```powershell
  New-EmailAddressPolicy -Name "Department Prefix Policy" -IncludedRecipients AllRecipients -ConditionalCustomAttribute1 "Department -eq 'Marketing'" -EnabledEmailAddressTemplates "SMTP:marketing-%g@domain.com"
```
  
 - To create an email address policy that adds a suffix to all email addresses for external recipients:
  
   ```powershell
  New-EmailAddressPolicy -Name "External Suffix Policy" -IncludedRecipients ExternalRecipients -EnabledEmailAddressTemplates "SMTP:%m@domain.com-external"
```
  
  - To create an email address policy that adds a domain name to all email addresses for a specific group:

  ```powershell
  New-EmailAddressPolicy -Name "Group Domain Policy" -IncludedRecipients AllRecipients -ConditionalCustomAttribute1 "Group -eq 'Accounting'" -EnabledEmailAddressTemplates "SMTP:%m@accounting.com"
  ```
  
  - To create an email address policy that adds a custom address to all email addresses for a specific mailbox:
  
  ```powershell
  New-EmailAddressPolicy -Name "Custom Address Policy" -IncludedRecipients AllRecipients -ConditionalCustomAttribute1 "Mailbox -eq 'JohnDoe'" -EnabledEmailAddressTemplates "SMTP:johndoe@custom.com"
```
  
  - New email address policy
  
  ```powershell
  New-EmailAddressPolicy -Name "Policy Name" -IncludedRecipients AllRecipients -ConditionalCustomAttribute1 "condition" -EnabledEmailAddressTemplates "SMTP:%m@domain.com"
```
  Note: Replace "Policy Name" with the desired name for the policy, "condition" with the condition that will trigger the policy to apply (such as a specific department or group), and "domain.com" with your domain name.
  
  - Use the following command to apply the policy:
  
  ```powershell
  Update-EmailAddressPolicy -Identity "Policy Name"
```
  - Note: Replace "Policy Name" with the name of the policy you just created.
  
  - You can also use the following command to verify the policy you've created:
  
  ```powershell
  Get-EmailAddressPolicy | Format-List
```
  
  - To create an email address policy for specific users
  
  ```powershell
  New-EmailAddressPolicy -Name "Specific Users Policy" -IncludedRecipients MailboxUsers -ConditionalCustomAttribute1 "Name -eq 'User1' -or Name -eq 'User2'" -EnabledEmailAddressTemplates "SMTP:%g.%s@domain.com"
```
 - Replace "User1" and "User2" with the specific user or users you want this policy to apply to, and "domain.com" with your domain name.
  
  - Use the following command to apply the policy:
  
  ```powershell
  Update-EmailAddressPolicy -Identity "Specific Users Policy"
```
  
  - To verify that the policy was applied to specific users, use the following command:
  
  ```powershell
  Get-Recipient -Filter {EmailAddresses -like "*"} | Where-Object {$_.EmailAddresses -like "SMTP:*domain.com"} | Format-List Name,EmailAddresses
```
  **Once the email address policy is configured, it will automatically apply to all new and existing recipients that meet the specified conditions, in this case, the policy will apply only to User1 and User2**
  
 <section id="domain">
      <h2>Configure Accepted Domain in Exchange 2019</h2> 
   
Accepted domains in Exchange 2019 are the domains for which the Exchange server will accept and deliver email. They specify which email addresses the server will recognize as valid and which it will reject. An accepted domain can be set as an authoritative domain, meaning the Exchange server is the final destination for email sent to that domain, or an internal relay domain, meaning the email will be forwarded to another email server. Accepted domains are typically set for the primary domain of an organization and any additional domains that the organization wants to receive email for. They can be managed and configured using the Exchange Management Shell (EMS) or the Exchange Admin Center (EAC) and it's a crucial part of the mail flow configuration in Exchange Server.
   
  - To configure an accepted domain in Exchange 2019, you will need to use the Exchange Management Shell (EMS). Here are the steps:

- Open the Exchange Management Shell (EMS) on the Exchange server.

- Use the following command to create a new accepted domain: 
   
   `New-AcceptedDomain -Name "domain.com" -DomainName "domain.com" -DomainType "Authoritative"`

  
   <b>Note: Replace "domain.com" with the domain name that you want to create as an accepted domain</b>
   
   - To set the new accepted domain as the default domain, use the following command:
   
   `Set-AcceptedDomain -Identity "domain.com" -IsDefault $true`

   - To verify the accepted domains configured on your Exchange organization, you can use the following command
   
   `Get-AcceptedDomain`
   
   ![18](https://user-images.githubusercontent.com/86381942/212829873-b8c15254-736c-445b-ac22-60aa5c0a1e2a.png)
   
   **Configure Accepted Domain in Exchange 2019 from EAC**
   
 - To configure an accepted domain in Exchange 2019 from the Exchange Admin Center (EAC), follow these steps:

- Open the Exchange Admin Center (EAC) by navigating to https://<your-server-name>/ecp.

- In the EAC, navigate to Mail Flow > Accepted domains.

- Click the "+" button to create a new accepted domain.

- Fill in the following fields:

        - Name: Enter a name for the accepted domain
        - Domain name: Type the domain name that you want to create as an accepted domain.
        - Accepted domain type: Select whether the domain is Authoritative or Internal relay.
   
 - Click Save to create the accepted domain.

- To set the new accepted domain as the default domain, select the domain and click the "Set as default" button

- To verify the accepted domains configured on your Exchange organization, navigate to Mail Flow > Accepted domains, you should see the domain you've just created
   
   ![19](https://user-images.githubusercontent.com/86381942/212830288-6ac964fb-b31c-45e3-bebc-1f99b0e54858.png)

   
<section id="address">
      <h2>Create Custom Address List in Exchange 2019 </h2>
      
A Custom Address List in Exchange 2019 is a collection of email addresses and contact information that is filtered and organized based on specific criteria, such as recipient type, custom attributes, and more. Custom address lists can be created and managed using the Exchange Management Shell (EMS) or the Exchange Admin Center (EAC) and it's a way to organize recipients in your organization for specific scenarios, for example, you can create an address list for all recipients in a specific department or location, or all recipients with a specific custom attribute. Custom address lists are used to make it easier to send email to a group of people, and they can be used in email clients such as Outlook and OWA (Outlook Web App) that support the use of custom address lists.
    
  <b>To create a custom address list in Exchange 2019, you will need to use the Exchange Management Shell (EMS). Here are the steps:</b>

- Open the Exchange Management Shell (EMS) on the Exchange server.

- Use the following command to create a new address list:

`New-AddressList -Name "Address List Name" -RecipientFilter {((RecipientType -eq 'UserMailbox') -and (CustomAttribute1 -eq 'value'))}`


**Note: Replace "Address List Name" with the desired name for the address list and "value" with the value of the custom attribute that will be used to filter the recipients in the address list.**

- Use the following command to update the offline address book (OAB) to include the new address list:

```powershell
Update-OfflineAddressBook -Identity "Default Offline Address Book"
```

- To verify that the custom address list was created, use the following command:

```powershell
Get-AddressList | Format-List Name
```

  <h3><b>Example</b></h3> 
  
- Create an address list for all recipients in the "Marketing" department, you would specify "Marketing" as the value in the recipient filter:

```powershell
New-AddressList -Name "Marketing Department" -RecipientFilter {((RecipientType -eq 'UserMailbox') -and (Department -eq 'Marketing'))}
```
![22](https://user-images.githubusercontent.com/86381942/212835823-37210c34-de06-45e7-aba8-3906a275493e.png)

- if you want to create an address list for all recipients that have a custom attribute named "Region" with the value "West", you would specify "West" as the value in the recipient filter:

```powershell
New-AddressList -Name "West Region" -RecipientFilter {((RecipientType -eq 'UserMailbox') -and (Region -eq 'West'))}
```

- It's also worth noting that you can use multiple attributes in the recipient filter to create more complex filter conditions, for example, you can filter based on recipient type and custom attributes:

```powershell
New-AddressList -Name "Contractors" -RecipientFilter {((RecipientType -eq 'UserMailbox') -and (IsContract -eq 'True'))}
```

**To delete a custom address list**
`Remove-AddressList -Identity "Address List Name"`

**verify that the address list has been deleted, use the following command:**
`Get-AddressList | Format-List Name`

<b>To create a custom address list in Exchange 2019 from the Exchange Admin Center (EAC), follow these steps:</b>

- Open the Exchange Admin Center (EAC) by navigating to https://<your-server-name>/ecp.

- In the EAC, navigate to Recipients > Address lists.

- Click the "+" button to create a new address list.

- Fill in the following fields:

        - Name: Enter a name for the address list
        - Select recipients: Select the recipients that should be included in the list.
        - Add recipients by: Choose the way you want to add recipients, you can add them manually or by filtering them based on recipient attributes.

- Click Save to create the address list.

- To verify the address list was created, navigate to Recipients > Address lists, you should see the address list you've just created.

![21](https://user-images.githubusercontent.com/86381942/212836549-629a7bb9-f1de-4a8e-a55b-c6cdbe18a7bf.png)

<section id="custom">
      <h2>Create Custom Global Address List</h2>
      
 A custom global address list (GAL) is a customized version of the default global address list in an Exchange Server organization. The default GAL contains all mail-enabled objects in an Exchange organization, such as users, groups, and contacts. A custom GAL, on the other hand, allows you to create a specific subset of those objects based on certain criteria, such as department, location, or custom attributes.

For example, you can create a custom GAL that only includes users in the Marketing department, or a custom GAL that only includes users in a specific location. This allows users to easily find and communicate with the specific group of people they need to, without having to search through the entire GAL.

- To create a custom global address list (GAL) in Exchange 2019, you can use the Exchange Management Shell. Here are the steps to follow:

- Open the Exchange Management Shell on your Exchange server.

- Use the New-GlobalAddressList cmdlet to create a new GAL. For example, the following command creates a new GAL called "Custom GAL" that includes all mail-enabled users in the "HR" department:

```powershell
New-GlobalAddressList -Name "Custom GAL" -RecipientFilter {(RecipientType -eq 'UserMailbox') -and (Department -eq 'HR')}
```

![23](https://user-images.githubusercontent.com/86381942/213072150-4aed3586-5c1d-4a07-85ac-d4290d391b7e.png)

- Use the Set-GlobalAddressList cmdlet to modify the newly created GAL as needed. For example, the following command sets the custom GAL as the default GAL:

`Set-GlobalAddressList -Identity "Custom GAL" -DefaultGlobalAddressList $true`

- Use the Update-GlobalAddressList cmdlet to update the GAL so that it will reflect the changes that you have made:

`Update-GlobalAddressList -Identity "Custom GAL"`

<B>Before create or modify a GAL, it's recommended to backup your current GAL and test the custom GAL on a test environment.</B>

- To check a custom global address list (GAL) in Exchange 2019

`Get-GlobalAddressList -Identity "Custom GAL"`

- To view the recipients in the custom GAL, you can use the Get-Recipient cmdlet with the -Filter or -RecipientFilter parameter. For example, the following command gets all the recipients in the custom GAL:

```powershell
Get-Recipient -RecipientPreviewFilter {(alias -ne $null) -and (RecipientType -eq 'UserMailbox') -and (CustomAttribute1 -eq 'Marketing')}
```
- To view the recipients in a specific department in the custom GAL, you can use the Get-Recipient cmdlet with the -Filter or -RecipientFilter parameter. For example, the following command gets all the recipients in the "Marketing" department in the custom GAL:

```powershell
Get-Recipient -RecipientPreviewFilter {(alias -ne $null) -and (RecipientType -eq 'UserMailbox') -and (Department -eq 'Marketing')}
```

<b>You can substitute "CustomAttribute1" with the custom attribute that you used in the filter when you created the custom GAL.</b>

To delete a custom global address list (GAL)

`Remove-GlobalAddressList -Identity "Custom GAL"`

<b>Before you delete a custom GAL, it's recommended to make sure that it is no longer needed and it won't affect any other functionality in your organization. Also it's a good practice to backup your current GAL and test the deletion on a test environment.</b>

<b>To create a custom global address list (GAL) in Exchange 2019 using the Exchange Admin Center (EAC), follow these steps:</b>

- Open the Exchange Admin Center (EAC) by navigating to https://yourserver/ecp in a web browser.

- Log in with your administrator credentials.

- In the EAC, navigate to Recipients > Address Lists.

- Click the "+" (plus) button to create a new address list.

- In the "New Address List" window, enter a name for the custom GAL.

- In the "Recipient filter" section, you can specify the criteria for the custom GAL. For example, you can include only users in the "Marketing" department by adding the following filter: (Department -eq 'Marketing')

- Click Save to create the custom GAL.

- The custom GAL will now appear in the list of address lists.

- To set this custom GAL as the default GAL, navigate to Recipients > Address Lists, select the custom GAL and click on the three dots on the right corner of the custom GAL and select "Set as Default

![24](https://user-images.githubusercontent.com/86381942/213074392-b8ccaf6c-1ee1-4e5c-8e1c-52ff19400f21.png)


<section id="offline">
      <h2>Create Offline Address Book in Exchange 2019</h2>
      
An Offline Address Book (OAB) is a local copy of a Global Address List (GAL) that is downloaded and cached on a client computer. The OAB allows Outlook clients to access contact information, even when they are not connected to the Exchange server. This is particularly useful for users who work remotely or who have limited or unreliable network connectivity. 

In Exchange 2019, OABs are generated automatically on a regular schedule and are distributed to Outlook clients via a web-based distribution method. The OAB generation process creates a copy of the GAL and compresses it into a file with a .oab file extension. This file can then be downloaded by Outlook clients.

**To create a new Offline Address Book in Exchange 2019, you can use the Exchange Management Shell. Here are the steps to follow:

- Open the Exchange Management Shell on your Exchange server.

- Use the New-OfflineAddressBook cmdlet to create a new OAB. For example, the following command creates a new OAB called "Custom OAB" that includes all mail-enabled users in the "Marketing" department:

```powershell
New-OfflineAddressBook -Name "Custom OAB" -AddressLists "Custom GAL"
```
![25](https://user-images.githubusercontent.com/86381942/213096614-3b2e44c6-09c4-463d-bad3-9f7ef322fd96.png)

![26](https://user-images.githubusercontent.com/86381942/213096631-8fba8139-960e-4a2b-bd8f-10ab243cf88e.png)

- Use the Update-OfflineAddressBook cmdlet to update the OAB so that it will reflect the changes that you have made:

```powershell
Update-OfflineAddressBook -Identity "Custom OAB"
```

- To set this custom OAB as the default OAB, use the Set-OfflineAddressBook cmdlet:

```powershell
Set-OfflineAddressBook -Identity "Custom OAB" -VirtualDirectories $null
```

![27](https://user-images.githubusercontent.com/86381942/213096933-be148d18-e194-431a-8529-7a6d2bbc1726.png)

**Delete an Offline Address Book (OAB)**

`Remove-OfflineAddressBook -Identity "Custom OAB"`

**View the Offline Address Book (OAB)**

`Get-OfflineAddressBook`

- Retrieve all the Offline Address Books in your Exchange organization, and display the name and server name of each.

```powershell
Get-MailboxDatabase | where {$_.OfflineAddressBook -ne $null} | Format-Table Name,OfflineAddressBook
```
**This command will retrieve all the mailbox databases in your Exchange organization, and display the name and Offline Address Book associated with each.**

- To view the properties of a specific Offline Address Book you could use the following command:

`Get-OfflineAddressBook -Identity "OAB name" | Format-List`

**This command will retrieve the specific Offline Address Book you are looking for and display all the properties of that OAB.**
  
  <section id="url">
      <h2>Configure Internal and External URLs in Exchange 2019</h2>
    - In order to configure internal and external URLs in Exchange 2019, you will need to use the Exchange Management Shell (EMS).
    - To configure the internal URLs, you can use the following cmdlet:
    
    `Set-WebServicesVirtualDirectory -Identity "EWS (Default Web Site)" -InternalUrl https://mail.contoso.com/EWS/Exchange.asmx`

  - To configure the external URLs, you can use the following cmdlet:
   
    `Set-WebServicesVirtualDirectory -Identity "EWS (Default Web Site)" -ExternalUrl https://mail.contoso.com/EWS/Exchange.asmx`

   ![28](https://user-images.githubusercontent.com/86381942/214220552-7d0b278e-8296-47bd-9698-f89cbc7aa3a1.png)
    
   
    
![29](https://user-images.githubusercontent.com/86381942/214220608-493a126b-e7b7-4f7a-a67f-e247357f1b23.png)

  
    
 <p>It's also recommend to use the same URL for internal and external to avoid issues with autodiscover, also it's important to configure the SSL certificate for these URLs.</p>

- Also you can configure Internal and External URLs for other virtual directories that exchange provide like OWA, OAB, Autodiscover, etc.
    
- For Outlook on the web (OWA):
    
    ```
    Set-OwaVirtualDirectory -Identity "OWA (Default Web Site)" -InternalUrl https://mail.contoso.com/owa -ExternalUrl https://mail.contoso.com/owa
```
    
    - For Offline Address Book (OAB):
    
    ```
    Set-OabVirtualDirectory -Identity "OAB (Default Web Site)" -InternalUrl https://mail.contoso.com/oab -ExternalUrl https://mail.contoso.com/oab
```
    
   - For Autodiscover:
    
    ```
    Set-AutodiscoverVirtualDirectory -Identity "Autodiscover (Default Web Site)" -InternalUrl https://mail.contoso.com/autodiscover/autodiscover.xml -ExternalUrl https://mail.contoso.com/autodiscover/autodiscover.xml
```
    
  - For ActiveSync
    
    ```
    Set-ActiveSyncVirtualDirectory -Identity "Microsoft-Server-ActiveSync (Default Web Site)" -InternalUrl https://mail.contoso.com/Microsoft-Server-ActiveSync -ExternalUrl https://mail.contoso.com/Microsoft-Server-ActiveSync
```
    
    
    
  - Make sure to replace "https://mail.contoso.com" with the appropriate URLs for your organization and to configure the SSL certificate for these URLs.
    
    
    <section id="pop3">
      <h2>Configure POP3 Services in Exchange 2019 with Outlook</h2>
      
- To configure POP3 services in Exchange 2019 with Outlook, you will need to perform the following steps:

- Open the Exchange Management Shell (EMS) on the Exchange server.

- Run the following cmdlet to enable the POP3 service:
      `Enable-Pop3`
      
 - Run the following cmdlet to set the POP3 service to start automatically:
      `Set-Service MSExchangePOP3 -StartupType Automatic`
      
- Run the following cmdlet to configure the POP3 service to listen on a specific IP address and port:
      `Set-PopSettings -ListenOnIPAddress "10.0.0.1" -ListenOnPort 110`
      
 - Run the following cmdlet to configure the POP3 service to require SSL for connections:
      `Set-PopSettings -SSLRequired $true
      
- You will need to configure the SSL certificate for the POP3 service.

- In Outlook, open the File menu and select the Account Settings option.

- Select the New button, and then select the POP option.

- Fill in the account information and use the appropriate POP3 settings, such as the IP address and port number of the Exchange server, and select the "More settings" button.

- In the "Advanced" tab, make sure the checkbox "This server requires an encrypted connection (SSL)" is checked

- Click on the OK button to save the settings and close the account settings window.

- Restart the Microsoft Exchange POP3 service by running the following cmdlet:
      `Restart-Service MSExchangePOP3`
      
 Test the POP3 connection by trying to send and receive email through Outlook.
Please note that the above configuration is a basic example, you may need to adjust the settings based on your organization's specific requirements. 
      
      
 <section id="outlook">
      <h2>Configure Outlook Anywhere in Exchange 2019</h2> 
   
   - To configure Outlook Anywhere (also known as RPC over HTTP) in Exchange 2019, you will need to perform the following steps:

- Open the Exchange Management Shell (EMS) on the Exchange server.

- Run the following cmdlet to enable Outlook Anywhere for the entire organization:

```powershell
  Set-OutlookAnywhere -Identity "ServerName\Rpc (Default Web Site)" -ExternalHostname <OutlookAnywhereFQDN> -DefaultAuthenticationMethod NTLM -InternalHostname <ExchangeServerFQDN> -InternalClientsRequireSsl $true -ExternalClientsRequireSsl $true
   ```

![30](https://user-images.githubusercontent.com/86381942/214227093-a5ca22b4-cb18-44b5-9e93-19adb568448e.png)
   
   
![31](https://user-images.githubusercontent.com/86381942/214227130-2c7bf9fe-a9d2-4d11-b28f-dbb9040f559a.png)
   
   
![32](https://user-images.githubusercontent.com/86381942/214227139-7e929ff0-7582-439f-b459-6a4d246faefd.png)

   
 <section id="restrict">
      <h2>Configure Message Delivery Restrictions for a Mailbox </h2>     
      
  *To configure message delivery restrictions for a mailbox in Exchange 2019:

- Open the Exchange Admin Center.
- Select recipients in the navigation menu.
- Select mailboxes.

![35](https://user-images.githubusercontent.com/86381942/215617981-5d37c76f-e61b-4b2c-94ce-1710539e627e.png)


- Select the mailbox for which you want to configure message delivery restrictions.
- Select edit.

![36](https://user-images.githubusercontent.com/86381942/215618033-dfa41cf0-5827-4ed1-b0c0-63709ad3ae4f.png)


- Select Mailbox Features.
- Under Message delivery restrictions, select Configure.
- Select the options you want to apply to the mailbox.
- Click Save to apply the restrictions.    
      
![38](https://user-images.githubusercontent.com/86381942/215618056-4ebb77d3-0205-4f79-8972-1e0ee33868b5.png)

We can see that This users doesnt have permission to send Email.

![39](https://user-images.githubusercontent.com/86381942/215618258-afd605a6-00a6-4661-be9b-aa546ffceb99.png)


## To configure message delivery restrictions for a mailbox using PowerShell in Exchange 2019:

- Open Exchange Management Shell.
- Use the following command to set message delivery restrictions for a specific mailbox:

`Set-Mailbox <Identity> -MessageDeliveryRestriction <Restriction>`
- Identity is the identity of the mailbox for which you want to set the message delivery restrictions.
- Restriction is the message delivery restriction you want to apply to the mailbox.

* Example.
`Set-Mailbox "Rob Smith" -MessageDeliveryRestriction RejectMessageFromSendersNotInSafeSendersList`

- Use the following command to verify the changes:
`Get-Mailbox <Identity> | Select MessageDeliveryRestriction`

<section id="attach">
      <h2>How to Increase Max Received Size in Exchange 2019</h2>
  - Use the following command to view the current attachment size limit:
    `Get-TransportConfig | Select MaxReceiveSize`  
  
  - Use the following command to increase the attachment size limit:
    `Set-TransportConfig -MaxReceiveSize <SizeInBytes>`
  
  - Restart the Microsoft Exchange Transport service for the changes to take effect:
    `Restart-Service MSExchangeTransport`
  
  ![40](https://user-images.githubusercontent.com/86381942/215620646-10df468d-f341-4a18-ab69-110050a8b0f7.png)
  
  ## To increase the maximum send message size (MB) in Exchange 2019
  
  - Use the following command to view the current maximum send message size limit:
  `Get-TransportConfig | Select MaxSendSize`
  
  - Use the following command to increase the maximum send message size limit:
  `Set-TransportConfig -MaxSendSize <SizeInBytes>`
  
  * Restart the Exchage Transport Services.
 
  ![41](https://user-images.githubusercontent.com/86381942/215620936-78acf442-1c08-43e7-8c34-4675fafe7074.png)

  ## To increase the maximum send message size limit in Exchange 2019 from Exchange Admin Center (EAC):

- Open the Exchange Admin Center.
- Select mail flow in the navigation menu.
- Select send connectors.
- Select the send connector for which you want to increase the maximum send message size limit.
- Select edit.
- Select the general tab.
- Under message size restrictions, increase the value in the maximum send size field.
- Select save to apply the changes.

  * Note: The maximum send message size limit applies to all email messages sent from the Exchange server, not just a specific mailbox.
  
  
  <section id="offaccess">
      <h2>Enable Offline Access in Outlook on the Web in Exchange 2019</h2>
    
- To enable offline access in Outlook on the Web (OWA) in Exchange 2019:
   - Log in to OWA as the user for whom you want to enable offline access.
   - Click on the gear icon in the upper-right corner and select "Offline settings".
   
    ![54](https://user-images.githubusercontent.com/86381942/215623538-1ce4a31a-f7bd-4243-b31c-ec30a620e67f.png)
    
    - Select the folders that you want to be available offline.
    - Click on the "Save" button to apply the changes.
    
    ![55](https://user-images.githubusercontent.com/86381942/215623643-3c47626c-7765-487f-8cb9-b226ea141f32.png)
    
    
<section id="emailfor">
      <h2>Configure Email Forwarding for a Mailbox in Exchange 2019</h2>
  
- To configure email forwarding for a mailbox in Exchange 2019:

- Use the following command to enable email forwarding for a specific mailbox:
  `Set-Mailbox <Identity> -ForwardingAddress <ForwardingAddress> -DeliverToMailboxAndForward $true`
  
* Identity is the identity of the mailbox for which you want to configure email forwarding.
* ForwardingAddress> is the email address to which messages will be forwarded.
* $true means that the messages will be delivered to the mailbox and forwarded to the specified address.
  
  ##Example
 
  ![57](https://user-images.githubusercontent.com/86381942/215625054-76f625b1-d545-4902-b623-e8f220e7e247.png)

  - Use the following command to verify the changes
  
`Get-Mailbox <Identity> | Select ForwardingAddress, DeliverToMailboxAndForward`
  
  
 <section id="mailtip">
      <h2>Configure Custom MailTips for Recipients in Exchange 2019</h2>   
   
   - Select the mailbox for which you want to configure a custom MailTip.
   - Scroll down to the MailTips section.
   - In the Message Tip box, enter the custom MailTip that you want to set.
   - Click Save.
   
   ![58](https://user-images.githubusercontent.com/86381942/215626218-ee6a724b-87e0-43b0-8a27-915f302fdc07.png)

   ![59](https://user-images.githubusercontent.com/86381942/215626250-cfd0ed78-1a7a-4916-9abd-18d797b15457.png)
   
   
<section id="quota">
      <h2>Configure Storage Quota for a Mailbox in Exchange 2019</h2>
  
 - To configure storage quota for a mailbox in Exchange 2019 using PowerShell, you can use the Set-Mailbox cmdlet.
  
  `Get-Mailbox -ResultSize Unlimited | Set-Mailbox -UseDatabaseQuotaDefaults $False -IssueWarningQuota 4.9GB -ProhibitSendQuota 5GB`
  
  - to check the storage quotas for a specific mailbox, or you can retrieve the storage quotas for all mailboxes in your organization by using the following command:
  
  `Get-Mailbox -ResultSize Unlimited | Select-Object DisplayName,IssueWarningQuota,ProhibitSendQuota`
  
* This will return a list of all mailboxes in your organization, including the DisplayName, IssueWarningQuota, and ProhibitSendQuota properties for each mailbox. The IssueWarningQuota property represents the mailbox size at which a warning message will be sent to the user, and the ProhibitSendQuota property represents the maximum size for a mailbox beyond which the user will not be able to send messages.
  
## Example
  
  ![60](https://user-images.githubusercontent.com/86381942/215628075-e0744dad-3ff8-466b-b567-4f4a5483e581.png)
  
  ![62](https://user-images.githubusercontent.com/86381942/215628087-80401b95-23c3-4bcc-af6f-e97f895b6b7a.png)
  
  <section id="limit">
      <h2>Introduction</h2>
    
    * To configure mailbox database limits in Exchange Server 2019
    
    `Set-MailboxDatabase -Identity <DatabaseName> -IssueWarningQuota <Size> -ProhibitSendQuota <Size> -ProhibitSendReceiveQuota <Size>`
    
    ![64](https://user-images.githubusercontent.com/86381942/215630843-51d3df3d-70e2-4af0-b46b-1f8f3adc89e4.png)
    
    - Use the following command to check mailbox database quota:
    `Get-MailboxDatabase -Identity "DB02" | Select-Object *Quota*`
    
    
    
    







  
  
  
   
   
   


  


      

      
      

      

      

      






























































   
   
  
  
  
  
  
  
  

  
     
