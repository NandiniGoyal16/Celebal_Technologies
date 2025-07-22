# ☁️ Cloud Infrastructure & Security Internship Journey @ Celebal Technologies

Welcome to my internship journey at *Celebal Technologies*!  
This repository contains my week-wise assignments, research, and project submissions for the **Cloud Infrastructure & Security** department.

🗓️ **Internship Duration:** *June 2, 2025 – August 3, 2025*  
💻 **Mode:** *Remote*  
🔐 **Domain:** *Cloud Infra & Security*

---

## 📌 Weekly Breakdown

### ✅ Week 1: Introduction to Networking & Protocols
**Duration:** June 2 – June 8, 2025  
**Topics Covered:**
- OSI Model (7 Layers)
- TCP/IP Model
- Protocols: TCP, UDP, HTTP, HTTPS, ICMP
- Difference between TCP & UDP

**Tasks Completed:**
- 📄 R&D Document on OSI Model
- 📄 R&D Document on TCP/IP Model
- 📄 R&D Document on Protocols

📁 [Week 1 Folder](./Week1)

---

### ✅ Week 2: IP Addressing, Subnetting & MAC Layer Protocols
**Duration:** June 9 – June 15, 2025  
**Topics Covered:**
- IPv4 & IPv6 Addressing
- Subnetting (CIDR, Netmask, VLSM)
- MAC Addressing
- ARP & RARP (and related protocols)

**Tasks Completed:**
- 📄 R&D Document on IP Addressing and Subnetting (IPv4 & IPv6)
- 📄 R&D Document on MAC Addressing and Functionality of ARP & RARP

📁 [Week 2 Folder](./Week2)

---

### ✅ Week 3: Azure Global Infrastructure
**Duration:** June 16 – June 22, 2025<br>
**Topics Covered:**
- Azure Global Architecture
- Geographies & Regions
- Availability Zones
- Data Centers & Edge Zones

**Tasks Completed:**
- 📄 R&D Document on Azure Global Infrastructure: Geographies, Regions, Availability Zones, Data Centers

📁 [Week 3 Folder](./Week3)

---

### ✅ Week 4: Azure Virtual Networking – VNets, Subnets, and Peering
**Duration: June 23 – June 30, 2025**<br>
**Topics Covered:**
- CIDR Ranges in Azure
- Virtual Networks (VNets) and Subnet Configuration
- Launching and configuring Linux & Windows VMs
- Network Security Groups (NSGs) and Inbound Rules
- Enabling communication via Ping (ICMP)
- VNet Peering: Concept, Types, and Implementation
- Cross-VNet communication setup
- Troubleshooting firewall & RDP issues

**Tasks Completed:**
- 📄 R&D Document: Practical Implementation - Deploying VMs Across Subnets and Peered VNets in Azure 
<!-- ⚙️ Created Linux & Windows VMs in separate subnets under VNet1
🌐 Enabled bidirectional communication (ping) using ICMP rules in NSG
🔒 Configured Windows Firewall to allow ICMP via GUI and CLI
🔁 Created a second Virtual Network (VNet2) and added another Linux VM
🔗 Connected VNet1 and VNet2 using VNet Peering (bi-directional)
📶 Verified cross-VNet connectivity by pinging between VMs across VNets
🧹 Cleaned up all resources post-deployment to avoid credit usage  -->

📁 [Week 4 Folder](./Week4)

---

### ✅ Week 5: NSG, ASG & IP Management in Azure
**Duration: July 1 – July 6, 2025**<br>
**Topics Covered:**
- Network Security Groups (NSGs): Purpose, working, and rule configuration
- Application Security Groups (ASGs): Logical grouping of VMs
- Allowing specific IPs to access Azure VMs via NSG
- Denying Internet access using outbound NSG rules
- Public IPs: Static vs Dynamic and how to assign them
- Service Tags in Azure (e.g., Internet, VirtualNetwork, AzureLoadBalancer)
- Creating and managing Network Interfaces (NICs)

**Tasks Completed:**
- 📄 R&D Document: NSG, ASG, IP Management, and Network Interface Configuration in Azure
<!-- ✅ Created and associated NSGs with subnets/NICs
✅ Created inbound rule to allow only specific IP access to VMs
✅ Configured outbound NSG rule to deny internet access from a VM
✅ Created static Public IP addresses and associated them with VMs
✅ De-associated Public IPs from NICs for cleanup testing
✅ Created ASGs and linked VMs to them
✅ Applied NSG rules based on ASG membership
✅ Created additional NIC manually and attached to VM
🖼️ Collected portal screenshots of each task and configuration
✅ Verified connectivity and rule enforcement
🧹 Cleaned up all created resources to preserve free-tier credits -->

📁 [Week 5 Folder](./Week5)

---

### ✅ Week 6: Tiered Architecture Deployment with NSG and Server Setup
**Duration: July 7 – July 13, 2025**<br>
**Topics Covered:**
- Azure Virtual Network Architecture Design
- Subnet Planning: Web, App, DB tiers
- Network Security Groups (NSG) configuration
- Public & Private IP setup
- Apache and IIS Server Installation
- Intra-tier and inter-tier connectivity verification via ICMP (ping)

**Tasks Completed:**
- 📁 R&D Document: Tiered Application Deployment in Azure with Subnetting, NSG Configuration, and Server Setup 
<!-- 🌐 Created three subnets:
WebSubnet (10.0.1.0/24)
AppSubnet (10.0.2.0/24)
DBSubnet (10.0.3.0/24)
💻 Deployed 6 VMs (1 Linux + 1 Windows in each subnet)
🔐 Configured NSGs to allow/block traffic between tiers:
Web → App ✅
App → Web & DB ✅
DB → Web/App ❌
🖥️ Installed Apache Server on Linux VMs using terminal
Verified using curl http://localhost
🖥️ Installed IIS Server on Windows VMs via PowerShell
🔁 Verified inter-VM connectivity using ping tests
📝 Documented observations, screenshots, and deviations
App and DB VMs didn’t have public IPs → Used jump box method via WebLinux
Performed quota check and VM core limit resolution -->

📁 [Week 6 Folder](./Week6)

---

### ✅ Week 7: Internal Load Balancer Deployment & Load Balancing in Azure
**Duration: July 14 – July 20, 2025**<br>
**Topics Covered:**
- Azure Load Balancer: Concepts & Types (Internal vs External)
- Layer 4 load balancing using 5-tuple hash
- Frontend IP, Backend Pool, Health Probes
- Load Balancing Rule vs Inbound NAT Rule
- Static vs Dynamic Public IP limitations (Student Subscription)
- Internal connectivity using private IP
- SSH using key-based authentication
- Load balancing traffic across backend VMs using nginx

**Tasks Completed:**
- 📄 R&D on Azure Load Balancer Implementation
<!-- 🔁 Created 3 Linux VMs in the same subnet with nginx installed and unique index pages (VM1, VM2, VM3)
🔐 Connected via SSH using private key and terminal
⚙️ Created Internal Load Balancer with:
Private frontend IP: 10.0.1.10
Backend pool (VM1, VM2, VM3 NICs)
Health Probe (HTTP on port 80)
Load balancing rule (TCP 80 to 80)
📟 Verified load balancing by running curl 10.0.1.10 from VM4 in same subnet
🖼️ Screenshots included:
Public IPs of VMs
SSH Output + nginx response per VM
Internal Load Balancer setup
Error while trying to create external load balancer (quota limit) -->

📁 [Week 7 Folder](./Week7)

---

### ⏳ Week 8: *(To be updated...)*
_Stay tuned for upcoming learnings and contributions._

---

### 🌟 Main Internship Project: Azure Privileged Identity Management (PIM)

<b>Project Overview:</b>As part of my internship at Celebal Technologies, I worked on a comprehensive project focused on Azure Privileged Identity Management (PIM), a critical feature of Microsoft Entra ID for managing, controlling, and monitoring privileged access in Azure environments. The project involved researching, documenting, and implementing PIM to enforce just-in-time (JIT) access, approval workflows, and audit trails, aligning with the principle of least privilege to enhance security.

**Tasks Completed:**
- 📄 Project Report on Provileged Identity Management
- Introduction to PIM and its key features (JIT access, approval workflows, audit trails).
- Setup prerequisites (Azure AD Premium P2 licensing, admin roles).
- Configuring Azure AD roles and Azure resource roles in PIM.
- Setting up privileged access groups and approval processes.
- Managing break-glass accounts and analyzing audit history.
- Exploring eligible vs. active roles and setting role time limits.
- Advanced features like Azure Monitor integration and PowerShell automation.
- Case studies and troubleshooting guides.

**🛠️ Attempted practical implementation of PIM in Azure Portal, including:**
- Assigning roles to users and groups.
- Configuring role settings (e.g., MFA, approval requirements).
- Testing JIT access activation.
- Creating privileged access groups and setting up approval workflows.
- Documented challenges faced during implementation.
- 🖼️ Included placeholders for screenshots of key configurations (e.g., role assignments, audit logs, approval workflows).

📁 [Main-Project](./Main-Project)

**Future Steps:**
- Work with tenant administrators to clarify student plan restrictions.
- Test PIM implementation on a trial or pay-as-you-go subscription.
- Enhance the PIM document with additional case studies and automation scripts.

---

## 🔍 About Me

👩‍💻 *Nandini Goyal*  
🎓 B.Tech CSE | Amity University Rajasthan  
🌐 Exploring Cloud | Passionate about Cybersecurity & Infrastructure

---

## 🚀 Goals for this Internship

- Strengthen understanding of cloud architecture and protocols.
- Gain hands-on experience in infrastructure security.
- Build real-world project exposure in Cloud & DevOps.

---

## 📫 Connect with Me

- [LinkedIn](https://www.linkedin.com/in/nandini-goyal-6b9116259/)
- [GitHub](https://github.com/NandiniGoyal16)
- [Gmail](nandinio4.goyal@gmail.com)

---

> “Learning never exhausts the mind.” — Leonardo da Vinci
