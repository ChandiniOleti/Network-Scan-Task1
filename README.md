# 🔍 Task 1 – Network Reconnaissance with Nmap

## 📌 Objective
The goal of this task is to learn **basic network reconnaissance** by scanning the local network for open ports using **Nmap** in Kali Linux.

Key Concepts:  
- Port Scanning  
- TCP SYN Scan  
- IP Ranges  
- Open Ports & Security Risks  
- Network Reconnaissance Basics  

---

## ⚙️ Tools Used
- **Kali Linux**
- **Nmap v7.94SVN**
- **(Optional)** Wireshark for packet analysis

---

## 🖥️ Steps Performed

### 1. Verified Nmap Installation
```bash
nmap --version
Output:
Nmap version 7.94SVN ( https://nmap.org )
Platform: x86_64-pc-linux-gnu

2. Found Local IP Address
ip a
My machine IP:
192.168.1.104/24
So the network range to scan was:
192.168.1.0/24

3. Performed TCP SYN Scan
sudo nmap -sS 192.168.1.0/24
📊 Results
3 hosts detected in the local network.

🔹 Host 1 – 192.168.1.1 (Router)
53/tcp   open  domain
80/tcp   open  http
443/tcp  open  https
1900/tcp open  upnp
🔹 Host 2 – 192.168.1.204 (Windows / Database Server)
135/tcp  open  msrpc
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
3306/tcp open  mysql
6646/tcp open  unknown
🔹 Host 3 – 192.168.1.104 (My Kali Machine)
All 1000 scanned ports closed
