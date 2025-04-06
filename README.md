# 🎫 osTicket - Prerequisites and Installation Guide

This repository outlines the setup and installation of the open-source help desk ticketing system [osTicket](https://osticket.com/). It's perfect for system admins or students looking to learn how ticketing systems work in an IT environment.

---

## 🖥️ Environment Used

- **Microsoft Azure** – Virtual Machines
- **Windows 10** – Client Machine
- **Windows Server 2019** – Domain Controller / Web Server
- **Remote Desktop Protocol (RDP)**
- **Internet Information Services (IIS)**

---

## ⚙️ Technologies Used

- **osTicket v1.15.8**
- **PHP Manager for IIS**
- **MySQL Database**
- **PHP 7.3**
- **HeidiSQL**

---

## 🧾 Prerequisites

Before installation, ensure you have the following:

- Azure account with at least two VMs (one client, one server)
- IIS installed with necessary roles
- PHP, MySQL, and PHP Manager installed
- Ports opened via **Network Security Group**
- File download permissions enabled via browser

---

## 🛠️ Installation Steps

1. **Install IIS and Required Features**
   - Enable: CGI, Common HTTP Features, Web Server
   - Download & install PHP Manager for IIS

2. **Install and Configure PHP**
   - Install PHP 7.3
   - Configure PHP path in IIS Manager using PHP Manager

3. **Install MySQL**
   - Download MySQL Server
   - Create a root password and remember it for osTicket config

4. **Install HeidiSQL (Optional)**
   - Makes managing MySQL easier via GUI

5. **Download and Extract osTicket**
   - [Download osTicket](https://osticket.com/download)
   - Extract to: `C:\inetpub\wwwroot\osTicket`

6. **Configure IIS for osTicket**
   - Set `osTicket` as a site or under default site
   - Ensure correct permissions (IUSR, IIS_IUSRS)

7. **Run the osTicket Setup Wizard**
   - Visit `http://localhost/osTicket` or your VM's IP
   - Complete the setup (DB info, admin user)

8. **Secure Installation**
   - Delete `/setup` folder after install
   - Rename `config.php` permissions to Read-Only

---

## ✅ Post-Installation

- Log in as Admin 
- Customize help topics, agents, SLA plans, etc.
- Ensure your cron jobs are configured

