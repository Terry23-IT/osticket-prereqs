# osticket-prereqs<p align="center">
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

- Computer or laptop
- Internet Connection
- Microsoft Azure

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/94f082ca-33c2-4869-a2c9-52cf43e25cf4)

In Microsoft Azure i created a virtual machine called osticket-vm on a windows 10 image and used 2vcpus for fast connection 
</p>
<br />
<br />

![image](https://github.com/user-attachments/assets/ee72a991-f5f5-470e-a2de-0a957b034ce4)

After creating the osTicket Azure virtual machine  I opened up remote desktop and put the os-ticket ip-address to open the virtual machine on my personal computer. Then I downloaded the osTicket-Installation-Files on the virtual machine
</p>
<br />
<br />

![image](https://github.com/user-attachments/assets/e291f3ff-80f6-4ce5-b45c-0188d6fd97db)

Within the virtual machine I opened the  folder for os ticket and dragged it onto the screen, right clicked on it and clicked on extract all. Theres going to be anothoer folder (probably under the recycle bin icon) that looks extracted. Take the floder that's not extracted asnd put it in the trash icon. Now to start the enable of IIS, cilck on the start and type control panel, within the control panel go to programs(unistall a progam in this case were adding a program) click the check box for Internet Information Servcices and expand it, then expand World Wide Web service, and expand Application Development Features, click on CGI and say ok
</p>
<br />
<br />

![image](https://github.com/user-attachments/assets/cac55177-683f-40eb-8730-b1358e643e5c)

within the osticket folder I used the files from OS ticket documentation aggregated them all(copied and pasted into a folder within the osTicket-installation-files)

 From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP

From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Username: root
Password: root

</p>
<br />
<br />

![image](https://github.com/user-attachments/assets/f86973ff-0bed-4c98-bfe4-5aa3d9c169c8)

Open IIS as an Admin from the start icon
(dont forget to click run as admin)

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

Reload IIS (Open IIS, Stop and Start the server)

Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”

</p>
<br />
<br />

![image](https://github.com/user-attachments/assets/da918554-93cc-4fa5-9dbc-f8bdd70164a7)

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

</p>
<br />
<br />

![image](https://github.com/user-attachments/assets/0222f076-9eac-4fcf-803f-df1c245509a5)

Rename: ost-config.php from ost-sampleconfig.php

From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
Disable inheritance -> Remove All(Remove all inherited permissions from the object)


New Permissions -> Everyone -> All
make sure the basic permissions have full control before continuing 
Then click apply

</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<br />
