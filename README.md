# 🛡️ vCISO Security Risk Assessment Externship

![Status](https://img.shields.io/badge/Status-In%20Progress-orange)
![Focus](https://img.shields.io/badge/Focus-Security%20Risk%20Assessment-blue)
![GRC](https://img.shields.io/badge/Domain-GRC-purple)
![Framework](https://img.shields.io/badge/Framework-NIST%20CSF%202.0-green)
![Program](https://img.shields.io/badge/Program-Extern-black)

Welcome to my **vCISO Security Risk Assessment Externship** repository.

This repository documents my hands-on learning journey in cybersecurity risk assessment, governance, risk and compliance (GRC), external attack-surface discovery, vulnerability analysis, and security reporting.

Through a simulated client engagement, I am learning how to identify critical assets, investigate security exposures, evaluate risks in a business context, and communicate findings in a structured, evidence-based manner.

The repository will be updated throughout the program as I complete additional assessments, develop deliverables, and build my final capstone projects.

---

## 📌 Program Overview

| Detail | Information |
|---|---|
| Program | vCISO Security Risk Assessment Externship |
| Organization | Extern |
| Role | Junior Security Consultant \| vCISO |
| Start Date | October 12, 2026 |
| Duration | 8 weeks |
| Current Progress | Weeks 1–2 completed |
| Primary Focus | Security Risk Assessment, GRC, External Exposure, Risk Reporting |

---

## 🏢 Simulated Client: Cumberland Claims Services

The program uses a simulated organization, **Cumberland Claims Services (CCS)**, as the client for a security risk assessment engagement.

CCS operates in a healthcare-related claims processing environment where the confidentiality, integrity, and availability of information are essential to business operations.

### Business Context

- **Largest customer:** Meridian Health System
- **Revenue dependency:** Meridian represents 31% of CCS revenue.
- **Operational environment:** 41 clinics and 2 hospital systems.
- **External integrations:** 2 clearinghouses.
- **Business deadline:** Customer contract renewal in 90 days.

These business details provide context for evaluating security risks, prioritizing findings, and understanding how technical weaknesses may affect business operations and customer relationships.

---

## 🎯 Assessment Objectives

The primary objectives of this engagement are to:

- Establish an accurate asset inventory and define the assessment scope.
- Identify publicly exposed domains, hostnames, and services.
- Distinguish current organizational assets from potentially unrelated or legacy exposures.
- Investigate vulnerabilities and validate findings using available evidence.
- Assess security risks in the context of business impact.
- Apply the NIST Cybersecurity Framework (CSF) 2.0 where appropriate.
- Document findings, evidence, gaps, and remediation considerations.
- Communicate assessment results clearly to technical and non-technical stakeholders.

---

## 🔎 Assessment Workflow

The engagement follows a structured assessment process:

| Phase | Objective |
|---|---|
| Business Context & Scope | Understand the client, business function, and assessment boundaries. |
| Asset Inventory | Identify assets, ownership, dependencies, and missing information. |
| External Exposure Discovery | Investigate public-facing domains and hostnames. |
| Evidence Correlation | Compare findings against the asset inventory and scope. |
| Vulnerability Investigation | Examine potential weaknesses and supporting evidence. |
| Risk Assessment | Evaluate findings in terms of likelihood, impact, and business relevance. |
| Reporting & Recommendations | Document findings and communicate practical next steps. |

---

# 📂 Project Breakdown

## Week 1 — Asset Inventory & Scope

**Status:** ✅ Completed

The first phase focused on understanding Cumberland Claims Services' business environment and establishing an initial inventory of assets relevant to the assessment.

### Key Activities

- Reviewed the client engagement context and assessment scope.
- Identified systems, applications, domains, and external access relationships.
- Compared available source information to identify inventory gaps.
- Investigated discrepancies and reconciled missing asset information.
- Considered asset ownership and dependencies when defining the assessment boundaries.

### Initial Asset Inventory

| Asset | Description / Role |
|---|---|
| MedFlow Production | Production claims processing application. |
| CCS-APP01 | Application server. |
| CCS-SQL01 | Database server. |
| Clinic Portal | External-facing clinic portal. |
| CCS-WEB01 | Web server. |
| CCS-SFTP01 | Secure file transfer server. |
| CumberlandClaims.com | Public organizational domain. |
| MedFlow Vendor Support Access | Third-party support access relationship. |
| Ridgeline IT Remote Access | External IT support access relationship. |

Additional assets and relationships were identified during the inventory review, including MedFlow test, MidSouth Exchange, and CCS-ARC01 / ArcVault.

### Key Learning Outcomes

- Asset inventories require more than collecting system names.
- Ownership, business purpose, dependencies, and exposure all affect risk assessment.
- Missing assets and inconsistent records can create blind spots in security reviews.
- Assessment scope must be established before conclusions about exposure or risk can be made.

---

## Week 2 — External Exposure & Attack-Surface Mapping

**Status:** ✅ Completed

The second phase focused on identifying publicly visible hostnames associated with the client's domain and determining how those identities relate to the assessment scope.

### Key Activities

- Used [crt.sh](https://crt.sh/) to investigate certificate transparency records for `cumberlandclaims.com`.
- Collected and reviewed 16 unique Matching Identities, including wildcard entries.
- Compared certificate issuance dates and issuers to help assess ownership.
- Distinguished more recent Amazon-issued certificates from older certificates associated with non-Amazon issuers.
- Preserved the bare domain as the registered domain rather than automatically treating it as an individual application or service.
- Compared discovered hostnames with the internal asset inventory and scope information.

### Hostname-to-Asset Mapping

| Hostname | Associated Asset / Service | Scope |
|---|---|---|
| `portal` | Clinic Portal | Scope A |
| `payers` | Meridian remittance | Scope B |
| `records` | Records Request | Scope C |
| `remote` | FortiGate | Scope D |

*The hostname mappings above reflect the assessment context documented during the exercise. Certificate transparency records alone do not prove that a host is currently active, vulnerable, or owned by the organization.*

### Key Learning Outcomes

- Publicly visible hostnames can reveal an organization's external attack surface.
- Certificate transparency is a useful reconnaissance source, but its results require interpretation.
- Certificate dates and issuers can support ownership analysis, but should not be treated as conclusive proof on their own.
- An exposed hostname is not automatically a security vulnerability.
- Correlating external discoveries with the asset inventory helps distinguish relevant exposures from unrelated or legacy records.

---

## 🔬 Additional Assessment Work

As the program progresses, this section will document further assessment activities, evidence-based findings, and reporting deliverables.

Areas explored or discussed include:

- Vulnerability investigation involving potential issues associated with the Clinic Portal and CCS-SQL01.
- Review of TLS configuration and HTTP security headers, including TLS 1.0/1.1 and HSTS.
- Use of external assessment resources such as [Qualys SSL Labs](https://www.ssllabs.com/ssltest/) and [Mozilla Observatory](https://observatory.mozilla.org/).
- Scope A reporting for the Claims Intake business function.
- Email security assessment concerning who can send email in Cumberland Claims Services' name.

**Note:** Specific findings, validation status, evidence, and remediation recommendations will be added here as they are confirmed in the assessment workbooks and supporting deliverables.

---

## 🧠 Skills Demonstrated

| Area | Skills / Concepts |
|---|---|
| Security Risk Assessment | Scoping, asset identification, evidence review, risk context |
| Governance, Risk & Compliance | Risk documentation, assessment structure, stakeholder reporting |
| External Attack Surface | Certificate transparency, hostname discovery, exposure mapping |
| Asset Management | Inventory reconciliation, ownership analysis, asset relationships |
| Vulnerability Analysis | Weakness investigation, evidence correlation, validation |
| Security Frameworks | NIST Cybersecurity Framework (CSF) 2.0 |
| Security Reporting | Documenting findings, identifying gaps, communicating risks |
| Business Risk | Understanding customer dependencies and operational impact |

---

## 📁 Repository Contents

This repository will evolve as the program progresses. It may include:

- Assessment notes and methodology.
- Asset inventory and scope documentation.
- External exposure and hostname mapping.
- Vulnerability investigation records.
- Security findings and supporting evidence.
- Risk assessment deliverables.
- Final capstone projects and reporting materials.

Additional folders, screenshots, diagrams, and links to individual projects will be added as the relevant work is completed and reviewed for public sharing.

---

## 📈 Program Progress

| Week | Focus Area | Status |
|---|---|---|
| Week 1 | Asset Inventory & Scope | ✅ Completed |
| Week 2 | External Exposure & Attack-Surface Mapping | ✅ Completed |
| Week 3 | Upcoming Assessment Work | ⏳ Pending |
| Week 4 | Upcoming Assessment Work | ⏳ Pending |
| Week 5 | Upcoming Assessment Work | ⏳ Pending |
| Week 6 | Upcoming Assessment Work | ⏳ Pending |
| Week 7 | Upcoming Assessment Work | ⏳ Pending |
| Week 8 | Final Deliverables & Capstone | ⏳ Pending |

*This tracker will be updated as each module and deliverable is completed.*

---

## 💭 Learning Reflection

This externship is helping me understand cybersecurity from a broader perspective: not only how technical weaknesses are discovered, but also how assets are identified, evidence is evaluated, risks are prioritized, and findings are communicated in a business context.

A structured risk assessment requires the ability to connect technical observations with organizational priorities. It also requires careful documentation, clear scope boundaries, and evidence-based conclusions.

As I continue through the program, I aim to strengthen my ability to assess security posture, investigate exposures, and produce clear, defensible security recommendations.

---

## ⚠️ Disclaimer

This repository documents educational work completed as part of a simulated security risk assessment externship.

Cumberland Claims Services and the associated business environment are used as a simulated case study. Assessment conclusions should be based on the evidence and scope documented in the relevant exercises.

Before publishing supporting materials, sensitive information, personal data, credentials, confidential evidence, and any restricted program content must be removed or appropriately redacted.

---

**More updates coming as the assessment progresses.** 🛡️
