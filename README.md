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



