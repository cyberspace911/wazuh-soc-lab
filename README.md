# Wazuh SIEM + Mailcow Mail Server SOC Lab

## 📋 Overview

This project implements a Security Operations Center (SOC) laboratory environment with:

- **Wazuh SIEM** v4.9.0 - Security information and event management
- **Mailcow** - Dockerized mail server (18 containers) with Rspamd spam filtering
- **Custom log collection** - Bash scripts + cron for Docker container logs
- **Security monitoring** - 809+ security alerts generated and analyzed

## 🏗️ Architecture

- **SOC Server** (192.168.1.16): Ubuntu 24.04, Wazuh SIEM (Docker)
- **Mail Server** (192.168.1.15): Ubuntu 24.04, Mailcow (18 containers), Wazuh Agent
- **Log Collection**: Custom scripts + cron (every minute)

## 🚀 Features

- ✅ Centralized log collection from 18 Docker containers
- ✅ Real-time security alerts for email threats (phishing, spam)
- ✅ 809+ security events generated and analyzed
- ✅ Custom log collection with Bash scripts and cron
- ✅ Active agent monitoring mail server (192.168.1.15)

## 📊 Deployed Agents

| Agent ID | Hostname | IP Address | OS | Version | Status |
|----------|----------|------------|-----|---------|--------|
| 001 | ubuntuu | 192.168.1.15 | Ubuntu 24.04 | v4.9.0 | ✅ Active |

## 🛠️ Technologies Used

- **SIEM**: Wazuh v4.9.0, OpenSearch
- **Mail Server**: Mailcow (18 containers), Postfix, Dovecot, Rspamd
- **Container Platform**: Docker, Docker Compose
- **OS**: Ubuntu 24.04 LTS
- **Scripting**: Bash, Cron

## 🔧 Quick Start

### Prerequisites
- Ubuntu 24.04 VMs
- Docker and Docker Compose

### Basic Commands

**SOC Server:**
```bash
git clone https://github.com/wazuh/wazuh-docker.git
cd wazuh-docker/single-node
docker compose up -d
