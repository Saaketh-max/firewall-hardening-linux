# firewall-hardening-linux
# 🔐 Linux Firewall Report: Firewall Configuration on Kali Linux

## 🧭 Objective
To configure and test firewall rules using UFW (Uncomplicated Firewall) in Kali Linux. This task demonstrates how to block and allow specific ports, verify rule effectiveness, and restore original settings—all while documenting the process for reproducibility.

---

## 🛠️ Tools Used

| Tool        | Purpose                                 |
|-------------|------------------------------------------|
| **UFW**     | Linux firewall configuration             |
| **Telnet**  | Testing blocked port connectivity        |
| **Nano**    | Editing and saving the report file       |
| **Terminal**| Command-line execution and scripting     |

---

## 📡 Ports Involved

| Port | Service | Action     | Reason                          |
|------|---------|------------|----------------------------------|
| 23   | Telnet  | Blocked    | Simulate vulnerable service      |
| 22   | SSH     | Allowed    | Ensure remote access remains     |

---

## 🧪 Step-by-Step Commands

# Step 1: Update system and install UFW
sudo apt update
sudo apt install ufw -y

# Step 2: Enable UFW firewall
sudo ufw enable

# Step 3: List current firewall rules
sudo ufw status numbered

# Step 4: Block inbound traffic on port 23 (Telnet)
sudo ufw deny 23

# Step 5: Test the rule locally (Telnet should fail)
telnet localhost 23

# Step 6: Allow SSH traffic on port 22
sudo ufw allow 22

# Step 7: List rules again to find rule number for port 23
sudo ufw status numbered

# Step 8: Remove the Telnet block rule (replace X with actual rule number)
sudo ufw delete X


🛠️ Tools Used in Firewall Configuration Task
Tool	Purpose
UFW	Uncomplicated Firewall — used to configure and manage firewall rules
Telnet	Used to test connectivity to blocked ports (e.g., port 23 for Telnet)
SSH	Secure Shell — verified access through allowed port (port 22)
Nano	Terminal-based text editor — used to write and save the report file
Terminal	Command-line interface — used to execute all firewall and testing steps
Git	Version control — used to track changes and push the report to GitHub
GitHub CLI (gh)	

📡 Ports Involved
Port	Service	Action	Purpose
23	Telnet	Blocked	Simulate blocking insecure traffic
22	SSH	Allowed	Maintain secure remote access

🧪 Key Steps Performed

    Installed and enabled UFW

    Listed current firewall rules

    Blocked inbound traffic on port 23

    Tested the block using Telnet

    Allowed SSH on port 22

    Removed the Telnet block rule

    Documented all commands and observations

    🧠 Firewall Summary

A firewall filters traffic by inspecting packets and applying rules based on port, protocol, and direction. UFW simplifies this process with readable commands like allow and deny. This task simulates real-world security hardening by disabling Telnet and preserving SSH access.

📁 Deliverables

    Markdown report with all commands and explanations

    Screenshots of rule status and Telnet test

    GitHub repository with structured documentation



