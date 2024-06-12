<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)



<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/8b82adbe-c991-43d6-ac20-b34bf693609d)
Step 1: Log into Azure --> search "virtual machines" --> click "create azure virtual machine" to create VM#1. Name this first virtual machine "DC-1" using your current region --> set the image type as "Windows Server 2022" (effectively making it a domain for the lab) --> Set username and password --> create VM #2 --> title it "Client-1" (repeat the same steps used to create VM#1 except for the image type select "Windows 10 pro" since this VM will be the employees'/ cleints' computer).

![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/e2a62ffc-e6fb-4fdc-8e3a-e2e11aee6fc7)
Step 2: Go to DC-1's network settings --> select networking --> click the hyperlink next to "network interface" --> "IP Configurations" --> "ipconfig1" --> change the assignment from dynamic to static (this ensures DC-1's IP address will not change) --> check the NIC settings to make sure both VMs are on the same "Vnet". This will ensure both VMs can communicate & connect with each other later in this lab.

![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/21d25b17-d837-4e47-8467-ef822367b83e)
Step 3: Remote Desktop into DC-1 via windows firewall security settings --> Advanced settings --> inbound/outbound rules to allow "IPV4 permissions" on DC-1's Firewall. This will open the firewall for connectivity after DC-1 is converted into a domain.

![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/f8a990a3-3b2d-4070-8d2a-9ebb838a7b0f)
Step 4: Ensure communication between both VMs via perpetual ping using cmd:ping -t (Ip Address).

![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/ff2d61d1-0b8a-4275-bfb6-f35d9a581022)
Step 5: Install "Active Directory" on DC-1. Set up DC-1 as a new domain.

![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/294fea66-91cc-4163-b243-a3271df03028)
Step 6: Remote Desktop into DC-1 to create two "Organzational Units" (OU), one titled "Admins" and another titled "Employees" within Active Directory.

