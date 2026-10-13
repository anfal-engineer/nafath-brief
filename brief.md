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
DNS over HTTPS (DoH) sends DNS queries and responses through encrypted HTTPS connections. It helps protect users from network observers reading their DNS queries and reduces the risk of attackers tampering with DNS traffic in transit. However, DoH does not hide the user's IP address from the DoH resolver, encrypt all website traffic by itself, or prevent websites and other parties from tracking users through other methods.

Resource: RFC 8484: DNS Queries over HTTPS (DoH) - https://www.rfc-editor.org/rfc/rfc8484.html
Cybersecurity
Phishing-resistant authentication prevents attackers from reusing authentication secrets at fake login sites because the authentication protocol binds the response to the legitimate service. Examples include FIDO2 security keys and passkeys using WebAuthn. Passwords, SMS codes, authenticator-app one-time passwords, and manually entered approval codes are not phishing-resistant, even when used as part of multi-factor authentication. The service should offer phishing-resistant methods to better protect citizens' accounts.

Resource: NIST SP 800-63B - Authenticator and Verifier Requirements - https://pages.nist.gov/800-63-4/sp800-63b/authenticators/
Data
Under Oman's Personal Data Protection Law, the authority should inform citizens about why their personal data is collected and obtain their explicit consent before processing it, as required by law. It must establish a personal data protection policy, maintain records of processing activities, and provide a way for individuals to exercise their rights. Certain sensitive data requires a Ministry permit, and data breaches must be reported when required by law. The authority must also follow applicable rules for transferring data outside Oman.

Resource: Executive Regulations of the Personal Data Protection Law - https://opendata.gov.om/ar/community/laws/3b3cbc1e-1e57-4b98-91f7-3def8f34f158
Misconception in My Track
A common misconception is that DNS over HTTPS (DoH) makes all online activity private and anonymous. In reality, DoH encrypts DNS queries between the client and its resolver, helping prevent observers on the network from reading or modifying those queries. However, it does not hide the client's IP address from the resolver or encrypt all other internet traffic by itself. Section 8, "Privacy Considerations," of RFC 8484 explains the privacy risks and limitations of DoH.
Open Question
How can a national login service choose a trusted DoH resolver while balancing citizens' privacy, service reliability, and protection against DNS-based attacks?
