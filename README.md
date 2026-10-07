# Nmap Network Scanning

## 📌 Project Overview

This is a beginner cybersecurity task using **Nmap** to scan my own computer and understand open ports and running services.

I used Nmap on Windows and scanned `127.0.0.1` (localhost).

## 🎯 Objectives

* Learn basic Nmap commands
* Identify open and closed ports
* Detect running services
* Understand basic network discovery
* Practice a beginner SOC Analyst task

## 🛠️ Tool Used

* Nmap
* Windows Command Prompt

## 🔍 Commands Used

### 1. Check Nmap installation

```cmd
nmap --version
```

### 2. Scan localhost

```cmd
nmap 127.0.0.1
```

### 3. Detect services and versions

```cmd
nmap -sV 127.0.0.1
```

### 4. Check PostgreSQL

```cmd
nmap -sV -p 5432 127.0.0.1
```

### 5. Check Splunk

```cmd
nmap -sV -p 8000 127.0.0.1
```

## 📊 Findings

The scan identified several open ports on my local Windows system.

| Port | Service               |
| ---- | --------------------- |
| 135  | Microsoft Windows RPC |
| 445  | Microsoft-DS / SMB    |
| 902  | VMware Authentication |
| 912  | VMware Authentication |
| 5357 | WSDAPI                |
| 5432 | PostgreSQL            |
| 8000 | Splunkd               |
| 8089 | Unknown               |
| 8194 | HTTP service          |

The scan also showed many closed TCP ports.

## 🔎 Key Observation

Port **8000** was identified as **Splunkd**, which matched my Splunk installation.

Port **5432** was identified as **PostgreSQL DB**.

Some ports were not fully identified by Nmap, showing that further investigation may be required.

## 📸 Screenshots

### Nmap Localhost Scan

![Nmap Localhost Scan](screenshots/nmap-localhost-scan.png)

### Nmap Service Detection

![Nmap Service Detection](screenshots/nmap-service-detection.png)

### Splunk Port Detection

![Splunk Port Detection](screenshots/nmap-splunk-port.png)

### PostgreSQL Port Detection

![PostgreSQL Port Detection](screenshots/nmap-postgresql-port.png)

## 📚 What I Learned

* How to install and verify Nmap
* How to scan a local system
* How to identify open and closed ports
* How to use `-sV` for service detection
* How to identify services running on specific ports
* Basic network discovery concepts
* How port information can support SOC investigations

## 🛡️ Security Note

This task was performed only against my own computer (`127.0.0.1`) for learning and cybersecurity practice.
