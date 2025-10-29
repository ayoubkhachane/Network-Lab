# Network-Lab | Virtual Enterprise Network

## Overview
This is my first cybersecurity lab project where I built a **virtual network** that simulates a small company environment.  
The goal was to practice **network setup, segmentation, firewall rules, and Active Directory** in a safe, isolated environment.

---

## Tools & Technologies
- **Virtualization:** VMware Workstation Pro  
- **Firewall/Router:** pfSense  
- **Servers:** Windows Server 2019 (AD, DNS, DHCP), Ubuntu Server  
- **Clients:** Windows 10  
- **Other Tools:** Wireshark (for traffic monitoring), Kali Linux (for testing network security)  

---

## Network Design
I divided the network into three main VLANs:

| VLAN | Purpose        | Subnet        | Devices                          |
|------|----------------|---------------|---------------------------------|
| 10   | Admin          | 192.168.10.0  | Windows Server, Admin PCs       |
| 20   | Users          | 192.168.20.0  | User PCs                        |
| 30   | Servers/DMZ    | 192.168.30.0  | Ubuntu server, Web server       |

- **pfSense** acts as the main router and firewall.  
- **Firewall rules** allow Admins to access all devices, while Users have limited access.  

---

## Setup Steps
1. **Create VMs** in VMware Workstation Pro for all machines.  
2. **Install pfSense** on the firewall VM and configure WAN/LAN interfaces.  
3. **Create VLANs** in pfSense and assign IP ranges.  
4. **Install Windows Server** and set up Active Directory, DNS, and DHCP.  
5. **Join client PCs** to the domain.  
6. **Test connectivity** between VLANs and verify firewall rules.  
7. (Optional) Use Wireshark to monitor traffic and test isolation between VLANs.

---

## Screenshots / Proof
*(I took screenshots of my lab setup and network diagrams here.)*  

- pfSense dashboard with VLANs  
- Active Directory Users and Computers  
- Windows clients joined to domain  
- Ping tests showing allowed and blocked connections  

---

## Learning Notes
- I learned how to **segment a network** using VLANs.  
- Configuring **firewall rules** between different subnets was very practical.  
- Active Directory integration made managing users and permissions easier.  
- Using Wireshark helped me **see how packets travel** across the network.  

---

## Next Steps
- Add a **SIEM server** to collect logs from the network.  
- Create **vulnerable machines** to simulate attacks.  
- Automate deployment using **Vagrant or Ansible**.  

---

**Author:** Ayoub Khachane  
