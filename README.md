<p align="center">
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

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/337595dc-a39e-42f6-a016-5160b7ed099c)

Setting up an Azure virtual network involves the following steps:

1. Sign in to the Azure Portal: Access the Azure Portal using your Azure account credentials.

2. Create a Virtual Network (VNet): Search for "Virtual Networks" in the search bar and select "Virtual Networks" from the search results. Click on "Add" to create a new VNet.

3. Define VNet settings: Give your VNet a name and choose the subscription, resource group, and location. Specify the address space for the VNet, which defines the IP address range. You can also configure DNS server settings if necessary.

4. Configure subnets: Within the VNet, create one or more subnets. Define the subnet name and IP address range for each subnet. Ensure that the subnet ranges do not overlap.

5. Advanced networking options: You may choose to configure additional settings, such as Network Security Groups (NSG) for controlling inbound/outbound traffic, User-Defined Routes (UDR) for custom routing, and VPN Gateway for connecting on-premises networks.

6. Peer virtual networks (optional): If you have multiple VNets and want to enable communication between them, you can set up VNet peering. This allows network traffic between the peered VNets.

7. Set up network security: Configure NSGs to enforce network security rules for subnets and control inbound/outbound traffic. You can define rules for allowing or denying specific protocols and port access.

8. Associate resources: Associate resources like virtual machines (VMs), load balancers, and other services with the virtual network. Ensure that the resources are deployed within the desired subnets.

9. Test connectivity: Validate connectivity by testing communication between resources within the virtual network. Verify that the configured network settings are functioning as expected.

By following these steps, you can easily set up a virtual network in Azure, which provides a secure and isolated network environment for your applications and services, enabling seamless communication and connectivity.
</p>
<p>



![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/262ae8fa-3d1d-4c6f-a244-f8a60cb30f2e)

To set up and use Remote Desktop, follow these general steps:

1. Enable Remote Desktop on the target computer: Open the System Properties on the computer you want to access remotely. Go to the Remote tab and enable "Allow Remote Connections to this computer." You may need to adjust firewall and network settings to allow Remote Desktop connections.

2. Obtain the IP address or hostname of the target computer: Note down the IP address or hostname of the computer you want to connect to remotely. You will need this information to establish the Remote Desktop connection.

3. Connect to the remote computer from another device: On your remote device (e.g., another computer or mobile device), launch the Remote Desktop client application. If it is not pre-installed, you can download it from the official website for your operating system.

4. Enter the IP address or hostname: In the Remote Desktop client, enter the IP address or hostname of the target computer you want to connect to.

5. Authenticate and connect: Enter the login credentials (username and password) for the target computer when prompted by the Remote Desktop client. Make sure you have the necessary permissions to access the remote computer.

6. Configure display and other settings (optional): The Remote Desktop client may offer options to adjust display settings, audio settings, and other preferences. Customize these settings as needed.

7. Connect and access the remote desktop: After providing the necessary information and settings, click on the "Connect" or "Start" button in the Remote Desktop client. This will establish the connection to the remote computer and show you its desktop interface.

8. Interact with the remote desktop: Once connected, you can use your local device's mouse, keyboard, and touch controls (if applicable) to interact with the remote desktop just as if you were physically sitting in front of it. You can run applications, access files, and perform tasks as if you were using the remote computer directly.

9. Disconnect and end the session: When you are finished with the remote session, you can either log off from the remote computer or simply close the Remote Desktop client application. This will end the connection and return you to your local device.

Remember to ensure that the target computer has Remote Desktop access enabled and is reachable from your remote device. Additionally, check for any firewall or network restrictions that might affect the Remote Desktop connection.
</p>
<p>



![image](https://github.com/derekjonesaa/configure-ad/assets/167825508/2afcd11f-4448-4409-9e09-02a3c0b0fbdf)

Setting up Active Directory (AD) involves several steps. Here's a simplified step-by-step guide:

1. Install Windows Server: Begin by installing Windows Server on a dedicated machine that will act as the domain controller for Active Directory.

2. Configure the Server: After installation, configure the server with a static IP address and assign it a unique hostname.

3. Promote to Domain Controller: Open the "Server Manager" and click on "Add roles and features." Select the Active Directory Domain Services role and proceed with the installation. After installation, promote the server to a domain controller.

4. Create a New Forest: In the Active Directory Domain Services Configuration Wizard, select "Add a new forest" and specify a domain name for your forest. Note that this domain will become the root of your Active Directory hierarchy.

5. Set Domain and Forest Functional Levels: Set the desired domain and forest functional levels based on the requirements of your environment.

6. Configure DNS: Ensure that Active Directory integrated DNS is installed and configured properly. This enables domain name resolution for Active Directory.

7. Complete the Installation: The installation process will install the necessary services and components, and a reboot may be required to finalize the configuration.

8. Manage Active Directory Users and Computers: Access the "Active Directory Users and Computers" tool to manage users, groups, and organizational units (OUs). You can create user accounts, assign them to groups, and organize them in OUs.

9. Group Policy: Use the Group Policy Management Console to create and manage group policy objects (GPOs). GPOs allow you to define and enforce specific settings, configurations, and restrictions across your domain.

10. Add Additional Domain Controllers (optional): For redundancy and fault tolerance, you can add additional domain controllers to your Active Directory environment. This provides backup in case the primary domain controller becomes unavailable.
</p>
<p>

<br />
