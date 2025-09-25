# Basic Vulnerability Scan — Task 3

This repository contains the deliverables for the Basic Vulnerability Scan task.

## Contents
- `reports/` — exported scan reports (PDF and raw).
- `screenshots/` — screenshots showing the scan setup, progress and sample vulnerability.
- `notes/vulnerabilities.md` — short descriptions and proposed remediation for the top findings.

## How I ran the scan
- Tool: Nessus Essentials (or OpenVAS/GVM)
- Target: 127.0.0.1 / local machine IP
- Scan type: Basic Network Scan / Full and Fast

## Top findings (example)
1. Vulnerability Title — CVSS: 7.5  
   - Evidence: open port 445, outdated SMB  
   - Fix: disable SMBv1 and apply Windows updates.  

