# VLAN (Virtual Local Area Network) 

This repository contains a Cisco Packet Tracer project demonstrating the use of **Virtual LANs (VLANs)** in networking.  
The project includes switches and PCs connected in a topology where VLANs are configured to separate network traffic logically.

---

## 📂 Project Files
- `VLan.pkt` → Cisco Packet Tracer project file  

---

## 🔑 What is VLAN?
A **Virtual LAN (VLAN)** is a logical subdivision of a switch network.  
It allows network administrators to create separate broadcast domains within a single switch.  

### 🎯 Key Benefits of VLANs:
1. **Segmentation** → Divide one physical network into multiple logical networks.  
2. **Security** → Isolate sensitive data by separating departments (e.g., HR, Finance, IT).  
3. **Efficiency** → Reduce unnecessary broadcast traffic.  
4. **Flexibility** → Devices can be grouped logically instead of physically.  

---

## 📌 Topology Overview
The topology has multiple PCs connected to switches, and VLANs are configured to separate traffic into different logical groups.  

### Example VLAN Plan
- **VLAN 10 (HR Department)**  
  - PCs: `PC0`, `PC1`  
- **VLAN 20 (IT Department)**  
  - PCs: `PC2`, `PC3`  
- **VLAN 30 (Finance Department)**  
  - PCs: `PC4`, `PC5`  

---

## 🚀 VLAN Configuration Example

### Step 1: Create VLANs on the Switch
```bash
Switch(config)# vlan 10
Switch(config-vlan)# name HR
Switch(config)# vlan 20
Switch(config-vlan)# name IT
Switch(config)# vlan 30
Switch(config-vlan)# name Finance
Step 2: Assign Ports to VLANs
bash
Copy code
Switch(config)# interface fastEthernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10

Switch(config)# interface fastEthernet 0/2
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 20

Switch(config)# interface fastEthernet 0/3
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 30
Step 3: Configure Trunk Links (if multiple switches are used)
bash
Copy code
Switch(config)# interface fastEthernet 0/24
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk allowed vlan all

📖 Learning Outcomes
Understand how VLANs segregate broadcast domains.

Learn how to configure VLANs on switches.

Understand access ports vs trunk ports.

Practice inter-VLAN communication (using router-on-a-stick or Layer 3 switch).

🛠 Requirements
Cisco Packet Tracer (Version 7.3 or later recommended)

✨ Author
Created by [Kajal Kachare] for practicing VLAN configuration in Cisco Packet Tracer.

