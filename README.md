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
- System Manager
- Active Directory Domain Services
- 

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Azure Domain Controller Setup
- Server Manager W/Active Directory
- Active Directory Users and Computers
- Set DNS to Domain Controller
- Reset/ Unblock Passwords 🔓

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


In Azure Cloud create your resource group with a Windows Server on it. Were going to set your Domain controllers IP address to static(nonmoving) so that it can be discovered on the network.We go to the Networking tab in the Domain controller and select the NIC(Network Interface Card). We enable ICMPv4 traffic in the Advance Firewall setting in your domain controller. You can find Firewall settings by typing it in the windows search bar or in the Control panel> Systems and Security> Windows Defender Firewall.
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
  

Look up Server manager in your Domain controller and go into add Roles and Features. Next is to create your Forest and Root name for your Active Directory. Forest is like your main container containing other users,groups, and computers. Finish installing and then restart to log back into Domain Controller.
</p>
<br />
<p>
  <img src= "https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/05635ad5-0e98-427c-b7eb-93ecf1038a7a">
</p>
<p>
<br />
  <img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/19e304de-a765-475d-84ba-464797083b67">

 Open active directory in start menu or by going into tools in your server manager. Right click on your Domain and create a new Organizational Unit(OU). OUs is a division inside of your Active directory so you can keep things seperate (like a folder in a folder). You can change users groups or add / remove users by going into properties and looking under (Members of) tab. 

</p>
<br />
<img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/0d83bce6-8305-4bf3-98fb-4073afa74fc0">
<p>
</p>
<br />
<img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/f011ee53-2a92-4250-8b97-a1acd13aaa1a">
<p>
</p>
<br />
Change DNS settings in Azure so it can start using your own Domain Controllers DNS instead of the one Azure automatically gives it. To find DNS settings go to the NIC(network interface card) in your VM and change from automatic DNS to custom DNS that has the private ip address of the domain controller your going to use. In that VM go to rename the PC in system settings and change your Domain. So System> Rename this PC (Advanced)> Computer Name> Change...> Domain> "Name of Domain". Restart computer
<p>
</p>
<br />
<img src="https://github.com/Klinsmannn/Active-Directory-within-Azure-VMs/assets/146140975/d69c0f61-69e9-4af0-8662-311e278596d1">

In Active Directory Users and Computers go to the (users) folder, right click on properties and go under the Account tab to check or uncheck the unlock password box.You can adjust other settings from there too like changing password at next logon or add/remove accounts for employees.😊

