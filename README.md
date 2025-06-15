<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Deploy a Domain Controller (DC-1) in Azure
 
- Deploy a client machine (Client-1) in Azure

- Assign a static private IP address to DC-1's network interface (in Azure portal)

- Log into DC-1 and temporarily disable Windows Firewall (for connectivity testing only)

- Set Client-1’s DNS server address to DC-1’s private IP address (via Azure VM settings or within Windows)

- Verify network connectivity from Client-1 to DC-1 by pinging DC-1’s private IP

- On Client-1, run ipconfig /all in PowerShell to confirm that the DNS server is correctly set to DC-1’s IP

- Install the Active Directory Domain Services (AD DS) role on DC-1

- Promote DC-1 to a Domain Controller, creating a new forest and domain (e.g., mydomain.com)

- Create a new Domain Admin user within the mydomain.com domain using Active Directory Users and Computers (ADUC)

- Join Client-1 to the domain (e.g., mydomain.com)

- Configure Remote Desktop access on Client-1 for non-administrative domain users (add users to the Remote Desktop Users group)

- Create additional domain users using PowerShell or ADUC

- Test domain user logins by signing into Client-1 with one of the new user accounts

- In Active Directory Users and Computers, verify that the new accounts exist in the appropriate Organizational Units (OUs)

<h2>Deployment and Configuration Steps</h2>

- Deploy a Domain Controller (DC-1) in Azure

![image](https://github.com/user-attachments/assets/06f81fe6-fa82-480f-bf53-6103d4f5ac2b)

- Deploy a client machine (Client-1) in Azure
  
![image](https://github.com/user-attachments/assets/7040c6e5-6e03-48f0-9cd5-7e2048665201)

- Assign a static private IP address to DC-1's network interface (in Azure portal)
  
![image](https://github.com/user-attachments/assets/9763434e-60c4-4325-97a8-dcde1ae4430b)

- Log into DC-1 and temporarily disable Windows Firewall (for connectivity testing only)
  
![image](https://github.com/user-attachments/assets/65d6e708-7ca2-4079-b425-8cc33ee75cd9)

- Set Client-1’s DNS server address to DC-1’s private IP address (via Azure VM settings or within Windows)
  
![image](https://github.com/user-attachments/assets/93151955-2e36-44ee-9f7e-2bfdc94b55ae)

- Verify network connectivity from Client-1 to DC-1 by pinging DC-1’s private IP

 ![image](https://github.com/user-attachments/assets/c4d008c0-4889-42da-bcd9-c72da1342f49)
  
- On Client-1, run ipconfig /all in PowerShell to confirm that the DNS server is correctly set to DC-1’s IP
  
  ![image](https://github.com/user-attachments/assets/0e9e62a8-956f-4675-8895-fc7064ff2966)


- Install the Active Directory Domain Services (AD DS) role on DC-1

![image](https://github.com/user-attachments/assets/3d652e65-5c06-4af8-841e-057ac4d28e95)

- Promote DC-1 to a Domain Controller, creating a new forest and domain (e.g., mydomain.com)

![image](https://github.com/user-attachments/assets/5581543a-ef78-453b-bd4e-3b1916913f63)

- Create a new Domain Admin user within the mydomain.com domain using Active Directory Users and Computers (ADUC)
  
  ![image](https://github.com/user-attachments/assets/aefd18b9-dfd7-41ff-8b2f-3307725c31e0)

-  Join Client-1 to the domain (e.g., mydomain.com)
  
![image](https://github.com/user-attachments/assets/c3e53b5f-3133-4d77-a629-0a990fefb01e)

- Configure Remote Desktop access on Client-1 for non-administrative domain users (add users to the Remote Desktop Users group)

![image](https://github.com/user-attachments/assets/2b0c6857-588f-40ae-a0c0-dd1eea7f7731)

- Create additional domain users using PowerShell or ADUC

![image](https://github.com/user-attachments/assets/c530c203-8fb1-4878-8126-b04d0a57cf56)

- Test domain user logins by signing into Client-1 with one of the new user accounts;

In Active Directory Users and Computers, verify that the new accounts exist in the appropriate Organizational Units (OUs)


![image](https://github.com/user-attachments/assets/72649e75-57ed-4aa5-bfd3-d70ea0afb30f)


