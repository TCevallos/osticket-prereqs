<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- IIS with CGI and Common HTTP Features
- IIS Management Console
- PHP Manager for IIS
- Rewrite Modle
- PHP 7.3.8
- VC-redist.x86.exe
- MySQL 5.5.62
- osTicket

<h2>Installation Steps</h2>

<p>In Microsoft Azure, create a resource group, a Windows 10 Virtual Machine, and a Virtual Network (Vnet).</p>

<img height="80%" width="80%" alt="Azure Virtual Machine" src="https://github.com/golayjustin/osticket-prereqs/assets/39071760/fd242b4b-8abc-4dad-bb17-6e36fdea9e34">
&nbsp;
&nbsp;

<p>Use "Remote Desktop Connection" to connect to the virtual machine.</p>
<img height="80%" width="80%" alt="Remote Connection"  src="https://github.com/golayjustin/osticket-prereqs/assets/39071760/0e7486ff-3c5f-4541-931b-305d7ee428f5">
&nbsp;
&nbsp;

<p>Install Internet Information Services in Windows with CGI and Common HTTP Features.</p>
<img height="80%" width="80%" alt="Internet Information Services" src="https://github.com/golayjustin/osticket-prereqs/assets/39071760/acab85e0-5174-4d6d-a2e8-661622de43d4">
&nbsp;
&nbsp;

<p>Download and install PHP Manager for IIS.</p>
<img height="80%" width="80%" alt="PHP Manager for IIS" src="https://i.imgur.com/aeOBNB4.png">
&nbsp;
&nbsp;

<p>Download and install the Rewrite Module.</p>
<img height="80%" width="80%" alt="Rewrite Module" src="https://i.imgur.com/G0H8GRa.png">
&nbsp;
&nbsp;

<p>Create the directory C:\PHP</p>
<img height="80%" width="80%" alt="PHP directory" src="https://i.imgur.com/Jk63pjQ.png">
&nbsp;
&nbsp;

<p>Download PHP 7.3.8 and unzip the contents into C:\PHP</p>
<img height="80%" width="80%" alt="PHP" src="https://i.imgur.com/Jk63pjQ.png">
&nbsp;
&nbsp;

<p>Download and install Microsoft Visual C++.</p>
<img height="80%" width="80%" alt="Visual C++" src="https://i.imgur.com/IY4XxGF.png">
&nbsp;
&nbsp;

<p>Download and install MySQL 5.5.62.</p>
<img height="80%" width="80%" alt="MySQL" src="https://i.imgur.com/CiOTZG9.png">
&nbsp;
&nbsp;

<img height="80%" width="80%" alt="MySQL Configuration" src="https://i.imgur.com/a7eqn9V.png">
&nbsp;
&nbsp;

<p>Open IIS as an Admin.</p>
<img height="80%" width="80%" alt="IIS as Admin" src="https://i.imgur.com/ERATRAk.png">
&nbsp;
&nbsp;

<p>Register PHP from within IIS and reload IIS.</p>
<img height="80%" width="80%" alt="Register PHP" src="https://i.imgur.com/fHlIpIA.png">
&nbsp;
&nbsp;

<p>Download osTicket. Copy "upload" folder to C:\inetpub\wwwroot and rename "upload" to "osTicket". Reload IIS.</p>
<img height="80%" width="80%" alt="Rename upload to osTicket" src="https://i.imgur.com/MOU6SCF.png">
&nbsp;
&nbsp;

<img height="80%" width="80%" alt="Reload IIS" src="https://i.imgur.com/A45y48g.png">
&nbsp;
&nbsp;

<p>Browse "*.80".</p>
<img height="80%" width="80%" alt="Browse *.80" src="https://i.imgur.com/cSeJ5U7.png">
&nbsp;
&nbsp;

<p>In PHP Manager, enable php_imap, php_intel, and php_opcache. Refresh browser.</p>
<img height="80%" width="80%" alt="php_imap" src="https://i.imgur.com/RTz8xJ2.png">
&nbsp;
&nbsp;

<img height="80%" width="80%" alt="php_intel" src="https://i.imgur.com/NLH6X51.png">
&nbsp;
&nbsp;

<img height="80%" width="80%" alt="php_opcache" src="https://i.imgur.com/5khu3OX.png">
&nbsp;
&nbsp;

<p>Rename "ost-sampleconfig" to "ost-config".</p>
<img height="80%" width="80%" alt="Rename to ost-config" src="https://i.imgur.com/0Rof4Nq.png">
&nbsp;
&nbsp;

<p>Assign permissions to ost-config by disabling inheritance and giving all permissions to "Everyone".</p>
<img height="80%" width="80%" alt="Permissions for ost-config" src="https://i.imgur.com/R2lhUus.png">
&nbsp;
&nbsp;

<p>Resume set up in the browser by inputing required information.</p>
<img height="80%" width="80%" alt="Input information into osTicket" src="https://i.imgur.com/7BiU7jq.png">
&nbsp;
&nbsp;

<p>Download and install HeidiSQL and create a database called "osTicket".</p>
<img height="80%" width="80%" alt="HeidiSQL" src="https://i.imgur.com/9ebN03I.png">
&nbsp;
&nbsp;

<img height="80%" width="80%" alt="HeidiSQL" src="https://i.imgur.com/9PS1Evn.png">
&nbsp;
&nbsp;

<p>Finish set up in the browser by entering MySQL Database as "osTicket". Select "Install now!"</p>
<img height="80%" width="80%" alt="Finish osTicket setup" src="https://i.imgur.com/ZpEDdWr.png">
&nbsp;
&nbsp;

<p>Both the help desk login page and end user web page are functioning.</p>
<img height="80%" width="80%" alt="osTicket log in page" src="https://i.imgur.com/PdCBl1m.png">
&nbsp;
&nbsp;

<img height="80%" width="80%" alt="osTicket end user web page" src="https://i.imgur.com/kCKiyBb.png">
&nbsp;
&nbsp;

<p>Before moving on, delete C:\inetpub\wwwroot\osTicket\setup and set the permissions to "Read" on ost-config file.</p>
<img height="80%" width="80%" alt="Set ost-config to read only" src="https://i.imgur.com/8pW1JCB.png">
&nbsp;
&nbsp;
