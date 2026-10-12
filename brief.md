Version: NAFATH-V1
Your track: Networking
Overview
A secure national digital login service depends on six connected IT fields. OAuth 2.0 enables delegated access to resources, while OpenID Connect adds an identity layer for verifying users during login. AI can flag suspicious sign-ins, but its risks—including inaccurate results, bias, privacy, and security—must be assessed and managed before deployment. The mobile app should request Android runtime permissions only when it needs access to restricted data or actions, and explain why access is needed. Networking protections such as DNS over HTTPS encrypt DNS queries between a device and its resolver, but do not hide all online activity. Cybersecurity controls, especially phishing-resistant authentication, help reduce account theft. Finally, the authority must handle citizens’ personal data in line with Oman’s Personal Data Protection Law. Together, these fields help make the service secure, reliable, privacy-conscious, and usable.
Software
OAuth 2.0 is an authorization framework that allows an application to obtain limited access to resources with the resource owner's permission. OpenID Connect (OIDC) builds on OAuth 2.0 by adding an identity layer that enables a client to verify a user's identity and obtain basic profile information. Therefore, OAuth 2.0 is mainly for delegated access, while OpenID Connect is designed to support user authentication and login.

Resource: OpenID Connect Core 1.0 - https://openid.net/specs/openid-connect-core-1_0.html
AI
Before deploying an AI model to flag suspicious logins, the authority should use the NIST AI Risk Management Framework to identify and manage risks throughout the model's lifecycle. Key concerns include false alerts, missed suspicious activity, biased outcomes, privacy risks, cybersecurity threats, and limited transparency. The authority should test the model's accuracy, monitor its performance, protect login data, and establish human oversight and clear accountability before relying on its alerts.

Resource: NIST AI Risk Management Framework - https://www.nist.gov/itl/ai-risk-management-framework
Mobile
Android's runtime permission model restricts access to certain sensitive data and device features. For apps targeting supported Android versions, dangerous permissions must be requested at runtime, when the feature requiring access is needed, rather than assuming permission has already been granted. The login app should request only necessary permissions, explain why they are needed, and handle denial gracefully so that users can continue using features that do not require the restricted access.

Resource: Android Developers — Permissions on Android - https://developer.android.com/guide/topics/permissions/overview
Networking
Cybersecurity
Data
Misconception in My Track
Open Question
