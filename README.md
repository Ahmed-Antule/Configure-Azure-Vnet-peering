# Configure-Azure-Vnet-peering

## What is Vnet peering in Azure
VNet Peering in Azure is a networking feature that allows you to connect two Azure Virtual Networks (VNets) seamlessly, enabling direct,private communication between them.
It's like connecting two offices with a private cable instead of using public roads.

### Key Features of VNet Peering:
Private and Secure Connection – Traffic between VNets stays within Microsoft’s network.

Low Latency and High Bandwidth – Uses the Azure backbone, ensuring fast communication.

Resource Sharing – VNets in different regions can communicate as if they were on the same network.

No Additional Bandwidth Restrictions – Data transfer is only limited by the VM’s network throughput.

Global VNet Peering – Allows peering across Azure regions (not just within a single region).

Full Mesh Connectivity – Multiple VNets can be interconnected using hub-and-spoke or full mesh topologies.

## Summary

### Step-1
#### Creating Virtual Networks (VNet)
![Capture1](https://github.com/user-attachments/assets/a712ac77-3537-42de-8688-717aac3d9214)

Create first VNet with a specified IP address range and then proceed with review and create
![Capture2](https://github.com/user-attachments/assets/15c7bb7a-270c-4521-8d5a-ab12457ffe70)
![Capture3](https://github.com/user-attachments/assets/20712721-6414-4da0-85d6-cb924080bce3)

Create second Vnet with a specified IP address range
![Capture4](https://github.com/user-attachments/assets/17855596-e583-45d4-8e72-abab89f7d82d)

### Step-2
#### Creating Virtual Machine
![Capture5](https://github.com/user-attachments/assets/28204d46-2468-4ddf-86ae-eeef218cc211)

Create the First VM and ensure that you select the VNet (network-1) during the setup
![Capture6](https://github.com/user-attachments/assets/6c40a151-a3ba-46d5-b048-e4f27b667b27)

Create the secong VM and ensure that you select the VNet (network-2) during the setup
![Capture7](https://github.com/user-attachments/assets/d55d741c-61c7-476d-aed2-199cfb110af9)

### Step-3
Connect both VMs using RDP,then turn Off the Firewall on both VMs to allow seamless communication between them.
![Capture8](https://github.com/user-attachments/assets/0e1dda0d-937d-4fe6-83ac-10c34fd1fdf3)
![Capture9](https://github.com/user-attachments/assets/33a8c2b6-3bf6-441a-a54c-aaa72a56f19d)
![Capture10](https://github.com/user-attachments/assets/cb18094b-9b6f-492d-a6c5-65b53825d778)

### Step-4
Go,to Virtual Network,select VNet you created,go to peering section and click on add button.
![Capture11](https://github.com/user-attachments/assets/d11ee0e7-2793-442b-b730-c1b6d5892105)

Assign a name to peering link and select the virtual network you want to establish communication with aand click on save
![Capture12](https://github.com/user-attachments/assets/ad034fbb-077e-4f42-a78a-5e05faca4665)

### Step-5
Check the IP address in both Virtual Machines(VM)
![Capture14](https://github.com/user-attachments/assets/75e1485c-d0df-4908-8d06-e9c31cd2ed69)
![Capture15](https://github.com/user-attachments/assets/7d456705-3446-4cab-a3a4-aaf096b0bf98)

Once IP Address is conformed, test the connection between both the VMs by pinging them
![Capture16](https://github.com/user-attachments/assets/d222d9f1-d36f-4519-b989-562110da70fd)
