Version: NAFATH-V1
Track: Networking

## Overview
This brief examines how six IT fields contribute to secure and reliable digital identity services: Software, Artificial Intelligence (AI), Mobile Development, Networking, Cybersecurity, and Data. A government single sign-on service allows citizens to access multiple government services through one account using a mobile application or website. These six fields support different aspects of the service. Software enables systems to communicate and manage authentication. AI can help identify suspicious login activity, while mobile development addresses application permissions. Networking supports communication between systems, cybersecurity helps protect accounts from threats, and data practices guide the responsible handling of personal information. Together, these fields help make the service more secure, reliable, and convenient for citizens.
## Software
OAuth 2.0 and OpenID Connect serve different purposes in digital identity systems. OAuth 2.0 is an authorization framework that allows applications to obtain limited access to protected resources. OpenID Connect builds on OAuth 2.0 by adding an identity layer that enables applications to verify a user’s identity and obtain basic profile information. In a government single sign-on service, OpenID Connect supports user login, while OAuth 2.0 enables delegated access to resources.
Resource: OpenID Connect Core 1.0 - https://openid.net/specs/openid-connect-core-1_0-errata2.html
## AI
Following the NIST AI Risk Management Framework (AI RMF), the authority should manage risks related to inaccurate predictions, security vulnerabilities, privacy breaches, bias, and lack of transparency or accountability. For suspicious-login detection, false positives may wrongly flag legitimate citizens, while false negatives may allow malicious logins to go undetected. The authority should also consider model manipulation and misuse of citizens’ personal data before deployment.
Resource: AI Risks and Trustworthiness - https://airc.nist.gov/airmf-resources/airmf/3-sec-characteristics/
## Mobile
Android’s runtime permission model restricts an app’s access to sensitive data and device features, such as location, the camera, and the microphone. For permissions classified as dangerous, the app must request the user’s approval at runtime, when the relevant feature requires access. Users can grant or deny the request, and the app should handle denial without assuming access is available. This model helps limit unnecessary access to personal information and device resources.
Resource: Permissions on Android -https://developer.android.com/guide/topics/permissions/overview
## Networking
DNS over HTTPS (DoH) sends DNS queries and responses over an encrypted HTTPS connection. It protects DNS queries from being easily read or modified by parties monitoring the network path between the user and the DoH resolver. However, it does not hide the user’s IP address from visited websites, prevent the DoH resolver from seeing queries, or independently guarantee the authenticity of DNS data. Therefore, DoH improves DNS privacy in transit but does not provide complete online anonymity or security.
Resource: RFC 8484: DNS Queries over HTTPS (DoH) - https://www.rfc-editor.org/rfc/rfc8484.html
## Cybersecurity
Phishing-resistant authentication binds the authentication process to the legitimate website, preventing credentials from being reused on fake sites. Resistant methods include FIDO2/WebAuthn security keys, FIDO-based passkeys, and certificate-based authentication. Non-resistant methods include SMS or email codes, manually entered one-time passwords (OTPs), and push notifications, even with number matching. For a government single sign-on service, phishing-resistant MFA helps protect citizens’ accounts from credential theft and impersonation.
Resource: Implementing Phishing-Resistant MFA - https://www.cisa.gov/sites/default/files/2023-01/fact-sheet-implementing-phishing-resistant-mfa-508c.pdf
## Data
Oman’s Personal Data Protection Law (Royal Decree 6/2022) regulates the collection and processing of personal data. An authority should obtain consent where required by law, protect data confidentiality, and apply appropriate safeguards against unauthorized access or disclosure. It must also respect individuals’ rights to request corrections, updates, or deletion of their data and comply with applicable personal data breach notification requirements. These measures help protect citizens’ privacy and support responsible data management.
Resource: Personal Data Protection Law - https://prod.mtcit.gov.om/ITAPortal_AR/Pages/Page.aspx?NID=1914&PID=2101437
## Misconception in My Track
A common misconception about DNS over HTTPS (DoH) is that it makes users completely anonymous online. In reality, DoH encrypts DNS queries while they travel between the client and the configured resolver, making them harder for network observers to read or modify. However, the DoH resolver can still see the queries it processes, and DoH does not hide all identifying information, such as the user’s IP address, from every party. Therefore, DoH improves DNS privacy in transit but does not guarantee complete online anonymity. 
Evidence: RFC 8484, Sections 8.1 “On the Wire” and 8.2 “In the Server”. https://www.rfc-editor.org/rfc/rfc8484.html
## Open Question
How can a government authority configure DNS over HTTPS to improve citizens DNS privacy while maintaining effective network security monitoring and protecting sensitive information?
