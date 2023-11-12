<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>

<p>This tutorial provides a step-by-step guide to the prerequisites and installation of the open-source help desk ticketing system osTicket.</p>

<h2>Environments and Technologies Used</h2>

<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Internet Information Services (IIS)</li>
</ul>

<h2>Operating Systems Used</h2>

<ul>
  <li>Windows 10 (21H2)</li>
</ul>

<h2>List of Prerequisites</h2>

<ul>
  <li>Azure Virtual Machine</li>
  <li>Internet Information Services (IIS)</li>
  <li>PHP Manager</li>
  <li>Rewrite Module</li>
  <li>VC Redist</li>
  <li>MySQL</li>
  <li>Heidi SQL</li>
  <li>osTicket v1.15.8</li>
</ul>

<p>Link to downloads: <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Downloads</a></p>

<h2>Installation Steps</h2>

<ol>
  <li>Create a virtual machine on <a href="https://portal.azure.com/">Azure Portal</a> with Windows 10 Pro, version 22H2, using at least 2 vCPUs and 16 GBs of memory.</li>

  <li>Connect to the virtual machine using the Remote Desktop Connection app, using the public IP address.</li>

  <li>In the Control Panel, open Programs and select "Turn Windows features on and off."</li>
  
  <li>Install/enable IIS in Windows with CGI and Common HTTP Features:
    <ul>
      <li>World Wide Web Services -> Application Development Features -> [X] CGI [X] Common HTTP Features</li>
    </ul>
  </li>

  <li>Check IIS installation by accessing 127.0.0.1 in a browser.</li>

  <li>Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) and the Rewrite Module (rewrite_amd64_en-US.msi).</li>

  <li>Create a folder in C drive called PHP. Download PHP 7.3.8 and unzip it into C:\PHP.</li>

  <li>Download and install VC_redist.x86.exe from the installation files.</li>

  <li>Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi), setting the root password to "Password1."</li>

  <li>Register PHP in IIS using PHP Manager, pointing to the php-cgi.exe file in C Drive -> PHP.</li>

  <li>Install osTicket v1.15.8 by downloading from the Installation Files, extracting, and copying the "upload" folder to c:\inetpub\wwwroot, renaming it to "osTicket."</li>

  <li>In IIS, go to sites -> Default -> osTicket, click "Browse *:80," and enable necessary extensions in PHP Manager.</li>

  <li>Rename ost-sampleconfig.php to ost-config.php, set file permissions, and restart IIS.</li>

  <li>Continue osTicket setup in the browser, install HeidiSQL, create a new session with username "root" and password "Password1."</li>

  <li>Create a new database named osTicket in HeidiSQL, fill in database settings in the browser, and clean up the setup folder in C:\inetpub\wwwroot\osTicket.</li>

  <li>Login to osTicket on the browser to complete the setup.</li>
</ol>

<p>Congratulations! You have successfully installed and set up osTicket!</p>
