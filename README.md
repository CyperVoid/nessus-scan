# Nessus Scan Report

This repository contains a clean and organized version of your Nessus scan task and findings.

---

##  1. Scan Setup
- **Type of Scan:** Basic Network Scan
- **Target IP:** `127.0.0.1`
- **Duration:** 30 minutes

---

##  2. Scan Summary
| Severity | Count |
|---------|-------|
| Critical | 0 |
| High | 0 |
| Medium | 1 |
| Low | 0 |
| Informational | 18 |

---

##  3. Key Vulnerabilities Identified
###  Medium Vulnerability 1
**Name:** SMB Signing Not Required  
**Affected Port/Service:** `445 / tcp / cifs`  
**Risk:** Allows attackers to perform Man‑in‑the‑Middle (MITM) attacks.  

####  Recommendation
- Enable SMB signing in Windows security policies.
- Ensure latest Windows security patches are applied.

---

##  4. Observations
- Nessus detected **1 Medium vulnerability** and **18 informational findings**.
- Informational findings do not pose direct risk but provide insights into services/configurations that could be abused when combined with other vulnerabilities.
- The main concern is **disabled SMB signing**, which increases susceptibility to MITM attacks.

---

##  5. Simple Fixes / Remediation
- ✅ Enable SMB signing through Windows Group Policy.
- 🔄 Regularly apply Windows updates and security patches.
- 🚫 Disable legacy/unused services (e.g., SMBv1, NetBIOS).
- 🔐 Implement strict firewall rules to reduce unnecessary exposure.
---

If you want, I can also generate the `smb-signing.md` file directly in this repo or add more files like screenshots, report folder, or a PDF summary.
