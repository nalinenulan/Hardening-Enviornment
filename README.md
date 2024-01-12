# Hardening-Enviornment

<h2>Description</h2>

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
Azure Sentinel will create reports anytime your KQL queries are found.  
<br />
<br />

Delete Strong Network Security Rule:<br />
<img src="https://i.imgur.com/3PrDg2G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
 In typical network security guidelines, and strong rules are implemented to enhance the overall security posture by controlling and restricting network traffic based on predefined policies. The objective of deleting or disabling these strong security rules is to simulate a scenario where critical security measures are intentionally weakened or compromised. This step allows me to assess how the network behaves when subjected to intentional vulnerabilities. It helps in identifying potential risks, vulnerabilities, and understanding the impact of weakened security configurations.
<br />
<br />


Create a Log for Incoming Traffic:<br />
<img src="https://i.imgur.com/oDoQxVW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Create a data collection rule within the Azure environment. In the context of a honeynet, data collection rules are essential components designed to capture and log various types of network activities, system events, and potential security incidents. The data collection rule may include configurations for logging network traffic, system logs, application-level events, or any other relevant information that can provide insights into the activities of potential adversaries. I will capture System logs and logging attempts by specifically focusing on login attempts. The honeynet can closely monitor authentication activities, detect suspicious login patterns, and identify potential unauthorized access attempts.

<br />
<br />


Summary:  <br/>
This cybersecurity project employs a honeynet setup with virtual machines running Linux and Windows to explore cybersecurity scenarios across different operating systems. The deliberate deletion of strong network security rules simulates intentional vulnerabilities, allowing for the assessment of network behavior under weakened security configurations. The creation of data collection rules within the Azure environment enables the capture and logging of various network activities and system events, with a focus on monitoring login attempts. Finally, the review of logs on a Log Analytics workspace provides centralized analysis and visualization, emphasizing the importance of monitoring and maintaining system security. The project contributes valuable insights into potential risks, vulnerabilities, and the impact of intentional security compromises.
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
