
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
   
   ```powershell
   New-AcceptedDomain -Name "domain.com" -DomainName "domain.com" -DomainType "Authoritative"
```
  **Note: Replace "domain.com" with the domain name that you want to create as an accepted domain**
   
   - To set the new accepted domain as the default domain, use the following command:
   
   ```powershell
   Set-AcceptedDomain -Identity "domain.com" -IsDefault $true
```
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

   


   
   
  
  
  
  
  
  
  

  
     
