nano ~/firewall-task-report/firewall-configuration-report.md
# 🔐 Linux Firewall Report: Firewall Configuration on Kali Linux

## 🧭 Objective
To configure and test firewall rules using UFW (Uncomplicated Firewall) in Kali Linux. This task demonstrates how to block and allow specific ports, verify rule effectiveness, and restore original settings—all while documenting the process for reproducibility.

---

## 🛠️ Tools Used

| Tool        | Purpose                                 |
|-------------|------------------------------------------|
| UFW         | Linux firewall configuration             |
| Telnet      | Testing blocked port connectivity        |
| Nano        | Editing and saving the report file       |
| Terminal    | Command-line execution and scripting     |

---

## 📡 Ports Involved

| Port | Service | Action     | Reason                          |
|------|---------|------------|----------------------------------|
| 23   | Telnet  | Blocked    | Simulate vulnerable service      |
| 22   | SSH     | Allowed    | Ensure remote access remains     |

---

## 🧪 Step-by-Step Commands

### 1. Install and Enable UFW
```bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable
sudo ufw status numbered
sudo ufw deny 23
telnet localhost 23
sudo ufw allow 22
sudo ufw status numbered
sudo ufw delete [rule_number]


