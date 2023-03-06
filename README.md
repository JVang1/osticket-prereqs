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
8. 
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Edit description.
</p>
<br />


<p>
9. 
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Edit description.
</p>
<br />
