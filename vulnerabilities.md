# Vulnerabilities — Expanded Notes
_Generated: 2025-09-25 11:08 UTC_

This file expands each simulated finding with context and remediation steps.

## 1. OpenSSL Heartbleed-like Vulnerability (Simulated)  (High)
- **Port / Service:** 443/tcp (https)
- **CVE:** CVE-2014-0160 (example)
- **CVSS (simulated):** 7.5
- **Evidence:** OpenSSL 1.0.1f detected in service banner (simulated)
- **Description:** A simulated Heartbleed-like memory disclosure vulnerability allowing remote attackers to read server memory.
- **Remediation:**
  - Upgrade OpenSSL to a version without the heartbeat vulnerability (e.g.,
  - >=1.0.1g). Apply vendor patches and restart services.

## 2. SMBv1 Server Enabled  (Critical)
- **Port / Service:** 445/tcp (microsoft-ds)
- **CVE:** N/A (configuration issue)
- **CVSS (simulated):** 9.1
- **Evidence:** SMBv1 protocol detected via banner (simulated)
- **Description:** SMBv1 is insecure and has known critical vulnerabilities (e.g., WannaCry).
- **Remediation:**
  - Disable SMBv1 on the host and enable SMBv2/SMBv3. Apply all OS security updates.

## 3. Outdated Apache HTTP Server (Directory Traversal Risk)  (Medium)
- **Port / Service:** 80/tcp (http)
- **CVE:** CVE-2017-9798 (example)
- **CVSS (simulated):** 6.8
- **Evidence:** Apache/2.2.15 detected in server header (simulated)
- **Description:** Older Apache versions may be susceptible to directory traversal and other issues.
- **Remediation:**
  - Update Apache to the latest stable release, review document root permissions,
  - and disable mod_autoindex if unnecessary.

## 4. Weak SSH Ciphers and MAC Algorithms  (Medium)
- **Port / Service:** 22/tcp (ssh)
- **CVE:** N/A (configuration)
- **CVSS (simulated):** 5.3
- **Evidence:** Server supports 3des-cbc, hmac-sha1 (simulated)
- **Description:** The SSH service is allowing weak ciphers and MACs which can be susceptible to cryptographic attacks.
- **Remediation:**
  - Reconfigure SSH to use strong ciphers (e.g., aes256-gcm@openssh.com) and strong
  - MACs. Restart sshd.

## 5. Default Credentials — Web Management Interface  (High)
- **Port / Service:** 8080/tcp (http-proxy)
- **CVE:** N/A (auth issue)
- **CVSS (simulated):** 8.0
- **Evidence:** Default admin:admin credentials accepted on /admin (simulated)
- **Description:** Web management interface accessible with default credentials allowing administrative access.
- **Remediation:**
  - Change default passwords, enforce strong password policy, restrict management
  - interface to trusted networks or enable MFA.

## 6. Insecure HTTP (Missing HSTS and TLS Weaknesses)  (Low)
- **Port / Service:** 80/tcp (http)
- **CVE:** N/A (configuration)
- **CVSS (simulated):** 4.3
- **Evidence:** No HSTS header; TLS 1.0 supported (simulated)
- **Description:** HTTP connections and weak TLS versions expose traffic to interception and downgrade attacks.
- **Remediation:**
  - Redirect HTTP to HTTPS, enable HSTS, and disable TLS 1.0/1.1. Use TLS 1.2+ and
  - modern cipher suites.

## 7. Outdated SMB Client Signing Not Required  (Medium)
- **Port / Service:** 445/tcp (microsoft-ds)
- **CVE:** N/A (configuration)
- **CVSS (simulated):** 6.5
- **Evidence:** SMB signing not required (simulated)
- **Description:** SMB client signing not required may allow man-in-the-middle attacks on SMB sessions.
- **Remediation:**
  - Require SMB signing via group policy or system config and ensure clients are
  - updated.

## 8. Localhost Unnecessary Service: FTP Running  (Low)
- **Port / Service:** 21/tcp (ftp)
- **CVE:** N/A (insecure service)
- **CVSS (simulated):** 3.7
- **Evidence:** FTP service banner: vsftpd 2.0.5 (simulated)
- **Description:** FTP transmits credentials in cleartext. Unnecessary services increase attack surface.
- **Remediation:**
  - Disable FTP if not required or replace with SFTP (SSH-based). Enforce secure
  - file transfer methods.
