Version: NAFATH-V4
Track: Networking

## Overview
A national service provider depends on software, artificial intelligence (AI), mobile applications, secure networks, cybersecurity, and trustworthy data to deliver essential services. Each area addresses a different supply-chain risk. Secure software configuration helps prevent secret exposure, while AI security reduces risks from manipulated inputs and poisoned training data. Mobile security controls help protect sensitive information and communications. Cybersecurity practices help identify and fix software vulnerabilities, and a Software Bill of Materials (SBOM) helps organizations track software components and assess risks. These protections work together through secure development, testing, monitoring, and timely updates. However, securing applications alone cannot guarantee that internet traffic reaches the correct destination. BGP route hijacking can redirect or disrupt traffic, while Resource Public Key Infrastructure (RPKI) helps networks validate route origins. How effectively can RPKI be combined with additional routing security measures to detect attacks that origin validation alone cannot prevent?
## Software
The Twelve-Factor App methodology recommends storing deployment-specific configuration in environment variables rather than hard-coding it in source code. Configuration includes service credentials, database connection details, and settings that vary between deployments. Keeping these values out of code reduces accidental exposure in repositories and allows settings to change without modifying the application. Sensitive secrets should also be managed through a secure secrets-management system.

Source: The Twelve-Factor App, Config — https://12factor.net/config
## AI
Adversarial machine-learning attacks target different stages of an AI system. Evasion attacks manipulate inputs at inference time to cause incorrect predictions, while poisoning attacks corrupt training data so the model learns harmful behavior. Defenses may include data validation, controlled training pipelines, adversarial testing, and monitoring. No single mitigation prevents every attack, so security measures should match the system’s risks.

Source: NIST, Adversarial Machine Learning — https://csrc.nist.gov/pubs/ai/100/2/e2025/final
## Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) defines security controls for mobile applications, covering data storage, cryptography, authentication, network communication, and privacy. Developers and testers can use these controls to establish security requirements and assess an application’s protections. The standard provides a consistent verification baseline, but following it does not guarantee that an application is completely secure.

Source: OWASP MASVS — https://mas.owasp.org/MASVS/02-Frontispiece/
## Networking
BGP route hijacking occurs when an autonomous system announces incorrect or unauthorized routes, potentially redirecting internet traffic through an unintended network or preventing it from reaching its destination. Resource Public Key Infrastructure (RPKI) supports Route Origin Validation by checking whether an autonomous system is authorized to announce an IP prefix. Operators can use this information to reject invalid routes. However, RPKI origin validation does not authenticate every autonomous system along the full route.

Source: RFC 6811, BGP Prefix Origin Validation — https://www.rfc-editor.org/rfc/rfc6811.html
## Cybersecurity
Log4Shell (CVE-2021-44228) was a critical vulnerability in Apache Log4j 2 that could allow remote code execution under vulnerable conditions. The vulnerability received a CVSS score of 10.0. Organizations should identify applications using affected versions, upgrade to fixed versions recommended by Apache, and verify that vulnerable components have been removed or updated. This incident highlights why software dependencies must be tracked and patched promptly.

Source: CISA, Mitigating Log4Shell — https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-356a
## Data
A Software Bill of Materials (SBOM) is a formal inventory of software components and their relationships. Important fields include the supplier, component name, version, unique identifiers, dependency relationships, author, and timestamp. An SBOM helps organizations identify potentially affected components when vulnerabilities are disclosed and supports software inventory management. However, it does not prove that software is safe; records must remain current and support ongoing vulnerability management.

Source: NTIA, The Minimum Elements for an SBOM — https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom
## Misconception in My Track
A common misconception is that deploying RPKI completely prevents BGP route hijacking. In reality, RPKI Route Origin Validation checks whether the autonomous system originating a route is authorized to announce the prefix; it does not validate every autonomous system in the full AS path. Therefore, some routing attacks may remain undetected. Network operators should combine RPKI with careful routing policies, monitoring, and additional security measures.

Source: RFC 6811, BGP Prefix Origin Validation — https://www.rfc-editor.org/rfc/rfc6811.html
## Open Question
How effectively can network operators combine RPKI Route Origin Validation with AS-path security and real-time routing monitoring to detect attacks that origin validation alone cannot prevent?
