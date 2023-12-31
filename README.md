<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- (PHPManagerForIIS_V1.5.0.msi)
- (rewrite_amd64_en-US.msi)
- (php-7.3.8-nts-Win32-VC15-x86.zip)
- VC_redist.x86.exe
- (mysql-5.5.62-win32.msi)
- osTicket v1.15.8
- HeidiSQL_12.3.0.6589_Setup.exe

<h2>Installation Steps</h2>

![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/41593889-ca4c-4ac6-9037-caa987cb952a)

- Go to Control Panel
- Select Programs
- Turn windows features on or off
- Enable Internet Information Services (IIS is the server that osTicket runs in)

<br />

![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/0af5c476-29ad-4c92-b94e-7f1fa0708020)

- Expand World Wide Web Services
- Expand Application Development
- Enable CGI
<br />

![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/9d14d055-60aa-42d4-970e-c3aa018897ae)

- Collapse Application Development
- Expand Common HTTP Features
- Ensure all services under Common HTTP Features are enabled

<br />

![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/bbd43b29-9eb6-4444-b4ac-90873f2381ef)

- Collapse World Wide Web Services
- Expand Web Management Tools
- Ensure IIS Managment Console is enabled
- Select Ok to begin installation
<br />

- Download and Install PHP Manager for IIS 
- Download and Install Rewrite Module

<br />

![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/8a1b9d7c-ce51-4450-8e5c-cfef8855a769)

- Create directory C:\PHP
- Download PHP 7.3.8
- Unzip contents into C:\PHP

![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/c27a0e0f-e405-4a28-9006-bbc2f6b89180)

- Download and Install VC_redist.x68.exe
- Download and Install MySQL
- Typical Setup
- Launch configuraion Wizard
- Standard Configuration
- Install as Windows Service
- Create Password (you will need this later during osTicket registration)
  
<br />

- Open IIS as administrator
- Double Click PHP Manager
![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/1de98877-9a50-4c25-a48c-26a3aa4982c5)
- Click Register new PHP version
- Provide path to php executable file which is in the PHP folder you created
![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/4d9fddef-e32d-4157-a9ee-177cb0f95b0f)
- Select OK
- Restart IIS server
![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/4f52912a-19e7-40d0-be4e-0c755dd17840)
- Install osTicket
- Extract and copy "upload" folder to c:\inetpub\wwwroot
![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/39e04966-9e2b-4c22-99c1-9062f7f092ee)
- Within c:\inetpub\wwwroot rename "upload" to "osTicket"
- Restart IIS server
- Expand sites
- Expand Default Web Site
- Select osTicket
- Click "Browse *:80"
![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/e1d9142c-4e02-4f79-b98c-7b58ad380515)
- You'll note not all extensions are enabled
- Return to IIS Manager, and double click PHP Manager
![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/86873285-3022-4282-a83a-619e326e3a80)
- Select "Enable or disable an extension"
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache
- Refresh osTicket in your browser and observe the changes
- Go to c:\inetpub\wwwroot\osTicket\include
- Rename "ost-sampleconfig.php" to "ost-config.php"
- Assign new permissions in "ost-config.php"
- 1st disable inheritance (remove all)
- Then set full control permissions for everyone
- Continue setting up osTicket in the browser
- Fill out System Setting and Admin User
- Before continuing with Database settings, download and install HeidiSQL
- Open Heidi SQL and create a new session
![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/e96b0bd0-bb2b-492a-90f8-a42350e82289)
- User: root
- Password: Password1
- Select Open
- Right click  and select create new database
- Name it "osTicket"
- Return to osTicket in the browser and fillout Database settings
- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: Password1
- Click "Install Now"
- osTicket should now be installed
- Delete c:\inetpub\wwwroot\osTicket\setup
- Set permissions to read only for c:\inetpub\wwwroot\osTicket\include\ost-config.php

<br />
