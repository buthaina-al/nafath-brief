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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
