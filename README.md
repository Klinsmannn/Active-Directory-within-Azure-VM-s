# Active-Direct 📂 <p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Azure Domain Controller Setup
- Server Manager W/Active Directory
- Active Directory Users and Computers
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/cfe7e4e1-0373-4684-8ac6-c0cd2ffd2c0e">
</p>
<p>
<br />
  <img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/8fe80f21-7cc0-443b-b3c8-bd3a1c9845ec">
</p>
</p>
<br />
<img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/3163cd8c-8e53-41b7-ad4a-e2fc0609bebb">
<p>
</p>
<br />
<img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/7eaecb01-f6d9-480c-90a8-3faa2b0de590">


In Azure Cloud create your resource group with a Windows Server on it. Were going to set your Domain controllers ip to static(nonmoving) so that it can be discovered on the network.We go to out Networking tab in the Domain controller and select the NIC(Network Interface Card). Lastly enable ICMPv4 traffic in the Advance Firewall setting in your domain controller. You can find Firewall settings by typing it in the windows search bar or in Control panel> Systems and Security> Windows Defender Firewall.
</p>
<br />

<p>
<img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/b5a94463-cc15-43ea-af35-80e8c4afac8a">
</p>
<p>
  <br />
  <img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/f654e30e-26d5-49ae-903f-b93585d76d73">
  <p>
  </p>
  <br />
  

Look up Server manager in your Domain controller and go into add Roles and Features. Next is to create your Forest and Root name for your Active Directory. Forest is like your main container containing other users,groups, and computers. Restart and Log back into Domain Controller.
</p>
<br />
<p>
  <img src= "https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/05635ad5-0e98-427c-b7eb-93ecf1038a7a">

</p>
<p>
 Open active directory in start menu or by going into tools in your server manager. 
</p>
<br />ory-within-Azure-VM-s
