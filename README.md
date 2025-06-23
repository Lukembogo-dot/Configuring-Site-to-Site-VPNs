# 🔐 Site-to-Site IPsec VPN Configuration Project (Cisco Packet Tracer)

This project demonstrates how to configure and verify a **site-to-site IPsec VPN tunnel** using Cisco IOS CLI in **Cisco Packet Tracer**. The VPN ensures secure communication between two remote LANs across an untrusted network.

---

## 🖥️ Devices Used

- 🛠️ **Routers**: R1, R2, R3 (Cisco 1941)
- 💻 **End Devices**: PC-A, PC-B, PC-C
- 🔌 **Switches**: S1, S2, S3
- 📡 **Connections**: Serial and Ethernet interfaces

---

## 🌐 IP Addressing Overview

| Device | Interface | IP Address       | Subnet Mask       | Connected To |
|--------|-----------|------------------|-------------------|--------------|
| R1     | G0/0      | 192.168.1.1      | 255.255.255.0     | S1 F0/1      |
| R1     | S0/0/0    | 10.1.1.2         | 255.255.255.252   | R2 S0/0/0    |
| R2     | G0/0      | 192.168.2.1      | 255.255.255.0     | S2 F0/2      |
| R2     | S0/0/0    | 10.1.1.1         | 255.255.255.252   | R1 S0/0/0    |
| R2     | S0/0/1    | 10.2.2.1         | 255.255.255.252   | R3 S0/0/1    |
| R3     | G0/0      | 192.168.3.1      | 255.255.255.0     | S3 F0/5      |
| R3     | S0/0/1    | 10.2.2.2         | 255.255.255.252   | R2 S0/0/1    |
| PC-A   | NIC       | 192.168.1.3      | 255.255.255.0     | S1 F0/2      |
| PC-B   | NIC       | 192.168.2.3      | 255.255.255.0     | S2 F0/1      |
| PC-C   | NIC       | 192.168.3.3      | 255.255.255.0     | S3 F0/18     |

---

## 🎯 Project Objectives

- ✅ Verify basic network connectivity  
- 🔐 Configure **ISAKMP Phase 1** (AES-256, DH Group 5, pre-shared key)  
- 🔐 Configure **IPsec Phase 2** (ESP-AES, ESP-SHA-HMAC)  
- 🧾 Apply **access lists** to define interesting traffic  
- 🧰 Bind **crypto maps** to router serial interfaces  
- 📊 Verify VPN tunnel with ping tests and `show crypto ipsec sa`

---

## ✅ Final Result

- 🔁 VPN tunnel successfully established between R1 and R3  
- 🔒 Interesting traffic was encrypted; uninteresting traffic passed in clear text  
- 📈 Tunnel verified via packet counters  
- 🏁 Achieved **100% completion** in Packet Tracer

---

## 🧠 What I Learned

This project strengthened my understanding of:

- IPsec VPN architecture
- ISAKMP and IPsec configuration on Cisco routers
- Practical use of ACLs and crypto maps
- Tunnel testing and verification techniques

---

## 📸 Screenshots

> Be sure to check the **screenshots folder** to see:
- Initial pings  
- Command-line configuration  
- Tunnel status before/after traffic  
- Final tunnel verification results

---

## 🔑 Default Credentials

- Console password: `ciscoconpa55`  
- VTY password: `ciscovtypa55`  
- Enable password: `ciscoenpa55`  
- SSH login: `SSHadmin` / `ciscosshpa55`  

---

## 👨‍💻 Author

Luke Mbogo  
🇰🇪 Nairobi, Kenya  
Cybersecurity & Networking Enthusiast  
