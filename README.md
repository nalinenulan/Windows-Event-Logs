# Windows EventLogs

<h2>Description</h2>
This project involves a deliberate exploration of the security implications associated with turning off the Windows firewall. The individual conducting the experiment created an attacker machine on a separate server and attempted unauthorized access to a Windows Virtual Machine (VM) using incorrect credentials. The primary objective was to assess the significance of firewalls in preventing unauthorized access and protecting against potential attackers.
<br />

<h2>Languages and Utilities Used</h2>
- <b>Windows Defender</b><br />
- <b>Windows Event Viewer</b>

<h2>Environments Used </h2>

- <b>Windows</b> 

<h2>Walk-through:</h2>

<p align="left">
Turn off Firewall: <br/>
<img src="https://i.imgur.com/ARgEcl0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Turning off the Windows firewall is best to get as many attackers as possible. Turning off the firewall can be done by going to Windows Defender. Then click on "Windows Defender Firewall Properties," navigate to the public profile, and turn the firewall off. WARNING: firewalls should be turned on for most computers. My computer is on a virtual network, so I have no Personally Identifiable Information on this computer.
<br />
<br />

Find failed login to Windows VM:<br />
<img src="https://i.imgur.com/lqOfNt3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
I created an attacker machine on a different server to make logs for review. I used the attacker virtual machine with the wrong credentials to make a failed login. There are many more failed attempts trying to log onto my virtual computer outside the attacker's vital machine, demonstrating the importance of firewalls.
<br />
<br />


Find failed login to Windows VM with filter:<br />
<img src="https://i.imgur.com/cn4xkJy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
To filter logs, you can use the filter feature in the Windows Event Viewer. To look for failed log-ins, you can use '4625'. This will show all failed attempts. Other useful  Event IDs are 1074: System has been shut down by a process/user. Event ID '4672'used for special privileges were assigned to a new logon. And '4719' is the event generated when the computer's audit policy changes.

<br />
<br />

Find failed login to SQL database:<br />
<img src="https://i.imgur.com/ypWUjwr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
I also used the attacker virtual machine to try and access my SQL database to see if that was secure without firewalls. Upon reviewing the logs, there were many attempts to get into the database as well. The code '18465' is used for any failed SQL logins. Other helpful event IDs are ‘17162’ (for restart of SQL Server) and ‘7364’ SQL Server Stopped
<br />
<br />


Summary:  <br/>
This project serves as an insightful exploration of the consequences of turning off the Windows firewall. Through intentional attempts to access a Windows VM and a SQL database with an attacker virtual machine, the project underscores the critical role of firewalls in preventing unauthorized access. The logs presented demonstrate the increased vulnerability and heightened risk of security breaches when firewalls are deactivated. The cautionary note regarding the necessity of firewalls for most computers reinforces the importance of maintaining robust security measures to safeguard sensitive information and prevent unauthorized access.
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
