<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Deployment Of Windows Server 2022
- Prepping server for domain status
- Connect User computer to server
- Ensure logins work for admins & non-adnin users

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/fqIFI7U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Successful deployment of Windows Server in Azure environment.
</p>
<br />

<p>
<img src="https://i.imgur.com/hVqzbB9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here is where i change my settings for the private ip address on the server from dynamic to static. I want the ip address to stay the same so the server can play host to the client computer.
</p>
<br />

<p>
<img src="https://i.imgur.com/KopD75T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Successful deployment of client computer.
</p>
<br />

<p>
<img src="https://i.imgur.com/G4BgNkB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here i am going into the server firewall settings to allow ICMP traffic inbound so client computer can communicate with server.
</p>
<br />

<p>
<img src="https://i.imgur.com/UgCQRGg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here i executed a ping command from the client computer to the server to ensure connectivity. As you can see, the connection was successful.
</p>
<br />

<p>
<img src="https://i.imgur.com/KVGdRrP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Active Directory has been installed and the server was promoted to domain status. Next, i will create an admin account & a user account.
</p>
<br />

<p>
<img src="https://i.imgur.com/WFtcVkQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Created an employee called jane admin & added her to the Domains Admin group. Next, i will connect client computer to the server.
</p>
<br />

<p>
<img src="https://i.imgur.com/jVQzEdu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Changed client DNS to server private ip address so to allow it to connect to the server.
</p>
<br />

<p>
<img src="https://i.imgur.com/Cdj3FYo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Used ipconfig /all to verify client computer connection to the server. Client DNS is 10.0.0.4 which is the same as the server private ip address.
</p>
<br />

<p>
<img src="https://i.imgur.com/ve164yk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Allowing all domain users remote desktop access to server via client computer.
</p>
<br />

<p>
<img src="https://i.imgur.com/yxEBpGc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Using Powershell ISE to generate random users to domain users in server.
</p>
<br />

<p>
<img src="https://i.imgur.com/wZXTSB8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Logged in as a random non-administrative user on client computer accessing the server.
</p>
<br />
</p>


