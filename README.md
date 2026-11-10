VLAN Configuration with Trunking and Native VLAN 999

Project Overview

This project demonstrates VLAN configuration, access port assignment, trunk link configuration, and native VLAN implementation using two Cisco 2960 switches in Cisco Packet Tracer.
The network is divided into three functional VLANs: IT, HR, and Management. An additional VLAN is configured for unused switch ports, while VLAN 999 is configured as the native VLAN for trunk communication between switches.

Network Devices
•	2 × Cisco 2960 Switches (S1 and S2)
•	6 × PCs
•	Cisco Packet Tracer

VLAN Configuration
VLAN ID	VLAN Name	Purpose
10	IT	IT Department
20	HR	HR Department
30	Management	Management Department
99	Unused_Ports	Unused Switch Ports
999	Native	Native VLAN for Trunking

Network Port Configuration
The following port assignments are configured on both switches:
Switch Ports	Mode	VLAN
Fa0/1–Fa0/6	Access	VLAN 10
Fa0/7–Fa0/12	Access	VLAN 20
Fa0/13–Fa0/18	Access	VLAN 30
Fa0/19–Fa0/24	Access / Shutdown	VLAN 99
G0/2	Access / Shutdown	VLAN 99
G0/1	Trunk	Native VLAN 999

IP Addressing Table
Device	VLAN	IP Address	Subnet Mask
IT-PC1	10	192.168.10.10	255.255.255.0
IT-PC2	10	192.168.10.11	255.255.255.0
HR-PC1	20	192.168.20.10	255.255.255.0
HR-PC2	20	192.168.20.11	255.255.255.0
Management-PC1	30	192.168.30.10	255.255.255.0
Management-PC2	30	192.168.30.11	255.255.255.0
S1	30	192.168.30.1	255.255.255.0
S2	30	192.168.30.2	255.255.255.0

Configuration Highlights
1. Create VLANs
Create VLANs 10, 20, 30, 99, and 999 on both switches.
2. Configure Access Ports
Assign switch access ports to their respective departmental VLANs.
3. Configure Unused Ports
Assign unused ports to VLAN 99 and administratively shut them down.
4. Configure Trunking
   
Configure GigabitEthernet0/1 on both switches as a trunk port and set VLAN 999 as the native VLAN.
6. Configure Management IP Addresses
•	S1: 192.168.30.1/24
•	S2: 192.168.30.2/24
Both switches use VLAN 30 as their management SVI.
Verification Commands
Use the following commands to verify the configuration:
show vlan brief
show interfaces trunk
show ip interface brief
show running-config

Expected Results
•	VLANs are successfully created on both switches.
•	Departmental access ports are assigned to the correct VLANs.
•	Unused ports are assigned to VLAN 99 and shut down.
•	The trunk link operates between S1 and S2.
•	VLAN 999 is configured as the native VLAN on both ends.
•	Management interfaces have the correct IP addresses.
•	Devices in the same VLAN can communicate across the trunk link.

Skills Demonstrated
•	Cisco Switch Configuration
•	VLAN Creation and Management
•	Access Port Configuration
•	VLAN Trunking
•	Native VLAN Configuration
•	Switch Management using SVI
•	Unused Port Security Practices
•	Basic Network Troubleshooting
•	Cisco IOS CLI Commands

Conclusion
This project demonstrates how VLANs can logically divide a network into separate departments while trunking enables communication between switches. Configuring a dedicated native VLAN and isolating unused ports also helps improve basic network organization and security.
Tool Used: Cisco Packet Tracer

