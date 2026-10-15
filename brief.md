Version: NAFATH-V1
Track: Software

## Overview
The NAFATH-V1 national digital login service integrates six critical IT domains to deliver a secure, unified authentication experience across mobile applications and web portals. Software architecture establishes standardized protocols to manage user sessions, while artificial intelligence continuously monitors behavioral analytics to flag anomalies and prevent fraudulent access attempts. Mobile integration relies on strict operating system runtime permissions to safeguard user privacy during biometric or credential prompts. Networking protocols like DNS over HTTPS protect query privacy against eavesdropping, complemented by phishing-resistant multi-factor authentication methods deployed at the cybersecurity layer. Finally, rigorous data governance ensures compliance with Oman's Personal Data Protection Law by enforcing strict collection and storage mandates for citizen records. Together, these pillars secure the ecosystem, culminating in the foundational software implementation governing OAuth 2.0 and OpenID Connect protocols.

## Software

OAuth 2.0 and OpenID Connect (OIDC) serve distinct purposes in digital architectures. OAuth 2.0 is an authorization framework designed to grant delegated access to protected resources without sharing user credentials. In contrast, OpenID Connect is an authentication layer built on top of OAuth 2.0 that introduces an ID token, explicitly managing user login and identity verification. For a single sign-on login service, OIDC handles authenticating the citizen, while OAuth 2.0 handles secure API access.

Resource: RFC 6749 - The OAuth 2.0 Authorization Framework - https://www.rfc-editor.org/rfc/rfc6749

## AI

Deploying an AI model to automatically flag suspicious logins requires managing several critical risks outlined in frameworks like the NIST AI Risk Management Framework. Key risks include validity and reliability failures, privacy degradation, and security vulnerabilities like adversarial prompt injection or model evasion. Furthermore, bias and disparate impact must be mitigated to prevent unfair login blocks for specific citizen demographics, alongside ensuring transparency and explainability so flagged accounts can be audited by human administrators before enforcement.

Resource: NIST AI 100-1 - Artificial Intelligence Risk Management Framework (AI RMF 1.0) - https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.100-1.pdf

## Mobile

Android's runtime permission model restricts application access to sensitive user data and device features, such as camera biometrics or location, until explicit user consent is granted. The login application must request these permissions dynamically at the exact moment a feature requiring them is accessed—for instance, prompting for camera permissions only when scanning a QR code or performing facial biometric verification. Applications cannot access protected resources preemptively.

Resource: Android Developers Documentation - Permissions on Android - https://developer.android.com/guide/topics/permissions/overview
