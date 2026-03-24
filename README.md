# osTicket Helpdesk Lab — Deployed on AWS EC2

![osTicket](https://img.shields.io/badge/osTicket-v1.18.1-blue)
![AWS](https://img.shields.io/badge/AWS-EC2%20Free%20Tier-orange)
![Stack](https://img.shields.io/badge/Stack-LAMP-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A fully functional helpdesk ticketing system deployed on AWS EC2 using the LAMP stack. This lab simulates real-world IT support operations including ticket triage, SLA management, department routing, escalation workflows, and canned responses.

---

## 📸 Screenshots

| User Support Portal | Successful Installation |
|---------------------|------------------------|
| ![Portal](screenshots/Platform.png) | ![Install](screenshots/osticket.png) |

| Agent Ticket Queue | Admin Dashboard |
|--------------------|----------------|
| ![Agent Panel](screenshots/Agent_Panel.png) | ![Admin Panel](screenshots/Admin_Panel.png) |

---

## 🏗️ Architecture

```
[User's Browser]
      ↓
[Apache - Web Server]       ← handles HTTP on port 80
      ↓
[PHP - Application Layer]   ← runs osTicket logic
      ↓
[MySQL - Database]          ← stores tickets, users, SLAs
      ↑
[AWS EC2 t2.micro]          ← Ubuntu 22.04, Free Tier
```

---

## ⚙️ Tech Stack

| Component | Technology |
|-----------|------------|
| Cloud | AWS EC2 (t2.micro, Free Tier) |
| OS | Ubuntu Server 22.04 LTS |
| Web Server | Apache 2 |
| Database | MySQL 8 |
| App Language | PHP 8 |
| Ticketing App | osTicket v1.18.1 |

---

## 🚀 What I Built & Configured

### Infrastructure
- Launched and configured an EC2 instance with a custom Security Group
- Installed and configured the full LAMP stack from scratch
- Set proper file permissions and secured MySQL post-install

### osTicket Configuration
- **Departments:** IT Support, Network & Infrastructure, HR Helpdesk
- **SLA Tiers:**
  - P1 Critical — 1 hour response, 24/7
  - P2 High — 4 hour response, 24/7
  - P3 Normal — 8 hour response, business hours
- **Help Topics:** Password Reset, Hardware Issue, Software Install, Network Connectivity, New Employee Onboarding
- **Agents & Roles:** Multiple agents across departments with manager/agent role separation
- **Canned Responses:** Pre-written replies for common ticket types

### Ticket Lifecycle Simulation
- Submitted tickets as an end user via the Support Center portal
- Triaged, assigned, prioritized, and resolved tickets as an agent
- Practiced internal notes, ticket transfers, and escalations
- Simulated overdue tickets and SLA breach scenarios

---

## 📋 Skills Demonstrated

- Linux server administration (Ubuntu)
- AWS EC2 and Security Group configuration
- LAMP stack deployment and configuration
- MySQL database administration
- Apache virtual host configuration
- IT helpdesk operations and ticket lifecycle management
- SLA planning and queue management
- Role-based access control

---

## 🔧 Setup Guide

Full step-by-step instructions in [SETUP.md](./SETUP.md)

**Quick overview:**
1. Launch EC2 t2.micro (Ubuntu 22.04)
2. Install Apache, MySQL, PHP + extensions
3. Download and deploy osTicket v1.18.1
4. Configure Apache virtual host
5. Run web installer
6. Post-install: lock config file, delete setup folder

---

## 📁 Repository Structure

```
osticket-aws-lab/
├── README.md
├── SETUP.md
├── screenshots/
│   ├── Platform.png        ← User-facing support portal
│   ├── osticket.png        ← Successful installation page
│   ├── Agent_Panel.png     ← Agent ticket queue
│   └── Admin_Panel.png     ← Admin dashboard & system logs
└── config/
    └── osticket.conf       ← Apache virtual host config
```

---

## 💡 Key Takeaways

Working through this project gave me hands-on experience with how enterprise helpdesk environments are structured — from infrastructure provisioning to end-user support workflows. Setting up SLA tiers and watching how ticket priority affects queue routing made abstract ITIL concepts much more concrete.

---

## 🔗 Full Write-Up

Medium article: _add link_
