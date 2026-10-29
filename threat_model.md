# Threat Model — CivicConnect

## System and trust boundaries
Citizen/staff browsers connect over HTTPS to a web front end/WAF, then to an API gateway and application services. Services access a database and private document storage. External integrations include identity verification, payment, email and SMS. Security logs are sent to centralized monitoring; backups are isolated.

Trust boundaries: public user to service; citizen to staff workflows; application to database/storage; service to third-party providers; production to backup and deployment environments.

## Assets
Citizen identity/profile data; applications and documents; staff/admin accounts; decisions and payment status; database and backups; audit logs; API credentials; source code and deployment secrets.

## Threats and mitigations
1. Account takeover — staff MFA, secure recovery, rate limits, anomaly detection.
2. Broken access control — server-side ownership and role checks on every request; automated authorization tests.
3. Injection/unsafe input — parameterized queries, validation, output encoding, secure code review.
4. Ransomware/outage — patching, segmentation, least privilege, isolated immutable backups, restore drills.
5. Misconfigured document storage — private-by-default access, encryption, automated configuration checks.
6. Denial of service — DDoS/WAF controls, rate limits, capacity testing, graceful degradation.
7. Insider misuse — least privilege, separate admin identities, audit review, access recertification.
8. Third-party compromise — scoped/rotated credentials, vendor review, integration monitoring and revocation.
9. Supply-chain compromise — dependency and secret scanning, protected branches, signed builds and release approval.
10. Phishing — staff training, phishing-resistant MFA where feasible, independent verification and reporting.

## Defensive priorities
Treat account takeover and broken access control as critical until validated. Track every action in a risk register with an owner, target date, evidence, and residual-risk decision.
