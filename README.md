# Hardening an Enviornment

<h2>Description</h2>

This project focused on fortifying security infrastructure by strategically utilizing languages and utilities such as KQL, Azure Log Analytics, and Azure Network Security Groups. The walk-through elucidates a meticulous incident review process within Azure Sentinel, demonstrating the efficacy of KQL queries and visualizations in uncovering patterns associated with attacking IP addresses. A specific incident involving a brute force attempt on a Windows VM is detailed, outlining anomaly detection and subsequent remediation steps. The project culminates with implementing NIST SP 800-53 security policies in Azure and blocking non-permitted IP addresses.
<br />

<h2>Languages and Utilities Used</h2>
- <b>KQL</b><br />
- <b>Azure Log Analytics</b><br />
- <b>Azure Virtual Machines</b><br />
- <b>Azure Network Security Groups</b><br />

<h2>Environments Used </h2>

- <b>Azure</b> 

<h2>Walk-through:</h2>

<p align="left">
Review Report: <br/>
<img src="https://i.imgur.com/PrMNYHm.png"/><br />
Azure Sentinel will create reports anytime your KQL queries are found in log analytics. Once you click on the event, you can use visual mode security analysts to graphically represent data, creating charts and graphs that showcase the activities of attacking IP addresses over time. These visualizations aid in identifying trends, patterns, and correlations that may be challenging to discern from raw log data.
<br />
<br />

Determining the Issue:<br />
<img src="https://i.imgur.com/3PrDg2G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
CUSTOM: Brute Force ATTEMPT - Windows<br />
Incident ID: 15
<br /><br />
There were 11 events triggered. 11 events are highly strange as most people get their log-in within three attempts. 141.98.11.170 This IP is not associated with any other login attempts.
<br /><br />
He potentially compromised “windows-vm” which involves several other incidents. This can be due to possible overexposure to Public Internet.
<br /><br />
The attacker was not able to gain access to the machine. Will block Ip address and check firewall permissions for “windows-vm”
<br /><br />
Remedies:
First, I isolated VM by turning off the machine through Azure. Then, I reset the password for the user so they could create a more secure password. Then I investigated how the attacker was able to get in and determined the Vm firewall was not strong enough, so I will analyze the firewall and harden it only to be permitted to route traffic to the server’s HTTPS port (443/TCP)

<br />
<br />

Implementing NISTc:<br />
<img src="https://i.imgur.com/oDoQxVW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Implementing NIST SP 800-53 security policies in Azure configures security controls, access management, and compliance measures to align with the comprehensive security framework outlined by the National Institute of Standards and Technology (NIST). This ensures that firewall settings align with the comprehensive framework, enhancing the effectiveness of Azure's firewalls in addressing cybersecurity requirements, access management, and compliance measures specified by NIST SP 800-53.

<br />
<br />


Summary:  <br/>
This project exemplifies a proactive and systematic approach to cybersecurity within the Azure environment. Leveraging powerful tools such as KQL, Azure Log Analytics, and Azure Sentinel, security analysts were able to not only identify and remediate specific incidents but also implement broader security measures aligned with NIST SP 800-53 standards. This project showed multiple ways to decrease brute force attacks. The walk-through provides a tangible example of incident response, showcasing the importance of continuous monitoring, analysis, and adherence to established security frameworks in safeguarding Azure resources against potential threats.
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
