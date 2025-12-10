# N8N-workflow-simple-automation
A collection of easy-to-use n8n automation workflows for everyday tasks. Includes simple examples, templates, and integrations to help beginners build efficient automated processes quickly and effortlessly.
<img width="1058" height="394" alt="image" src="https://github.com/user-attachments/assets/d1bf0be3-11f2-4807-875d-29628e3f685d" />

## 🔧 What you’ll find here

-Ready-to-use n8n workflows
-Step-by-step automation examples
-Integrations with popular apps and APIs
-Helpful notes and best practices for building your own workflows

## 🎯 Purpose

To provide a clean, organized place for lightweight automations that anyone can copy, adapt, and run in their own n8n instance.

## 🤝 Contributions

Feel free to add your own simple automations or improve existing ones!

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Deployment Guide

---
### 🌐 Deploy & Use n8n (Official Cloud)
n8n Cloud is the easiest and fastest way to start using n8n. It requires no installation, no server setup, and no maintenance. Everything runs on the official n8n infrastructure with built-in security and automatic updates.
<img width="1648" height="831" alt="image" src="https://github.com/user-attachments/assets/9b737aaf-9acb-4772-9a9d-69741a687f1a" />
[This image is taken on 2025-12-10. When you see this image the pricing and plans may be changed.]

---
## 🚀 How to Deploy & Use n8n on the Cloud (Step-by-Step)

### 1. Go to the n8n Cloud Portal
Visit the official cloud platform:
👉 https://app.n8n.cloud

### 2. Create an Account or Sign In
You can sign up using:

* Email & password
* Google account
* GitHub account

### 3. Create Your Workspace
After signing in:
- Click Create Workspace
- Choose a workspace name
- Select your region
- Choose your plan (Starter, Pro, or Enterprise)<br><br>
Your workspace will be created automatically within seconds.

### 🖥️ 4. Access Your n8n Dashboard
Once the workspace is ready:
- Click Open n8n Editor
- You will be redirected to the workflow editor (your automation canvas)<br><br>
This is where you build, edit, and manage all workflows.

### ⚙️ 5. Create Your First Workflow
1. Click New Workflow
2. Drag and drop nodes (e.g., HTTP Request, Google Sheets, Telegram, Slack, MySQL, etc.)
3. Connect the nodes
4. Click Execute Workflow to test<br><br>
n8n executes each node and shows their output clearly.

### 🔄 6. Activate the Workflow
Once tested:
1. Turn ON the Activate switch
2. Your workflow now runs automatically based on triggers such as:
3. Cron
4. Webhook
5. App integrations
6. Scheduled events

Database changes (depending on nodes)

### 🔐 7. Manage API Keys & Credentials

n8n Cloud provides secure credential handling.<br>
You can add credentials for: Google Services, Slack, Telegram, Notion, GitHub, Airtable, Stripe, …and many more.

All credentials are stored securely in the n8n cloud environment.

### 📊 8. Monitor Executions

In your workspace:

- Go to Executions
- Check:
    - Success logs
    - Failures
    - Runtime
    - Input/Output data

Errors can be debugged easily with detailed logs.

### 💾 9. Backups & Updates (Automatic)

n8n Cloud automatically handles:

- Backups
- Security patches
- Performance updates
- Infrastructure scaling

No manual maintenance is required.

---
## ⭐ Benefits of Using n8n Cloud

- Zero setup — start in minutes

- Secure hosting by the n8n team

- Automatic updates, backups, and monitoring

- No server or DevOps needed

- Scalable & reliable environment

- Fastest way to begin using n8n

- Ideal for individuals, teams, and businesses

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 🏠 Deploy & Use n8n (Self-Hosted)

Self-hosting n8n gives you full control, unlimited usage, and the ability to run automation on your own infrastructure. You can deploy n8n on various platforms depending on your technical preference and environment.

### 📦 Self-Hosting Options Available

You can run n8n on:

#### 1. Docker / Docker Compose (Recommended)

Most stable and easiest to maintain.

#### 2. Linux Server Installation (Node.js + npm)

For custom environments and lightweight setups.

#### 3. Windows / macOS Local Installation

Good for development or testing.

#### 4. Cloud Providers

AWS, Google Cloud, Azure, DigitalOcean, Hetzner, Vultr, etc.

#### 5. Kubernetes (Helm Chart)

For scaling and production workloads.

#### 6. Raspberry Pi / ARM-based Devices

For home labs or low-cost automation projects.

---
### 🚀 Deploy n8n Using Docker (Recommended Method)

#### 1. Install Docker & Docker Compose

Follow installation steps for your OS:
https://docs.docker.com/get-docker/

#### 2. Create a docker-compose.yml File
```
version: '3'
services:
  n8n:
    image: n8nio/n8n
    ports:
      - "5678:5678"
    volumes:
      - ./n8n_data:/home/node/.n8n
    environment:
      - N8N_BASIC_AUTH_ACTIVE=true
      - N8N_BASIC_AUTH_USER=admin
      - N8N_BASIC_AUTH_PASSWORD=yourpassword
```
#### 3. Start n8n
```
docker-compose up -d
```
#### 4. Access n8n

Open your browser and go to:
👉 http://localhost:5678

---

### 🖥 Install n8n on Linux (Node.js)

#### 1. Install Node.js (LTS)
```
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
```
#### 2. Install n8n globally
```
npm install -g n8n
```
#### 3. Start n8n
```
n8n start
```

Access at: http://localhost:5678

---

### 🪟 Install on macOS or Windows (Local Development)

#### 1. Install Node.js

Download LTS version from: https://nodejs.org/

#### 2. Install n8n
```
npm install -g n8n
```

#### 3. Run n8n
```
n8n start
```

--- 
### ☁ Deploy on Cloud Providers

You can deploy n8n on any cloud using Docker or Node.js. Popular choices:
- AWS EC2 (most flexible)
- Google Cloud Compute Engine
- Microsoft Azure VM
- DigitalOcean Droplets (easy for beginners)
- Hetzner Cloud (low cost)
- Vultr / Linode

Basic steps:
1. Create a Linux server (Ubuntu recommended)
2. Install Docker or Node.js
3. Deploy n8n using the instructions above

Set up a domain and reverse proxy (optional but recommended)

---

### ☸ Deploy on Kubernetes (Helm)

For production-grade scaling.

#### 1. Add the n8n Helm repo
```
helm repo add n8n https://helm.n8n.io/
```

#### 2. Install n8n
```
helm install n8n n8n/n8n
```

---

###🧪 Deploy on Raspberry Pi / ARM

Use the ARM-compatible Docker image:
```
docker pull n8nio/n8n:latest-rpi
```
Follow the same Docker Compose steps.

---

## ⭐ Benefits of Self-Hosting n8n

- Complete control over your data and infrastructure

- Unlimited workflows and executions

- Integrate with internal/private systems

- Customizable configuration & environment variables

- Cost-efficient (use your own server)

- Can scale with Docker, Docker Swarm, or Kubernetes

- Run locally, offline, or in secure environments

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 📘 Final Notes

This repository is designed to help you easily explore, understand, and use n8n automations—whether you're using the official n8n Cloud or deploying n8n on your own self-hosted environment. Each guide, workflow, and instruction is created to be beginner-friendly, practical, and ready to use.

By following the steps above, you can:

- Start instantly with n8n Cloud, the fastest and easiest option

- Deploy n8n on your own infrastructure for full control and unlimited usage

- Build, test, and activate powerful automation workflows

- Learn best practices to scale your automations over time

This repository will continue to grow with more workflows, templates, and guides designed to save time, simplify processes, and help you automate anything—your way.
