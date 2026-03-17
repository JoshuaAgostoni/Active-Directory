<h1>Active Directory Lab</h1>



<h2>Description:</h2>
This project demonstrates the design and deployment of a secure Active Directory (AD) environment used for security testing, logging, and attack simulation. The environment was manually configured to showcase applied knowledge of <b>Identity and Access Management (IAM)</b>, network service hardening, and the attacker-defender lifecycle within a virtualized setting. All supporting evidence screenshots are located in the /screenshots folder within the GitHub repository.


<h2>2.	Architecture Components:</h2>

* <b>VirtualBox Host-Only / NAT Network:</b> Isolated environment for safe vulnerability testing and network segmentation.
* <b>Domain Controller (DC01):</b> Windows Server 2022 running AD DS and DNS services.
* <b>Client Workstation (Client01):</b> Windows 10 Enterprise joined to the CyberLab.local domain.
* <b>Attacker Node:</b> Kali Linux instance used for network reconnaissance and vulnerability scanning.
* <b>Logging:</b> Sysmon and Windows Event Logs configured for forensic capability and monitoring.

 


<h2>Environments Used: </h2>

<b>Windows Server 2022 VM - Kali Linux VM - Windows 10 WorkStation VM</b>

<h2>Program walk-through:</h2>

<p align="center">
 <br/>
Shows the Creation of the Home Lab Active Directory Network.
 <br/>
<a href="https://imgur.com/OB7Q8WW"><img src="https://i.imgur.com/OB7Q8WW.png" title="source: imgur.com" /></a>
<br />
<br />
Displays the selection of Windows Server 2022 Standard Evaluation (Desktop Experience), ensuring a full GUI for administrative management. <br/>
<a href="https://imgur.com/ej6UzdA"><img src="https://i.imgur.com/ej6UzdA.png" title="source: imgur.com" /></a>
<br />
<br />
Shows the deployment of the new forest CyberLab.local, demonstrating the ability to configure root domain infrastructure and DNS zones.
<a href="https://imgur.com/Fn9UrVN"><img src="https://i.imgur.com/Fn9UrVN.png" title="source: imgur.com" /></a>
<br />
<br />
Shows the creation of the new user Victim.  <br/>
<a href="https://imgur.com/pQB8ZsZ"><img src="https://i.imgur.com/pQB8ZsZ.png" title="source: imgur.com" /></a>
<br />
<br />
Shows manual configuration of the client's IPv4 properties to use the Domain Controller's IP address (192.168.10.4) as the Preferred DNS server. <br/>
<a href="https://imgur.com/e2EPhR2"><img src="https://i.imgur.com/e2EPhR2.png" title="source: imgur.com" /></a>
<br />
<br />
Displays the "Welcome to the CyberLab.local domain" confirmation on the Windows 10 workstation, verifying successful DNS resolution and LDAP authentication.  <br/>
<a href="https://imgur.com/1abgL4q"><img src="https://i.imgur.com/1abgL4q.png" title="source: imgur.com" /></a>
<br />
<br />
This image verifies the final deployment of a Windows 10 "Victim" workstation within the VM VirtualBox environment.
<a href="https://imgur.com/BBZbkZe"><img src="https://i.imgur.com/BBZbkZe.png" title="source: imgur.com" /></a>
<br />
  <br/>
Demonstrates the use of Responder on Kali Linux to perform LLMNR and mDNS poisoning, successfully intercepting an NTLMv2-SSP authentication hash from a domain user.
<a href="https://imgur.com/iL29k7Q"><img src="https://i.imgur.com/iL29k7Q.png" title="source: imgur.com" /></a>
<br />
<br />
Shows John the Ripper was used to successfully decrypt the previously captured NTLMv2 hash.
<a href="https://imgur.com/z1gVp4q"><img src="https://i.imgur.com/z1gVp4q.png" title="source: imgur.com" /></a>


<h2>7.	Security Principles Demonstrated</h2>

* <b>Identity & Access Management (IAM):</b> Centralized authentication and restricted permissions via Active Directory.
*	<b>Network Segmentation:</b> Isolated lab environment to prevent lateral movement to host systems.
*	<b>Principle of Least Privilege:</b> Utilizing specific DSRM and Administrative credentials for distinct tasks.
*	<b>Continuous Monitoring:</b> Baseline logging of Windows Event Logs for security auditing and threat detection.
*<b>Data Protection:</b> Ensuring secure configuration of directory services and access restriction.

