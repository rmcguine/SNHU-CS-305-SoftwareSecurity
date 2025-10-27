# SNHU-CS-305-SoftwareSecurity

# Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?
Artemis Financial is a financial services client that needed stronger application security, specifically modern cryptography for data integrity and encrypted transport for web traffic. The engagement focused on adding a SHA-256 hashing step, enabling HTTPS with a certificate, and hardening the API to reduce breach risk.

# What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?
I implemented HTTPS/TLS, added a modern hash routine (SHA-256) via MessageDigest, tightened error handling, and ran a dependency vulnerability scan—practical guardrails that reduce the attack surface. Secure coding protects client trust, reduces incident likelihood and costs, and supports smoother audits and reliability under hostile traffic.

# Which part of the vulnerability assessment was challenging or helpful to you?
Standing up the self-signed certificate to actually enable HTTPS was a key milestone and good hands-on practice. Wiring in the hash and validating it with a checksum, then confirming with a dependency check, made security improvements measurable and verifiable.

# How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?
I layered SHA-256 hashing for integrity, enforced HTTPS/TLS for transport protection, improved API input handling, and used dependency scanning to catch known CVEs. Going forward, I’d keep CI checks enforced (SCA/SAST/secret scanning) and maintain modern TLS and security headers to continuously assess and mitigate risk.

# How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?
Functionally, I handled errors appropriately (e.g., NoSuchAlgorithmException) and verified behavior with checksum validation, ensuring the refactor didn’t break runtime paths. Security-wise, I ran a dependency check after the changes to confirm no new vulnerabilities were introduced. 

# What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?
Spring Boot’s security-friendly API patterns, Java’s MessageDigest for SHA-256, and routine dependency vulnerability scans formed the core toolkit. I’ll reuse the CI gate of SCA/SAST/secret scanning plus disciplined config/secret handling and safer error responses in future work.

# Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?
I’d show the HTTPS enablement with a working certificate, the SHA-256 integrity flow in code, and a before/after dependency-check snapshot demonstrating reduced risk. The write-up summarizing milestones and the rationale for algorithm and transport choices would also showcase practical, business-oriented security thinking.
