Version: NAFATH-V1
Track: Programming

## Summary
The proposed national digital sign-on service unifies government access through a single citizen account. Integrating these six IT domains ensures a robust foundation: Software engineering establishes secure authentication protocols, while AI risk management monitors anomalies to protect user accounts. Mobile runtime permissions safeguard device resources, and Encrypted DNS (DoH) secures transit communication against surveillance. Furthermore, phishing-resistant multi-factor authentication prevents credential theft, and compliance with Oman's Personal Data Protection Law guarantees lawful data collection and storage. Ultimately, this brief focuses on resolving software engineering misconceptions regarding authentication versus delegated authorization protocols.

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
DNS over HTTPS (DoH) is a protocol for performing remote Domain Name System (DNS) resolution via the HTTPS protocol. For service users, DoH protects privacy and integrity by encrypting DNS queries and responses, preventing on-path attackers from eavesdropping on or tampering with the websites and services users are trying to reach. However, DoH does not protect the actual IP addresses of the servers being communicated with after resolution, nor does it secure the content of the subsequent HTTPS traffic.

Resource: RFC 8484 - DNS Queries over HTTPS (DoH) - https://datatracker.ietf.org/doc/html/rfc8484

## Cybersecurity
Phishing-resistant multi-factor authentication relies on cryptographic mechanisms that bind credentials to a specific origin, ensuring they cannot be captured or relayed by an attacker. MFA methods such as FIDO2/WebAuthn security keys and platform authenticators (like Windows Hello or biometric hardware enclaves) are considered phishing-resistant because they verify the domain. Conversely, SMS-based OTPs, email codes, and standard software push notifications are vulnerable to interception and adversary-in-the-middle phishing sites.

Resource: NIST SP 800-63B - Digital Identity Guidelines: Authentication and Lifecycle Management - https://pages.nist.gov/800-63-3/sp800-63b.html

## Data
Under Oman's Personal Data Protection Law (Royal Decree No. 6/2022), the authority must adhere to strict obligations when collecting and storing citizens' personal data. These include obtaining explicit and lawful consent from the data subject, processing data transparently and solely for specified legitimate purposes, implementing adequate technical and organizational security measures to prevent breaches, ensuring data minimization and accuracy, and respecting citizens' rights to access, correct, or request deletion of their personal data.

Resource: Ministry of Transport, Communications and Information Technology - Personal Data Protection Law (Oman) - https://www.mtcit.gov.om/ITAPortal/Data/English/DocLibrary/202364121511202/Personal%20Data%20Protection%20Law.pdf

## Misconception in My Track
A common misconception in the programming track is that OAuth 2.0 is an authentication protocol used to log users into applications. In reality, OAuth 2.0 is strictly an authorization framework designed to delegate access to protected resources, whereas OpenID Connect (OIDC) is the actual authentication layer built on top of it to handle user logins. This distinction is explicitly clarified in the foundational specifications and architectural overviews provided by the OpenID Foundation and IETF standards documents.

Resource: OpenID Foundation - Welcome to OpenID Connect - https://openid.net/connect/

## Open Questions
What specific encryption algorithms and key management practices will be mandated by national regulatory bodies for storing citizen identity tokens securely within the cloud infrastructure?
