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

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- A valid Azure subscription.
- Remote desktop access to Azure VM.
- Internet Information Services (IIS) enabled on Windows.
- Necessary installation files for osTicket and dependencies.
- Basic understanding of Windows server administration.

<h2>Installation Steps</h2>

<h3>Part 1: Creating a Virtual Machine in Azure</h3>
<ul>
    <li>Created a Resource Group in Azure.</li>
    <li>Created a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs.
        <ul>
            <li>Allowed the creation of a new Virtual Network (Vnet) during VM setup.</li>
        </ul>
    </li>
</ul>

<h3>Part 2: Installation Steps</h3>
<ul>
    <li><strong>Set Up Azure Virtual Machine:</strong>
        <ul>
            <li>Created an Azure VM named "Vm-osticket" with Windows 10, 4 vCPUs.</li>
            <li>Set the username as "labuser1" and the password as "Qwerty123456789".</li>
        </ul>
    </li>
    <li><strong>Access Installation Files:</strong>
        <ul>
            <li>Used provided installation files for osTicket and its dependencies.</li>
        </ul>
    </li>
    <!-- Add other installation steps here in similar format -->
</ul>

<h3>Installing and Enabling IIS in Windows with CGI and Common HTTP Features:</h3>
<!-- Remaining Installation Steps -->

<h3>Install Additional Components:</h3>
<ul>
    <li>Downloaded and installed PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi).</li>
    <li>Downloaded and installed the Rewrite Module (rewrite_amd64_en-US.msi).</li>
</ul>

<h3>Set Up PHP:</h3>
<ul>
    <li>Created a directory at C:\PHP.</li>
    <li>Unzipped PHP 7.3.8 into C:\PHP.</li>
    <li>Installed VC_redist.x86.exe.</li>
    <li>Installed MySQL 5.5.62 with typical setup and standard configuration, using "Qwerty123456789" as the password.</li>
</ul>

<h3>Configure IIS:</h3>
<ul>
    <li>Opened IIS as an Admin.</li>
    <li>Registered PHP within IIS.</li>
    <li>Reloaded IIS (stopped and started the server).</li>
</ul>

<h3>Install osTicket:</h3>
<ul>
    <li>Downloaded osTicket v1.15.8 and extracted it to c:\inetpub\wwwroot.</li>
    <li>Renamed the "upload" folder to "osTicket".</li>
    <li>Reloaded IIS.</li>
</ul>

<h3>Configure osTicket:</h3>
<ul>
    <li>Checked and enabled necessary PHP extensions in IIS (php_imap.dll, php_intl.dll, php_opcache.dll).</li>
    <li>Renamed ost-sampleconfig.php to ost-config.php in the osTicket include directory.</li>
    <li>Assigned full access permissions to ost-config.php for Everyone.</li>
</ul>

<h3>Complete osTicket Setup:</h3>
<ul>
    <li>Named the Helpdesk and set a default email.</li>
    <li>Installed HeidiSQL and set up a database named “osTicket”.</li>
</ul>

<h3>Finalize Installation:</h3>
<ul>
    <li>Completed the osTicket setup in the browser with MySQL details.</li>
    <li>Clicked “Install Now!” and verified successful installation.</li>
    <li>Accessed the help desk login page at <a href="http://localhost/osTicket/scp/login.php">http://localhost/osTicket/scp/login.php</a>.</li>
    <li>Provided the end users with the osTicket URL: <a href="http://localhost/osTicket/">http://localhost/osTicket/</a>.</li>
</ul>

<h3>Clean-Up Steps:</h3>
<ul>
    <li>Deleted the "setup" directory in C:\inetpub\wwwroot\osTicket.</li>
    <li>Set the permissions of ost-config.php to "Read" only.</li>
</ul>

