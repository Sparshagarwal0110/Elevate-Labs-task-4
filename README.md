# Elevate-Labs-task-4

# 🔒 Task 4: Setup and Use a Firewall on Windows

## 🎯 Objective
Configure and test basic firewall rules to allow or block traffic using Windows Defender Firewall.

---

## 🛠️ Tools Used
- **OS**: Windows 11
- **Firewall**: Windows Defender Firewall with Advanced Security

---

## 🧾 Step-by-Step Guide

### 1. 🚪 Open Firewall Settings
- Go to `Control Panel > System and Security > Windows Defender Firewall`.
- Click **Advanced Settings** on the left.

### 2. 🚫 Block Inbound Traffic on Port 23 (Telnet)
- In **Inbound Rules**, click **New Rule**.
- Select **Port** → Click **Next**.
- Choose **TCP**, enter **23**, click **Next**.
- Select **Block the connection** → Click **Next**.
- Name the rule `Block Telnet` and finish.

### 3. 🧪 Test the Block
- Try:  
  - `telnet localhost 23`  
  - Or scan from another machine using `nmap <Windows_IP> -p 23`
- It should **fail to connect**.

### 4. 🔓 Allow Inbound SSH (Port 22)
> Only if OpenSSH Server is installed on Windows.

- In **Inbound Rules**, click **New Rule**.
- Select **Port** → Choose **TCP**, enter **22**.
- Select **Allow the connection**.
- Name the rule `Allow SSH`.

### 5. ❌ Remove Telnet Block Rule
- In **Inbound Rules**, right-click `Block Telnet`.
- Choose **Delete** to remove the rule.

---

## 📸 Screenshot (Attach here)
> Screenshot showing:
> - Block rule for port 23

---

## 📘 Summary: How Firewalls Filter Traffic

Windows Firewall acts as a barrier between the system and external networks:
- It inspects traffic and applies rules based on:
  - **Ports**
  - **Protocols**
  - **Applications**
- **Block rules** prevent unwanted/insecure traffic (e.g., Telnet).
- **Allow rules** enable trusted services (e.g., SSH or RDP).

This ensures only safe and intended communication is allowed.

---

## ✅ Final Status Check
- In **Windows Firewall with Advanced Security**, verify active rules.

---

## 🔚 End of Report
