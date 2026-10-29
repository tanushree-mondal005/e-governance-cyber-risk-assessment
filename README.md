# E-Governance Cyber Risk Assessment & Threat Model

This repository contains a defensive, hypothetical threat-model project for a public-service portal called CivicConnect.

## Contents
- `README.md` — project overview and safe-use note
- `risk_register.csv` — threat/risk register with likelihood, impact, priority, and treatment
- `threat_model.md` — system context, trust boundaries, threats, and mitigations
- `risk_assessment_methodology.md` — scoring method and limitations

## Scope
The model covers a citizen portal, staff/admin portal, APIs, database, document storage, backups, and third-party integrations. It is a tabletop assessment only. No real government service was tested, scanned, or accessed.

## Risk scoring
Likelihood and impact use a 1–3 qualitative scale. Score = likelihood × impact:
- 1–2 Low
- 3–4 Medium
- 6 High
- 9 Critical

## Frameworks referenced
- NIST Cybersecurity Framework (CSF) 2.0
- NIST SP 800-30 Rev. 1
- OWASP Top 10 / ASVS
- CERT-In public guidance

## How to use
Review the Word report and companion files, validate assumptions against the actual authorized environment, assign control owners, and update risk ratings using evidence. Do not test or scan any system without written authorization.
