Basic Switch and End Device Configuration using Cisco Packet Tracer.

This project demonstrates how to build and secure a simple network topology using **Cisco Packet Tracer**.  
It covers end device configuration, network expansion with a switch, and the application of a basic firewall rule.

---
🧰 Tools Used
- Cisco Packet Tracer (network simulation & configuration)

---

## 📚 Project Overview
- Started with a **basic PC-to-server connection** using a crossover cable.  
- Configured **IP addresses** on the PC and server to enable communication.  
- Verified connectivity with:
  - `ipconfig` on the PC  
  - `ping 192.168.0.1` to test reachability  
  - Simple PDU one-time ping message  

- Expanded the network by adding **two more PCs and a switch**.  
- Assigned IPs to all devices and confirmed connectivity across the network.  

- Configured a **firewall on the server**:  
  - **Blocked ICMP traffic** (pings were denied).  
  - **Allowed IP traffic** so that web browsing to the server still worked.  

---

## 🖥️ Devices and IP Assignments

| Device        | IP Address   | Subnet Mask     |
|---------------|--------------|-----------------|
| **MARYSERVER0**   | `192.168.0.1` | `255.255.255.0` |
| **MARYPC0**       | `192.168.0.2` | `255.255.255.0` |
| **MARYPC1**       | `192.168.0.3` | `255.255.255.0` |
| **MARYPC2**       | `192.168.0.4` | `255.255.255.0` |

---

## 🔐 Firewall Configuration
- **Service Enabled:** Firewall  
- **Deny Rule:** ICMP protocol traffic  
  - Remote IP: `0.0.0.0`  
  - Wildcard Mask: `255.255.255.255`  
- **Allow Rule:** IP protocol traffic  
  - Remote IP: `0.0.0.0`  
  - Wildcard Mask: `255.255.255.255`  

**Verification:**  
- Pings to the server failed (ICMP blocked).  
- HTTP access to the server via web browser succeeded (IP traffic allowed).  

---

## ✅ Test Checklist
- [x] PC-to-Server connection verified with `ping`  
- [x] Connectivity confirmed across all PCs and Server after expansion  
- [x] Firewall blocked ICMP successfully  
- [x] Web access to the server remained functional  

---

## 📌 Key Takeaways
- Learned how to configure basic **IP addressing** and test connectivity.  
- Understood how to apply **firewall rules** in Packet Tracer.  
- Demonstrated how security controls (blocking ICMP) can coexist with allowed traffic (HTTP).  

---


## 🔒 Key Security Configuration
- **Firewall enabled** on the server.  
- **Deny rule:** Blocked ICMP traffic to prevent reconnaissance (ping sweeps).  
- **Allow rule:** Permitted IP traffic to ensure legitimate communication (e.g., HTTP).  
- **Verification:** ICMP blocked successfully, but HTTP browsing remained functional.  

---

## 📈 Key Takeaways
- Reinforced understanding of **IP addressing and subnetting**.  
- Learned how to configure and test **basic device connectivity**.  
- Gained practical insight into **firewall rules and traffic filtering**.  
- Saw how **security and availability** must be balanced in network design.  

---

## 🧩 Challenges Faced
- After enabling the firewall, some expected services were briefly unreachable.  
- Needed to refine rule order and scope to avoid blocking legitimate traffic.  
- Ensured that ICMP was denied while still allowing HTTP access.  

---

## 🚀 Future Improvements
- Introduce **VLANs** for segmentation of users and servers.  
- Use a **router or Layer 3 switch** to enable inter-VLAN routing.  
- Add **DHCP services** for dynamic IP assignment.  
- Implement **Access Control Lists (ACLs)** on routers/switches.  
- Extend to **OSPF, NAT, and EtherChannel** to mirror enterprise-level designs.  

---

## 6. Conclusion
This project successfully demonstrated how to build and secure a simple Packet Tracer network. Starting from a single PC-to-server connection, the network was expanded with a switch and additional hosts. Finally, firewall rules were applied to enhance security by blocking ICMP traffic while still allowing legitimate services like web access.

