# SIEM in Azure
Skills learned: Azure Portal, Microsoft Sentinel, Kusto Query Language, Network Security Groups, Powershell

<h2>Description</h2>
I am following a tutorial from a video at this <a href="https://www.youtube.com/watch?v=RoZeVbbZ0o0&t=29s">link</a>. <br/>
I created a virtual machine in Azure and exposed it to the internet as a honeypot. I then created a Log Analytics Workspace in Azure and connected it to the VM to pull logs from the Windows Event Viewer.  Next, I connected Mircosoft Sentinel (SIEM) to the VM. I observed live attacks (RDP Brute Force) from around the world and used a custom PowerShell script to translate the attackers IP address to Geolocation data using an API and plotted it on the Microsoft Sentinel Map using custom logging. 
<br/>

<h2>Firewall rule to allow all traffic into VM</h2>

<p align="center">
<img src="https://user-images.githubusercontent.com/67126494/179144406-85bcc3fb-0491-4a48-877a-fb8fe872705a.png" alt="all all firewall rule"/>
</p>

<br/>

<h2> Connect Log Analytics Workspace to VM</h2>
<p align="center">
<img src="https://user-images.githubusercontent.com/67126494/179144452-3c4cca44-b66e-4f15-bcc1-02a5f3484d92.png" alt="connect LAW to VM"/>
</p>
 
<br/>

<h2> Start Microsoft Sentinel and connect it to the Log Analytic Workspace </h2>
<p align="center">
<img src="https://user-images.githubusercontent.com/67126494/179144468-6f0d6d34-604e-472c-87c6-cbdb340faa9a.png" alt="Start Sentinel"/>
</p>

<br/>

<h2> Custom Powershell script to extract data from failed RDP login and find geolocation through API </h2>
<p align="center">
<img width="890" alt="Powershell Script running" src="https://user-images.githubusercontent.com/67126494/179144515-02644e67-ec02-4283-94a7-ea7ce069c099.png">
</p> 

<br/>

<h2> Querying the custom logs </h2>
<p align="center">
<img src="https://user-images.githubusercontent.com/67126494/179144489-53e90aff-d691-4b6f-a49c-768434640785.png" alt="qeuried custom logs"/>
</p>

<br/>

<h2> Final map of attacks </h2>
<p align="center">
<img src="https://user-images.githubusercontent.com/67126494/179144543-0da9a4ba-5e92-48c3-bb5c-976d14600419.png" alt="final attack map"/>
</p>
 <!--

<h2>Walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


--!>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
