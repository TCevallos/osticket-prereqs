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

<p>Next simply connect to your newly created VM using RDP using the public IPv4 address. If you are a Mac user you will have to download Microsoft RDP. 
</p>
<img src="https://i.imgur.com/uLVKzxS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
</p>
<p>
Now that you are connected to your VM you will have to enable IIS. Simply access the control panel then select uninstall a program. Off to the left select "Turn windows features on or off". A list will appear then you will enable Internet Information Services.
</p>  
<img src="https://i.imgur.com/qtEnuWu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
</p>
<p>
Excellent. Now that you have enabled IIS we need to install Web Platform Installer. I have provided a link here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
  That link will provide you with all of the material you need to download to get osTicket up and running. Simply click the link and install the Web Platform Installer
</p>
<img src="https://i.imgur.com/AxHCfQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Once you have installed Web Installer Platform open it. From inside the application you are going to install MySQL 5.5 Afterwards install x86 version of PHP up until 7.3. There are some failed files such as C++ redistributable package as well as PHP 7.3.8 and PHP Manager for IIS those files can be found with the install link.
</p>
<img src="https://i.imgur.com/JJ8bZeJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
</p>
<p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
</P>
<img src="https://i.imgur.com/TUGiSKi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
</p>
<p>
Open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
</p>
<img src="https://i.imgur.com/4AkTkV0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Go back into IIS manager and enable some extensions. To do this you have to go to Sites->Default->osTicket
Then double click on PHP manager. Click on "Disable or enable an extension" Enable "php_intl.dll" & "php_opcache.dll" then refresh the osTicket webserver and obsereve the changes "Intl Extension" should now be enabled. 
</p>
<img src="https://i.imgur.com/APZgUTT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php
Assign permissions to ost-config.php Disable inheritance->Removeall
New Permissions->Everyone->all
</p>
<img src="https://i.imgur.com/1nYaYGe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Afterwards continue setting up osTicket in the browser (click continue) then you will name the Helpdesk to your liking. Select a default email that will receive emails from customers who submit tickets. 
</p>
<img src="https://i.imgur.com/RmVk3q5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
<p>Continue Setting up osticket in the browser MySQL Database: osTicket MySQL Username: root MySQL Password: Password1 Click “Install Now!”
Congratulations, hopefully it is installed with no errors!
Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
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
