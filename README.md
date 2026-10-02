# active-directory-home-lab
Windows Server lab covering Active Directory, users and groups, Group Policy, shared folders, and NTFS permissions.

## Part 1: Active Directory Domain Services Deployment

### Installing the AD DS Role

<img width="952" height="803" alt="image" src="https://github.com/user-attachments/assets/3366c048-7d88-481d-87c1-5d57587f5e3a" />

I opened the Add Roles and Features Wizard to begin installing Active Directory Domain Services on the Windows Server.

### Selecting Active Directory Domain Services

<img width="966" height="489" alt="image" src="https://github.com/user-attachments/assets/1cd81a27-01f4-4f40-906a-fb24283d26db" />

I selected the Active Directory Domain Services role to install the components needed for centralized authentication and directory management.

### Completing the AD DS Installation

<img width="1019" height="531" alt="image" src="https://github.com/user-attachments/assets/feb253c4-b4c5-4595-8542-f976171acc7b" />

The AD DS role installation completed successfully. The server was ready to be promoted to a domain controller.

### Creating the Forest and Domain

<img width="994" height="734" alt="image" src="https://github.com/user-attachments/assets/0bd0dc37-7231-423b-94c6-f22b54213f48" />

I created a new Active Directory forest with the domain name corp.local. This became the domain used throughout the lab.

### Checking Prerequisites for Domain Controller Promotion

<img width="997" height="513" alt="image" src="https://github.com/user-attachments/assets/d51451c6-643d-42b4-a6fd-24742c8da5f4" />

I ran the prerequisite checks before promoting the server to a domain controller. The checks confirmed that installation could proceed.

### Successful Prerequisite Validation

<img width="1019" height="581" alt="image" src="https://github.com/user-attachments/assets/a33bd408-0551-4e67-9890-6aa7dc6ebfbc" />

The prerequisite checks completed successfully, confirming that the server was ready for domain controller promotion.

### Verifying the Domain in Active Directory Users and Computers

<img width="980" height="508" alt="image" src="https://github.com/user-attachments/assets/b951ef0a-f29b-47b5-9d37-1cd505b23666" />

After promotion, I opened Active Directory Users and Computers and verified that the corp.local domain was available for administration.

### Creating a Domain User Account

<img width="1020" height="705" alt="image" src="https://github.com/user-attachments/assets/e743a131-0069-4992-a181-f9a2df0cb5f1" />

I created a user account within the domain using Active Directory Users and Computers. This demonstrated centralized user account administration.

### Part 1 Summary

I installed Active Directory Domain Services, created the corp.local forest and domain, and promoted the server to a domain controller. I then verified the domain in Active Directory Users and Computers and created a domain user account.

## Part 2: Organizational Units and User Management

### Creating Departmental Organizational Units

<img width="939" height="495" alt="image" src="https://github.com/user-attachments/assets/914bc0b4-4488-454d-9212-5d480e69c053" />

I created Organizational Units for IT, Human Resources, and Sales to organize user accounts and groups by department.

### Creating IT Accounts and a Security Group

<img width="966" height="495" alt="image" src="https://github.com/user-attachments/assets/6540265e-9b40-41b9-a366-9ce826d6abf1" />

I created IT department accounts and the IT Staff security group to support departmental access management.

### Creating HR Accounts and a Security Group

<img width="984" height="742" alt="image" src="https://github.com/user-attachments/assets/acacc6e8-7254-4b82-8f88-6489b67c19c1" />

I created Human Resources accounts and the HR Staff security group within the HR Department OU.

### Creating Sales Accounts and a Security Group

<img width="977" height="573" alt="image" src="https://github.com/user-attachments/assets/05bdb0d4-4a4b-4cad-acf0-d4ba88b3752c" />

I created Sales department accounts and the Sales Staff security group within the Sales Department OU.

### Configuring the Domain Password Policy

<img width="950" height="497" alt="image" src="https://github.com/user-attachments/assets/72492e6e-6cde-4769-a788-7d86d2f38253" />

I used Group Policy Management to configure and link a password security policy at the domain level.

### Setting Password Policy Requirements

<img width="953" height="406" alt="image" src="https://github.com/user-attachments/assets/3c077e08-d9f1-4e3e-8419-83c8c38997bb" />

I configured password history, password age, minimum length, and complexity requirements for domain accounts.

### Verifying IT Staff Membership

<img width="1052" height="458" alt="image" src="https://github.com/user-attachments/assets/f04a9c43-3050-4999-aeee-d1630ed87ab9" />

I checked the IT Staff group's membership to confirm that the appropriate IT accounts were included.

### Reviewing HR Staff Group Membership

<img width="1064" height="438" alt="image" src="https://github.com/user-attachments/assets/3dfef981-2b48-46ac-a5a9-3a93b9823f5b" />

I reviewed the HR Staff security group's membership in Active Directory Users and Computers.

### Confirming HR User Membership

<img width="1036" height="434" alt="image" src="https://github.com/user-attachments/assets/2d5a38b3-204e-4366-9f8c-56f0be43a8cb" />

I confirmed that HR User1 and HR User2 were listed on the Members tab of the HR Staff security group.

### Confirming Sales User Membership

<img width="1044" height="602" alt="image" src="https://github.com/user-attachments/assets/5d0b7c74-b669-47e3-9bc8-db3a9477f034" />

I confirmed that Sales User1 and Sales User2 were listed on the Members tab of the Sales Staff security group.

### Part 2 Summary

I created departmental OUs, user accounts, and security groups, then verified group memberships. I also configured a domain password policy to manage account password requirements centrally.

## Part 3: Shared Folders and Access Control

### 1. Creating Departmental Shared Folders

<img width="1020" height="489" alt="image" src="https://github.com/user-attachments/assets/9d06f6cf-b307-4581-ace7-c0230a9a3953" />

I created IT_Share, HR_Share, and Sales_Share inside C:\CompanyShares to organize departmental files.

### 2. Configuring IT Share NTFS Permissions

<img width="1008" height="511" alt="image" src="https://github.com/user-attachments/assets/1649fe5d-6676-4d3d-a5c1-a9c9c06cfc30" />

I assigned the IT Staff security group Full Control permissions to IT_Share while retaining access for Administrators and SYSTEM.

### 3. Configuring HR Share NTFS Permissions

<img width="1027" height="791" alt="image" src="https://github.com/user-attachments/assets/ea2ba05c-f14d-4994-b80e-72c477b4b54f" />

I assigned the HR Staff security group Full Control permissions to HR_Share while retaining access for Administrators and SYSTEM.

### 4. Configuring Sales Share NTFS Permissions

<img width="1071" height="683" alt="image" src="https://github.com/user-attachments/assets/d9b143e8-084a-4df7-ba9d-0fcf9b49ec67" />

I assigned the Sales Staff security group Full Control permissions to Sales_Share while retaining access for Administrators and SYSTEM.

### 5. Testing Denied Access to the IT Share

<img width="1039" height="568" alt="image" src="https://github.com/user-attachments/assets/f97272e9-d0c7-4fd1-8ea6-23e56f97031f" />

I attempted to open \\localhost\IT_Share. Windows displayed a permission-denied message for the account used in this test.

### 6. Testing Denied Access to the Sales Share

<img width="1062" height="505" alt="image" src="https://github.com/user-attachments/assets/6d8a4bb0-8f39-4318-81f4-e80e802ebe3c" />

I attempted to open \\localhost\Sales_Share. Windows displayed a permission-denied message for the account used in this test.

### 7. Testing Denied Access to the HR Share

<img width="1061" height="543" alt="image" src="https://github.com/user-attachments/assets/944aa5d0-145e-444e-8cf7-cb86b479bad2" />

I attempted to open \\localhost\HR_Share. Windows displayed a permission-denied message for the account used in this test.

### 8. Verifying Access to the IT Share

<img width="1027" height="565" alt="image" src="https://github.com/user-attachments/assets/6adc9b0b-2163-4687-b813-80da5a815331" />

I successfully opened IT_Share through its network share path, confirming access during this test.

### 9. Verifying Access to the Sales Share

<img width="1055" height="780" alt="image" src="https://github.com/user-attachments/assets/a6db2b9a-156e-4e8f-9820-e3c302126f7e" />

I successfully opened Sales_Share through its network share path, confirming access during this test.

### 10. Verifying Access to the HR Share

<img width="1045" height="680" alt="image" src="https://github.com/user-attachments/assets/35ef4c5d-c3de-468e-a5dc-e94c8a94fbb0" />

I successfully opened HR_Share through its network share path, confirming access during this test.

### Part 3 Summary

I created departmental shared folders, configured NTFS permissions using Active Directory security groups, and documented both denied and successful access tests.

## Part 4: Mapping Network Drives with Group Policy

### 1. Creating the IT Drive Mapping GPO

<img width="1034" height="736" alt="image" src="https://github.com/user-attachments/assets/b4666b95-f37b-4c7e-99d9-8f72e6847025" />

I created a Group Policy Object named IT Drive Mapping to configure the IT department’s network drive.

### 2. Configuring the IT Drive Mapping

<img width="1061" height="914" alt="image" src="https://github.com/user-attachments/assets/751b69fd-1dde-4982-868e-3dd37d53b838" />

I used Group Policy Preferences to map the IT shared folder to drive I:.

### 3. Reviewing the IT Drive Mapping Configuration

<img width="977" height="600" alt="image" src="https://github.com/user-attachments/assets/bd93cedc-60bc-4423-991d-328e65a475c3" />

I verified that the I: drive mapping appeared in the GPO’s Drive Maps settings.

### 4. Verifying the IT Network Drive

<img width="1004" height="536" alt="image" src="https://github.com/user-attachments/assets/190b660c-2ab3-42f5-8382-6a9fbbd625c0" />

I confirmed that IT Share (I:) appeared under Network Locations in File Explorer.

### 5. Opening the IT Shared Drive

<img width="1052" height="808" alt="image" src="https://github.com/user-attachments/assets/bccfaf9e-db00-438e-ae24-d03ad393a9f1" />

I opened IT Share (I:) successfully to verify access to the mapped folder.

### 6. Creating the Sales Drive Mapping GPO

<img width="1048" height="554" alt="image" src="https://github.com/user-attachments/assets/26b24ad0-93d2-4d67-a5e7-912603850df1" />

I created a Group Policy Object named Sales Drive Mapping for the Sales department.

### 7. Configuring the Sales Drive Mapping

<img width="1048" height="529" alt="image" src="https://github.com/user-attachments/assets/370cef62-4f3e-48db-8836-dfe7c9bede4e" />

I used Group Policy Preferences to map the Sales shared folder to drive S:.

### 8. Reviewing the Sales Drive Mapping Configuration

<img width="1041" height="759" alt="image" src="https://github.com/user-attachments/assets/9efa1c43-919f-492a-847e-b51360252348" />

I verified that the S: drive mapping appeared in the GPO’s Drive Maps settings.

### 9. Verifying the Sales Network Drive

<img width="1031" height="808" alt="image" src="https://github.com/user-attachments/assets/b6cf5b79-03c0-4d40-9e01-7db973c1106c" />

I confirmed that Sales Share (S:) appeared under Network Locations in File Explorer.

### 10. Opening the Sales Shared Drive

<img width="993" height="753" alt="image" src="https://github.com/user-attachments/assets/e1a4fc01-e4df-4e37-9257-98ad24ab04ac" />

I opened Sales Share (S:) successfully to verify access to the mapped folder.

### 11. Creating the HR Drive Mapping GPO

<img width="1033" height="535" alt="image" src="https://github.com/user-attachments/assets/2d69c58a-2cb3-4833-a7c7-ed1767935235" />

I created a Group Policy Object named HR Drive Mapping for the HR department.

### 12. Configuring the HR Drive Mapping

<img width="1048" height="540" alt="image" src="https://github.com/user-attachments/assets/6118502b-76b1-408b-9043-3ad21a8e3ab6" />

I used Group Policy Preferences to map the HR shared folder to drive H:.

### 13. Reviewing the HR Drive Mapping Configuration

<img width="900" height="676" alt="image" src="https://github.com/user-attachments/assets/af7f1d0d-275d-4e35-bdea-458019957796" />

I verified that the H: drive mapping appeared in the GPO’s Drive Maps settings.

### 14. Applying the Group Policy Updates

<img width="900" height="566" alt="image" src="https://github.com/user-attachments/assets/6a7898ab-909f-45af-8617-33366746a911" />

I ran gpupdate /force and confirmed that both computer and user policies updated successfully.

### 15. Verifying the HR Network Drive

<img width="937" height="494" alt="image" src="https://github.com/user-attachments/assets/494517a3-063b-4370-923e-c084c20fc3f0" />

I confirmed that HR Share (H:) appeared under Network Locations in File Explorer.

### 16. Opening the HR Shared Drive

<img width="900" height="674" alt="image" src="https://github.com/user-attachments/assets/2a0c2e50-d2bd-483b-b1cb-7a691fa2b8ed" />

I opened HR Share (H:) successfully to verify access to the mapped folder.

### Part 4 Summary

I configured Group Policy Preferences to map departmental shared folders to drives I:, S:, and H:. I verified that each mapped drive appeared in File Explorer and opened successfully, demonstrating centralized network drive configuration.
