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

- PHP manager for IIS - ensures PHP is correctly configured to run IIS
- Rewrite module - facilitates URL rewriting and redirect users to URLs
- VC_redist.x86 (redistributable) - osTicket utilizes Microsoft Visual C++ to ensure smooth operation
- MySQL - for storing data into databases
- HeidiSQL - interface for accessing MySQL

<h2>Installation Steps</h2>
First we will open Microsoft Edge and download the necesarry files to begin installation at <a href= https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD>osTicket-Installation-Files.zip</a>. Once downloaded find the folder, then right click and Extract All to your desktop for ease of access.
<p>
<p>
<img src="https://i.imgur.com/Y4sLyc0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will need to enable Internet Information Services. To do so utilize Windows search to find and open the Control panel, then select Programs -> Turn Windows features on or off, now navigate down to Internet Information Services and check the box to enable. We also need to enable CGI within the IIS which we can find by expanding Internet Information Services -> World Wide Web Services -> Application Development Features then check the box next to CGI to enable and click OK to save.
</p>
<br />

<p>
<img src="https://i.imgur.com/mcssxOL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now return back to the osTicket-Installation-Files folder and begin installing PHPManagerIIS_V1.5.0, rewrite_amd64_en-US, and VC_redist.x86
</p>
<br />

<p>
<img src="https://i.imgur.com/5C3nb8V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will need to create a new dierctory called C:\PHP, to do so open the C: drive within File Explorer and create a folder called PHP. We will now return to the osTicket-Installation-Files and extract the PHP zipped folder into the new directory C:\PHP 
</p>
<br />
<img src="https://i.imgur.com/VrLjpLe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will move on to install MySQL with Standard Configuration then create a username and password.
</p>
<br />
<img src="https://i.imgur.com/MDRAmC7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Next utilize Windows search and type IIS then Run as administrator. Open PHP Manager then register new PHP version under PHP setup and select C:\PHP\php-cgi.exe. Return to the home screen of IIS and restart the server on the right hand side of the application.
</p>
<br />
<img src="https://i.imgur.com/63lZDxi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Extract the osTicket-v1.15.8 from our Installation-Files folder and within the files move the "upload" folder into C:\inetpub\wwwroot, then rename the folder from upload to osTicket.
</p>
<br />
<img src="https://i.imgur.com/TgTW6Dh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Head back to IIS Manager and restart the server again. On the left panel you will want to expand Sites -> Default Web Site then click on osTicket and on the right panel click on Browse *:80 (http) which should open up the osTicket Installer webpage showing you a few missing extensions which we will install. Bring up your IIS again and open the PHP Manager within the osTicket Homepage then click enable or disable an extension under PHP Extensions and enable php_imap.dll, php_intl.dll and php_opcache.dll. Refresh the osTicket Installer webpage and the necessary extensions should now show a checkmark. 
</p>
<br />
<img src="https://i.imgur.com/gxJUQqn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Extract the osTicket-v1.15.8 from our Installation-Files folder and within the files move the "upload" folder into C:\inetpub\wwwroot, then rename the folder from upload to osTicket.
</p>
<br />
<img src="https://i.imgur.com/TgTW6Dh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Extract the osTicket-v1.15.8 from our Installation-Files folder and within the files move the "upload" folder into C:\inetpub\wwwroot, then rename the folder from upload to osTicket.
</p>
<br />
<img src="https://i.imgur.com/TgTW6Dh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
