# SMB Signing Not Required


**Severity:** Medium
**Port/Service:** 445/tcp (CIFS)


## Description
SMB signing is not required on the target host. Without SMB signing, an attacker positioned on the network may perform MITM attacks.


## Impact
- Traffic tampering
- Credential interception
- Unauthorized modification of SMB communication


## Fix
- Enable SMB Signing via Group Policy:
- `Computer Configuration > Windows Settings > Security Settings > Local Policies > Security Options`
- Set **Microsoft network client: Digitally sign communications (always)** to **Enabled**.
- Set **Microsoft network server: Digitally sign communications (always)** to **Enabled**.
```
