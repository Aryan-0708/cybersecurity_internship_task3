# cybersecurity_internship_task3

# Vulnerability Scan on Localhost using Nessus Essentials

## Objective

The goal of this task was to perform a basic vulnerability scan on my own PC using Nessus Essentials, identify high-risk vulnerabilities, and understand how vulnerability assessment works in practice.

## Tools Used

- Nessus Essentials (community edition)
- Target: Localhost (127.0.0.1)

## Steps I Followed

1. Installed Nessus Essentials and activated it using the free license key.
2. Allowed Nessus to download all required plugins and components.
3. Created a Basic Network Scan in Nessus with the target set to 127.0.0.1.
4. Launched the scan and waited for it to complete.
5. Analyzed the scan results and documented the findings.

## Scan Results Summary

Nessus categorizes vulnerabilities into five types:

1. Critical  
2. High  
3. Medium  
4. Low  
5. Informational

In my scan of the local system (127.0.0.1), the following results were found:

- Total vulnerabilities found: 97  
  - Critical: 0  
  - High: 0  
  - Medium: 2  
  - Low: 0  
  - Informational: 95  

## Most Critical Vulnerabilities

Since there were no Critical or High vulnerabilities, the Medium ones are considered the most important in this scan.

### 1. SSL Certificate Cannot Be Trusted

Plugin ID: 51192  
Severity: Medium  
CVSS v3 Base Score: 6.5  
Description: The SSL certificate on the system cannot be trusted. This can happen if the certificate is self-signed, expired, or from an untrusted certificate authority. In a public environment, it could make the system vulnerable to man-in-the-middle attacks.  
Suggested Fix: Replace the certificate with a valid one issued by a trusted certificate authority.

### 2. SMB Signing Not Required

Plugin ID: 57608  
Severity: Medium  
CVSS v3 Base Score: 5.3  
Description: The SMB server does not require message signing, which allows attackers to perform man-in-the-middle attacks on SMB traffic.  
Suggested Fix: Configure the system to enforce SMB message signing.

## Screenshots

The screenshots (dashboard, SSL certificate issue, SMB signing issue) are available in the `task3_cybersecurity_internship` folder.

## Report

The full Nessus scan report is available in the `task3_cybersecurity_internship` folder in HTML format.

## Conclusion

This task helped me understand how vulnerability scanners like Nessus work, how to configure and run a scan, and how to interpret and prioritize vulnerabilities based on severity.
