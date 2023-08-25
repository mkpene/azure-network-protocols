<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create some sample file shares with various permissions
- Attempt to access file shares as a normal user
- Create an “ACCOUNTANTS” Security Group, assign permissions, an test access
- Check back to make sure access is granted and works correctly

<h2>Actions and Observations</h2>


![image](https://github.com/mkpene/azure-network-protocols/assets/142267681/4929221a-bc42-47fe-8127-fa784272d184)

<p>
I created a security group called "ACCOUNTANTS." I accessed the Active Directory Users and Computers console on the domain controller and added a new security group named "ACCOUNTANTS." I identified a couple of users who should have access to the shared folder. I added these users to the "ACCOUNTANTS" security group. With the security group in place, I went back to the shared folder on the "ServerVM." I configured the folder's permissions, granting read and write access to the "ACCOUNTANTS" security group.
</p>
<br />


![image](https://github.com/mkpene/azure-network-protocols/assets/142267681/bc825f68-ba3b-4b96-b290-442d324cd161)

<p>
On another virtual machine, the client machine, I logged in using one of the user accounts that belonged to the "ACCOUNTANTS" security group. To ensure that permissions were working as intended, I also logged in with a user who was not part of the "ACCOUNTANTS" security group and attempted to access the shared folder. I observed how access was granted or denied based on the user's group membership.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
