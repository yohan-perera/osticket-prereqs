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

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/cc5ce6b7-d2c4-4360-adb1-a393242bfc68)
<p>
Create Resource Group
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/4783e6ba-dbc0-45e0-9e92-1b54caf4d950)
<p>
Create Windows 10 Virtual Machine (VM) with Virtual Network (Vnet)
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/e445c154-ed9c-42f8-a01a-5f2fc39cc3c1)
<p>
Establish RDP connection to VM-osTicket (Public IP Address)
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/500380d1-a659-4c36-9523-51783602f6b1)
<p>
Once RDP connection is established, install and enable ‘Internet Information Services’ using the ‘Turn Windows features on or off tool’. Expand ‘Web Development Tools’ and ensure ‘IIS Management Console’ is checked. Furthermore, expand ‘World Wide Web Services’, then expand ‘Application Development Features’ and ensure ‘CGI’ is checked. Finally expand ‘Common HTTP Features’ and ensure everything is checked.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/78a79cff-3742-494a-9359-3b2e7d3b4d63)
<p>
Navigage to localhost or loopback address (127.0.0.1) to verify that ‘Internet Information Services’ has been enabled and installed correctly. It should load the default ‘Internet Information Services’ infographic.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/e17d1ca0-8d64-4856-a726-2cf6c15b083e)
<p>
Install ‘PHP Manager for IIS’ (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/f339a510-f50b-4c69-9260-898fa37425b0)
<p>
Install ‘IIS URL Rewrite Module 2’ (rewrite_amd64_en-US.msi)
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/ca2f1ceb-587a-4537-beb7-0560c825cbf6)
<p>
Create directory for PHP in local storage (C:\PHP)
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/1e71be49-ebce-4023-8814-03b1b023fe38)
<p>
Download PHP 7.3.8 installation files (php-7.3.8-nts-Win32-VC15-x86.zip) and extract into ‘C:\PHP’
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/93fed4d7-9284-4637-81fe-b06f696c9580)
<p>
Install ‘VC_redist.x86.exe’
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/bd477c77-e5dc-41b8-bccd-457fa34d18ca)
<p>
Install MySQL Server 5.5 (mysql-5.5.62-win32.msi), ensuring ‘Typical’ installation setup is selected.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/92a51ed7-3383-4b6a-8d3f-35336c225368)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/309fec2c-471f-49f3-ae2c-cff0fb1e2354)
<p>
Launch the ‘MySQL Server Instance Configuration Wizard’ and enter appropriate configuration details before selecting ‘Execute’.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/c09e124f-4a87-41cb-b754-2e69f5d9576e)
<p>
Open ‘Internet Information Services (IIS) Manager’ as administrator, then open ‘PHP Manager’
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/04a5d9ed-4c64-4f2a-9574-9c1b2c5bafab)
<p>
Select ‘Register new PHP version’ and navigate to previously created ‘PHP’ folder, selecting ‘php-cgi.exe’, then restart server
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/0b2cf13b-7555-480b-aeed-cb42cc1ad119)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/abae85b7-ed91-4b67-be0a-d7da00d1971a)
<p>
Download osTicket installation files ‘osTicket-v1.15.8’, extract files, and copy ‘upload’ folder to ‘C:\inetpub\wwwroot’, after which rename ‘upload’ folder to ‘osTicket’ and restart server.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/ba2b93c6-c4b9-4e1d-88d5-911c8d5b8d1f)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/4762b795-4f06-4730-8be2-109a78b287ae)
<p>
Within ‘Internet Information Services (IIS) Manager’, navigate to ‘…\Sites\Default Web Site\osTicket’ and select ‘Browse *:80 (http). This should open a browser window instance of the osTicket Installer.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/d7d419e8-57e4-42ca-9adf-6d94f51c9f57)
<p>
Within ‘Internet Information Services (IIS) Manager’, navigate to ‘…\Sites\Default Web Site\osTicket’ and open ‘PHP Manager’, then select ‘Enable or disable an extension’.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/3b22d8db-2354-4e05-8ce1-671098fbf582)
<p>
Ensure ‘php_imap.dll’, ‘php_intl.dll’, and ‘php_opcache.dll’ are enabled.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/bbb99e91-3a3c-4ac9-8f3c-2f4e305b7563)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/20533da8-25f7-43ed-af48-9c178794fc08)
<p>
Navigate to ‘C:\inetpub\wwwroot\osTicket\include’ and rename ‘ost-sampleconfig.php’ to ‘ost-config.php’
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/8f36d5ac-eb71-4e56-b888-b32c08387af1)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/2b899a1e-761e-417d-9ba8-f0fb64469f6e)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/f7791375-7dc4-4a17-ae7e-e85aa33c4de0)
<p>
Edit ‘ost-config.php’ file permissions to ‘Disable inheritance’, then add permissions giving ‘Everyone’ full control over the file.</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/ff06e38a-d1d9-40b8-a169-b2ca59b5b53d)
<p>
Navigate to the osTicket Installer browser window and fill in appropriate details for the installer.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/3ec5ea73-b867-456a-9386-c618f3be714c)
<p>
Download and install HeidiSQL (HeidiSQL_12.3.0.6589_Setup.exe).
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/9a6c55ed-25b3-4b1f-a4cc-0d7245ee56f8)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/8e1a933a-4015-498c-a90d-98d61a8729df)
<p>
Open HeidiSQL and create new session to connect to MySQL server, inputting appropriate details.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/28a07dda-00e5-453e-a747-0242402f482e)
<p>
Create new ‘osTicket’ database in HeidiSQL.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/f18de6ea-8b53-4cfa-9c54-e585557c582c)
<p>
Finish inputting final details in osTicket Installer and click ‘Install Now’.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/09d5d0b5-e9b3-4b37-b3dc-b45ec6e36ae9)
<p>
Delete ‘C:\inetpub\wwwroot\osTicket\setup’.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/02b4f1a6-f474-4cee-beab-a71afebfd53f)
<p>
Navigate to ‘C:\inetpub\wwwroot\osTicket\include’ and set file permissions for ‘ost-config.php’ to read only.
</p>
<br />

![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/ee14ccbd-0328-44ed-9fdf-6468a0d4c403)
![image](https://github.com/yohan-perera/osticket-prereqs/assets/156178441/e9c2a566-b3f9-4578-8c0e-ad51e967eeff)
<p>
Navigate to ‘http://localhost/osTicket/scp/login.php’ and login with appropriate credentials to verify that osTicket has been installed correctly and allows us to log in.
</p>
<br />
