<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

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
- https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe

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

- Download and Install PHP Manager for IIS https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link
- Download and Install Rewrite Module https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link

<br />

![image](https://github.com/JordanDanielWest/osticket-prereqs/assets/96628562/8a1b9d7c-ce51-4450-8e5c-cfef8855a769)

- Create directory C:\PHP
- Download PHP 7.3.8 https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link
  

<br />
