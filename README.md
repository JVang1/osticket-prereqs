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

- Create a [Microsoft Azure Tenant](https://portal.azure.com/)
- Sign up for a [Microsoft Azure Subscription](https://portal.azure.com/#view/Microsoft_Azure_SubscriptionManagement/SubscriptionCreateBlade)
- Create a [Resource Group](https://portal.azure.com/#create/Microsoft.ResourceGroup) under the subscription 
- Create a [Virtual Machine](https://portal.azure.com/#create/Microsoft.VirtualMachine-ARM) (Windows 10 with 2-4 Virtual CPUs) within the resource group
- [osTicket Installation Files](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

<h2>Installation Steps</h2>

<p>
1. Remote Desktop Connection
</p>
<img src="https://imgur.com/53e8bhq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remote Login into the Microsoft Azure virtual machine using its' Public IP address along with the username and password created.  
</p>
<br />


<p>
2. Install/Enable IIS with CGI
</p>
<img src="https://imgur.com/9rH6bXP.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the search bar, type and click on the "Turn Windows features on or off" program. Locate and turn on the "Internet Information Services" folder. Turn on and expand the "World Wide Web Services" and "Application Development Features" folders, then turn on the "CGI" folder and click "OK".        
</p>
<br />


<p>
3. From the osTicket Installation Files, download and install [PHP Manager for IIS](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view) (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />


<p>
4. From the osTicket Installation Files, download and install the [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view) (rewrite_amd64_en-US.msi)
</p>
<br />


<p>
5. Create the directory C:\PHP
</p>
<img src="https://imgur.com/5yyUWaN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using File Explorer, navigate to the Windows (C:) Drive. Once inside, right click and create a new folder named "PHP".
</p>
<br />


<p>
6. From the osTicket Installation Files, download [PHP 7.3.8](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view) (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip/extract the contents into "C:\PHP" folder. 
</p>
<img src="https://imgur.com/N0l3BvH.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
7. From the osTicket Installation Files, download and install [VC_redist.x86.exe](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view).
</p>
<br />


<p>
8. From the osTicket Installation Files, download and install [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view) (mysql-5.5.62-win32.msi)
</p>
<img src="https://imgur.com/shPZ6qT.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
During installation, Choose Setup Type "Typical". 
<p>  
</p>
<img src="https://imgur.com/VyejqjQ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>  
<p>  
Launch the MySQL Instance Configuration Wizard. 
<p>  
</p>
<img src="https://imgur.com/jyJjfFv.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>  
<p>   
Select "Standard Configuration". 
<p>  
</p>
<img src="https://imgur.com/o45UtOD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>  
<p>   
Set "Install As Windows Service". 
<p>  
</p>
<img src="https://imgur.com/BQXFjyt.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>  
<p>   
Create and enter the root password.   
</p>
</p>
<img src="https://imgur.com/fM1GMla.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>  
<p>   
Click on "Execute".   
</p>
<br />


<p>
9. Open and run Internet Information Services (IIS) as an Administrator.
</p>
<img src="https://imgur.com/I2YHQFu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
10. Register PHP from within Internet Information Services (IIS).
</p>
<img src="https://imgur.com/cC0lCnD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
From PHP Manager, click on "Register new PHP version". Provide a path "C:\PHP\php-cgi.exe" and click "OK". 
</p>
<br />


<p>
11. Reload IIS (Open IIS, Stop and Start the server)
</p>
<img src="https://imgur.com/b51REZa.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
12. From the osTicket Installation Files, download and install [osTicket v1.15.8](https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view).
</p>
<img src="https://imgur.com/KHNFlTi.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Extract and copy “upload” folder to c:\inetpub\wwwroot.
</p>
</p>
<img src="https://imgur.com/Q3VzmNG.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within c:\inetpub\wwwroot, rename folder “upload” to “osTicket”.
</p>
<br />


<p>
13. Reload IIS (Open IIS, Stop and Start the server)
</p>
<img src="https://imgur.com/b51REZa.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
14. From IIS, click on the drop down arrows for "Sites", then "Default Web Site". Click on folder "osTicket". On the right, click “Browse *:80(http)”.
</p>
<img src="https://imgur.com/V6EOgOQ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
15. Note that some extensions are not enabled.
</p>
<img src="https://imgur.com/uvvbg5b.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
</p>
<img src="https://imgur.com/uBdmiGZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to IIS, Sites -> Default Web Sites -> osTicket. Double-click on PHP Manager. Click “Enable or disable an extension”.
</p>
</p>
<img src="https://imgur.com/i3JUAgf.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>  
Enable: php_imap.dll, php_intl.dll, and php_opcache.dll.
</p>
</p>
<img src="https://imgur.com/Qhg9swS.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Refresh the osTicket site in the browser and observe the changes.
</p>
<br />


<p>
16. Rename: ost-config.php
</p>
<img src="https://imgur.com/qmQ5mTj.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
</p>
</p>
<img src="https://imgur.com/zOFRs8I.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>  
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />


<p>
17. Assign Permissions: ost-config.php
</p>
<img src="https://imgur.com/JyC5LWu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right-click "ost-config.php" file and click on "Properties". Click on "Security" tab, then "Advanced". Click on "Disable inheritance" -> "Remove all
inherited permissions from this object".
</p>
</p>
<img src="https://imgur.com/8fYKht1.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on "Add". Click on "Select a principal", enter object name "Everyone", then click "OK". 
</p> 
</p>
<img src="https://imgur.com/JyC5LWu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p> 
 -> All  
</p>
<br />


<p>
18. 
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Edit description.
</p>
<br />


<p>
19. 
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Edit description.
</p>
<br />


<p>
20. 
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Edit description.
</p>
<br />


<p>
21. 
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Edit description.
</p>
<br />


<p>
22. 
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Edit description.
</p>
<br />
