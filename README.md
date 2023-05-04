# osTicket-Installation-Prerequisites
In This lab I will download and install osTicket and the necessary pre-installation software programs required to install osTicket.

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

<h3>List of Installation Steps</h3>

- Part 1 (Create Virtual Machine in Azure)
- Part 2 (Install osTicket Prerequisites)
- Part 3 (Configure IIS)
- Part 4 (Install osTicket)
- Part 5 (Download and HeidiSQL and install)


<h2>osTicket Prerequisites Installation Steps</h2>

<h3>Part 1 (Create Virtual Machine in Azure)</h3>

<p> <img src="https://i.imgur.com/nnklcHH.png" height="60%" width="60%" alt="Part 1 (Create Virtual Machine in Azure)"/>
<p>

<p>
<img src="https://i.imgur.com/sODoms9.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>

<p> Select a username and password
<p>
<img src="https://imgpile.com/images/h3Mxb2.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

</p> Select the default disk settings
<p>
<img src="https://imgpile.com/images/h3MLto.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p> Accept the default network settings
<p>

<img src="https://imgpile.com/images/h3JnUa.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p>
Make sure RDP 3389 is selected
<p>
<img src="https://imgpile.com/images/h3JTzN.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3JbvW.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p>
Select review and create
<p>

<img src="https://imgpile.com/images/h3JbvW.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p> When validation passes, create.
Azure will display the components that are being created during deployment.
<p>
<img src="https://imgpile.com/images/h3JJhS.md.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p> Here we see the new osTicket VM, click on it to view the details.
<p>
<img src="https://imgpile.com/images/h3JQ9g.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p> Log on to the osTicket VM using the public IP address.
Use RDP to logon with the username and password of the osTicket VM.
<p>
<img src="https://imgpile.com/images/h3Jv6N.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>

<h3>Part 2 (Install osTicket Prerequisites)</h3>

<p> On the osTicket VM, open search and search for
<b>“Turn Windows features on and off”</b>
<p>
<img src="https://imgpile.com/images/h3Jjeo.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<p>
 <p> Select IIS, Internet Information Services >
 Expand down to CGI > World wide web > Application developer >
 check CGI select > ok
<p>
<img src="https://imgpile.com/images/h3PTju.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p> Test the Web Server by typing 127.0.0.1 in your web browser.
You should get the IIS page.
<p>
<img src="https://imgpile.com/images/h3PKuX.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p> Download and Install PHP Manager for IIS_v15.0 msi
<p>
<img src="https://imgpile.com/images/h3PPjr.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p> Download / install the Rewrite Module (rewrite_amd64_en-Us msi)
<p>

<img src="https://imgpile.com/images/h3PmfW.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p> Create the directory ‘c:\PHP’ on the local hard drive of the VM
<p>
<img src="https://imgpile.com/images/h3P871.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p> Download PHP 7.3.8  /  unzip to c:\PHP
<p>
<img src="https://imgpile.com/images/h3PXLx.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>

<p> Download and install VC redst x86.exe 
<p>
<img src="https://imgpile.com/images/h3PqDo.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>

<p> Download and Install MySQL 5.5.62 msi 
<p>
<img src="https://imgpile.com/images/h3P2XC.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>

<p> select typical installation > select launch config wizard >
Select standard configuration > install as Windows Service
<p>
<img src="https://imgpile.com/images/h3YIGr.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3YuHR.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3Y7pg.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3YUbc.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p> Enter username and root password for SQL: 
<p>

<img src="https://imgpile.com/images/h3YbY1.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p>Execute > Finish 
<p>
<img src="https://imgpile.com/images/h3pU91.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://imgpile.com/images/h3pYcu.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>


<h3>-Part 3 (Configure IIS)</h3

<p>Open IIS as an Admin
<p>
 <img src="https://imgpile.com/images/h3p3Bo.pn" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
 <p>Open PHP Manager
<p>
 <img src="https://imgpile.com/images/h3SIFu.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
 
 <p>Register new PHP version
 Browse to the PHP execution file (php-cgi.exe)
Click on the server and select restart on the Actions pane
<p>
<img src="https://imgpile.com/images/h3SCFr.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3StJg.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3SxLc.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<h3>-Part 4 (Install osTicket v1.15.8)</h3

<p>download osTicket
extract and copy the “upload” folder to “c:\inetpub\wwwroot”
within c:\inetpub\wwwroot, rename “upload” to “osTicket”
<p>
<img src="https://imgpile.com/images/h3SEmh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>Copy the ‘upload’ folder to “c:\inetpub\wwwroot”
<p>
<img src="https://imgpile.com/images/h3ZnHW.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p> 
rename the folder to “osTicket”
<p>
<img src="https://imgpile.com/images/h3ZNgx.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p>Reload IIS (Open IIS, Stop and Start the server)
<p>
<img src="https://imgpile.com/images/h67M6g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p>Go to sites --> Default website  --> osTicket
On the right, click “Browse *:80 (http)”
<p>
<img src="https://imgpile.com/images/h67mjx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p>If you see the following page in the web browser,
osTicket was successfully installed.
<p>
<img src="https://imgpile.com/images/h67of8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p>Some extensions are not enabled, to enable:
Go to IIS > sites > default > osTicket
Double-click PHP Manager
Click “enable or disable an extension”
Enable the following extensions:
Php_imap.dll
Php_intl.dll
Php_opchche.dll
<p>
<img src="https://imgpile.com/images/h67Au3.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<p>Refresh the IIS browser to see that the extensions are enabled [view > refresh]
All selected extensions should be enabled.
<p>
<img src="https://imgpile.com/images/h67kjF.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p>Rename ‘ost-config.php’
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To:      C:\inetpub\wwwroot\osTicket\include\ost-config.php
<p>
<img src="https://imgpile.com/images/h67BXu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://imgpile.com/images/h67FEk.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>  Assign the following Permissions for ost-config.php
Disable inheritance > Remove all
New Permissions > Everyone > all

Right-click ost-config.php > properties > security tab > advanced
<p>
<img src="https://imgpile.com/images/h67eDE.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p>Disable inheritance
<p>
<img src="https://imgpile.com/images/h6NRGx.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>Remove all
<p>
<img src="https://imgpile.com/images/h6Nbpo.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>Advanced > Add
<p>
<img src="https://imgpile.com/images/h6N9lS.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>Select principal
<p>
<img src="https://imgpile.com/images/h6NCQ8.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>Select a user group:  Everyone  >  check names  >  ok
<p>
<img src="https://imgpile.com/images/h6N2dR.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>Select full control
<p>
<img src="https://imgpile.com/images/h6NLgc.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>Apply > ok > ok
<p>
<img src="https://imgpile.com/images/h6NkUN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p>Continue the osTicket setup in the web browser
Select continue
<p>
<img src="https://imgpile.com/images/h6NWkP.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>Fill out the  fields for “System Settings and "Admin User" 
***** Do not install or fill out the Database section yet,
HeidiSQL must be installed first.
<p>
<img src="https://imgpile.com/images/h6NFn1.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://imgpile.com/images/h6Ngox.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://imgpile.com/images/h6NvSj.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>


<h3> Part 5 (Download and HeidiSQL and install)</h3

<p>Download HeidiSQL and install
<p>
<img src="https://imgpile.com/images/h6NErC.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://imgpile.com/images/h6NpgS.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>Now create a new database
select:  new
<p>
<img src="https://imgpile.com/images/h6NZU8.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>Username: root 
Password:: xxxxxxxxxxxx
***Remember this username and password
select: open
<p>
<img src="https://imgpile.com/images/h6Nek3.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>This is the connection to the SQL server
<p>
<img src="https://imgpile.com/images/h6U4xw.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>Go back to the browser and fill in the “Database settings” section using the credentials from HeidiSQL
*** Do not install yet.
<p>
<img src="https://imgpile.com/images/h6UnoF.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>Create a database named osTicket
right-click Unnamed > Create new > Database
<p>
<img src="https://imgpile.com/images/h6U7rk.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>Name: osTicket > ok
<p>
<img src="https://imgpile.com/images/h6UNvM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>Go back to your browser > enter the database name you just created “osTicket” and select install now.
<p>
<img src="https://imgpile.com/images/h6Uww4.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>If you see this page, your installation was successful!
<p>
<img src="https://imgpile.com/images/h6UR0G.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>It’s time to clean up installation files, select the setup folder
in the location below and delete it. 
<p>
<img src="https://imgpile.com/images/h6UdxX.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>Set permissions to read-only for ‘ost-config.php’,
located at “c>\inetpub\wwwroot\osTicket\include\ost-config.php”
right-click > properties > security > advanced
<p>
<img src="https://imgpile.com/images/h6Ulhj.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>select: everyone > edit > read & execute and read > apply > ok
<p>
<img src="https://imgpile.com/images/h6UEeh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://imgpile.com/images/h6Uycc.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>Test the URLs used  for the admin and the client to login to osTicket
In your web browser, enter this URL to Browse to the help desk login page:  http://localhost/osTicket/scp/login.php
this is the admin login
<p>
<img src="https://imgpile.com/images/h6w56o.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>The Admin portal works!
<p>
<img src="https://imgpile.com/images/h6wTRC.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>This is the URL used for end-users to logon and create tickets, “http://localhost/osTicket/”
 Make sure both of these URLs direct you the correct login page for osTicket
<p>
<img src="https://imgpile.com/images/h6wdB8.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>In the next tutoral I will perform the proceedure
for osTicket post installation configuration
<p>





