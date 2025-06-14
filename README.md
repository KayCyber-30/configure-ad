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

- Set up Domain Controller in Azure
- Set up Client-1 in Azure
- After VM is created, set Domain Controller’s NIC Private IP address to be static
- Log into the VM and disable the Windows Firewall (for testing connectivity)
- After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address
- Attempt to ping DC-1’s private IP address and ensure the ping succeeded
- From Client-1, open PowerShell and run ipconfig /all and the output for the DNS settings should show Dc-1's private IP Address
- Install Active Directory
- Create a Domain Admin user within the domain
- Join Client1 to your domain(my-domain.com)
- Set up Remote Desktop for non-administrative users on Client-1
- Create a bunch of additional users and attempt to log into client-1 with one of the users
<h2>Deployment and Configuration Steps</h2>

- Set up Domain Controller in Azure

![image](https://github.com/user-attachments/assets/06f81fe6-fa82-480f-bf53-6103d4f5ac2b)

- Set up Client-1 in Azure

![image](https://github.com/user-attachments/assets/7040c6e5-6e03-48f0-9cd5-7e2048665201)

- After VM is created, set Domain Controller’s NIC Private IP address to be static

![image](https://github.com/user-attachments/assets/9763434e-60c4-4325-97a8-dcde1ae4430b)

- Log into the VM and disable the Windows Firewall (for testing connectivity)

![image](https://github.com/user-attachments/assets/65d6e708-7ca2-4079-b425-8cc33ee75cd9)

- After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address

![image](https://github.com/user-attachments/assets/93151955-2e36-44ee-9f7e-2bfdc94b55ae)

- Attempt to ping DC-1’s private IP address and ensure the ping succeeded

 ![image](https://github.com/user-attachments/assets/c4d008c0-4889-42da-bcd9-c72da1342f49)
  
- From Client-1, open PowerShell and run ipconfig /all and the output for the DNS settings should show Dc-1's private IP Address

  ![image](https://github.com/user-attachments/assets/0e9e62a8-956f-4675-8895-fc7064ff2966)


Install Active Directory
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
