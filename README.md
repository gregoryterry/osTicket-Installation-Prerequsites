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

<h2>List of Installation Steps</h2>

- Part 1 (Create Virtual Machine in Azure)
- Part 2 (Install osTicket Prerequisites)
- Part 3 (Install osTicket)
- Part 4 (osTicket Post Installation Setup)
- Part 5 (Tickets and Ticket Lifecycle)


<h2>osTicket Prerequisites Installation Steps</h2>
<p> Part 1 (Create Virtual Machine in Azure)

<p> <img src="https://i.imgur.com/nnklcHH.png" height="60%" width="60%" alt="Part 1 (Create Virtual Machine in Azure)"/>
<p>

<br />

</p>
<br />

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

<p> When validation passes, create.  Azure will display the components that are being created during deployment.
<p>
<img src="https://imgpile.com/images/h3JJhS.md.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p> Here we see the new osTicket VM, click on it to view the details.
<p>
<img src="https://imgpile.com/images/h3JQ9g.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p> Log on to the osTicket VM using the public IP address.  Use RDP to logon with the username and password of the osTicket VM.
<p>
<img src="https://imgpile.com/images/h3Jv6N.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>


<p> Part 2 (Install osTicket Prerequisites)
<p>

<p> On the osTicket VM, open search and search for “Turn Windows features on and off”
<p>
<img src="https://imgpile.com/images/h3Jjeo.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<p>
 <p> Select IIS, Internet Information Services > Expand down to CGI > World wide web > Application developer > check CGI select > ok
<p>
<img src="https://imgpile.com/images/h3PTju.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p> Test the Web Server by typing 127.0.0.1 in your web browser.  You should get the IIS page
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

<p> select typical installation > select launch config wizard > Select standard configuration > install as Windows Service
<p>
<img src="https://imgpile.com/images/h3YIGr.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3YuHR.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3Y7pg.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<img src="https://imgpile.com/images/h3YUbc.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<p> Enter username and root password for SQL: 
<p>

<img src="https://imgpile.com/images/h3YbY1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

