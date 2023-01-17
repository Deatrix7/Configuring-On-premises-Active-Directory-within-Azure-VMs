<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com/watch?v=85-bp7XxWDQ)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/s8yRNMh.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Active Directory

1.Login to DC-1 and install Active Directory Domain Services

2.Promote as a DC: Setup a new forest as mydomain.com (this can be anything, just remember what it is)

3.Restart and then log back into DC-1 as user: mydomain.com\labuser

Create an Admin and Normal User Account in AD
1.In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”

2.Create a new OU named “_ADMINS”

3.Create a new employee named “Jane Doe” (same password) with the username of “jane_admin”

4.Add jane_admin to the “Domain Admins” Security Group

5.Log out or close the Remote Desktop connection to DC-1 and log back in as “mydomain.com\jane_admin”

6.User jane_admin as your admin account from now on
</p>
<br />

<p>
<img src="https://i.imgur.com/Aa2Srdf.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Join Client-1 to your domain (mydomain.com)

1.From the Azure Portal, set Client-1’s DNS settings to the DC’s Private IP address

2.From the Azure Portal, restart Client-1

3.Login to Client-1 (Remote Desktop) as the original local admin (labuser) and join it to the domain (computer will restart)

4.Login to the Domain Controller (Remote Desktop) and verify Client-1 shows up in Active Directory Users and Computers (ADUC) inside the “Computers” container on the root of the domain

5.Create a new OU named “_CLIENTS” and drag Client-1 into there


Setup Remote Desktop for non-administrative users on Client-1

1.Log into Client-1 as mydomain.com\jane_admin and open system properties

2.Click “Remote Desktop”

3.Allow “domain users” access to remote desktop

4.You can now log into Client-1 as a normal, non-administrative user now
</p>
<br />

<p>
<img src="https://i.imgur.com/QENCJrv.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
