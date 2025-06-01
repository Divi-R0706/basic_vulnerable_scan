# 🔒 Basic Vulnerability Scan Report

This project contains a basic manual vulnerability scan of a Windows 10 system using built-in tools, without any third-party scanners.

## 🗓️ Date
01 June 2025

## 🖥️ System Information
- **OS**: Windows 10 Pro (Version 10.0.26100.4061)
- **IP Address**: 192.168.14.221

## 🧪 Methodology
- Manual scan using:
  - `ipconfig`
  - `systeminfo`
  - `netstat -an | find "LISTEN"`
  - (Optional) PowerShell: `Get-NetTCPConnection`
- No external tools (OpenVAS/Nessus) used.

## 📋 Key Findings

| Port | Service | Risk Level | Action |
|------|---------|------------|--------|
| 445  | SMB     | High       | Disable SMBv1 |
| 139  | NetBIOS | High       | Block externally |
| 135  | RPC     | Medium     | Restrict access |
| Others | Various | Medium-Low | Review & monitor |

## 🧷 References
- [CVE-2017-0144 (SMB)](https://nvd.nist.gov/vuln/detail/CVE-2017-0144)
- [Microsoft SMB Security](https://learn.microsoft.com/en-us/windows/security)

## 📸 Screenshots
All outputs and evidence are included in the `/screenshots` folder.

---

📘 *This project demonstrates basic vulnerability scanning and awareness using default system tools.*
