# Date :27/10/2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>

<img width="1917" height="1073" alt="Screenshot 2026-10-27 190041" src="https://github.com/user-attachments/assets/3c32c3c2-b608-4fcb-995d-1641730b164e" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>

<img width="1917" height="1077" alt="Screenshot 2026-10-27 190446" src="https://github.com/user-attachments/assets/2a0655c7-0aa0-4129-a021-df94e9da7913" />


•	IP configurations on PCs<br>
PC0:

<img width="1917" height="1078" alt="Screenshot 2026-10-27 185723" src="https://github.com/user-attachments/assets/76436889-8a8b-41d5-95d1-1fb6e78a0036" />


PC1:

<img width="1917" height="1078" alt="Screenshot 2026-10-27 185749" src="https://github.com/user-attachments/assets/7d4fe423-24db-4bc7-b19b-43ab6d7a5976" />


•	Successful ping between PC0 and PC1<br>
PC0:
<img width="1915" height="1076" alt="Screenshot 2026-10-27 184458" src="https://github.com/user-attachments/assets/5c46b6d9-0832-4e75-997f-b5ae8a41a064" />

PC1:
<img width="1917" height="1075" alt="Screenshot 2026-10-27 185623" src="https://github.com/user-attachments/assets/686fb34f-5208-4cae-b2cd-ec7f030842d6" />



________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

