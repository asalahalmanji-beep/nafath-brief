Version: NAFATH-V1
Track: Programming

## Summary
The proposed national digital sign-on service unifies government access through a single citizen account. Integrating these six IT domains ensures a robust foundation: Software engineering establishes secure authentication protocols, while AI risk management monitors anomalies to protect user accounts. Mobile runtime permissions safeguard device resources, and Encrypted DNS (DoH) secures transit communication against surveillance. Furthermore, phishing-resistant multi-factor authentication prevents credential theft, and compliance with Oman's Personal Data Protection Law guarantees lawful data collection and storage, collectively delivering a secure identity infrastructure.

## Programming
OAuth 2.0 is an authorization framework designed to grant delegated access to resources without sharing credentials, whereas OpenID Connect (OIDC) is an identity layer built on top of OAuth 2.0 specifically designed for user authentication and returning profile information via an ID token. For the national sign-on service, OIDC handles verifying user identity during login, while OAuth 2.0 manages authorized access to external government APIs.

Resource: RFC 6749 - The OAuth 2.0 Authorization Framework - https://datatracker.ietf.org/doc/html/rfc6749

## Artificial Intelligence
Before deploying an AI model for automated suspicious login detection, authorities must manage several risks highlighted by frameworks like the NIST AI Risk Management Framework, including privacy degradation from behavioral profiling, algorithmic bias leading to false positives or discrimination against legitimate users, lack of model interpretability and transparency, and security vulnerabilities such as adversarial evasion attacks and data poisoning that could compromise system integrity.

Resource: NIST AI 100-1 - Artificial Intelligence Risk Management Framework (AI RMF 1.0) - https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.900-1.pdf

## Mobile
Android’s runtime permission model limits what a sign-on application can access by requiring explicit user consent for sensitive resources like storage or location, ensuring the app cannot access them by default. The application must request these permissions dynamically at the exact moment the specific feature requiring them is invoked, rather than at installation, following Google's principle of context and necessity.

Resource: Android Developers - Request app permissions - https://developer.android.com/training/permissions/requesting

## Networking

## Cybersecurity

## Data

## Misconception in My Track

## Open Questions
