
# Inspection Summary Report

## Inspection Identification

- **Project:** SouthNorthern University – Grants Management System (GMS)
- **Course:** AP/ITEC 4040 – Fall 2026
- **Inspecting Group:** Cyber OpsV2
- **Meeting Date:** November 24, 2026
- **Meeting Platform:** Zoom

## Work Product Description

The inspected work product was the anonymous Software Requirements Specification (SRS) draft provided in `6.zip`. The document describes the functional and non-functional requirements for SouthNorthern University's Grants Management System.

Our inspection focused on grant applications, Department Chair approvals, data requirements, software interfaces and security. Supporting requirements related to user classes, constraints, assumptions and dependencies were also reviewed.

Section numbers and requirement IDs were used to locate and reference issues throughout the inspection.

## Inspectors

| # | Role | Inspector | Preparation Time (hours) |
| --- | --- | --- | ---: |
| 1 | Author Representative | Jorjan Buenaflor | 2 |
| 2 | Moderator | Abilaksan Logathasan | 3 |
| 3 | Recorder | Siru Gautam | 1.5 |
| 4 | Reader | Bahareh Azmi | 2.5 |
| | | **Total Preparation Time** | **9** |

The author representative is a member of the inspecting group who performed the author role during the formal inspection, rather than an original author of the inspected SRS.

## Inspection Data

| Metric | Value |
| --- | --- |
| Planned for Inspection | 5 primary sections and 4 supporting sections |
| Actually Inspected | Selected requirements from Sections 1.2, 2.2, 2.4, 2.5, 3.1, 3.2, 4.3, 5.2 and 6.5 |
| Meeting Time | Approximately 1 hour |
| Total Planning Effort | 2 person-hours (estimated) |
| Total Overview Effort | 1 person-hour (estimated) |
| Total Preparation Effort | 9 person-hours |
| Total Meeting Effort | 4 person-hours |
| Actual Rework Effort | Not applicable at this stage |
| Major Issues | 8 |
| Minor Issues | 5 |
| Total Unique Issues | 13 |


## Inspection Process Description

### Planning and Preparation

- After receiving the anonymous SRS draft, our group reviewed the document and selected high-risk and mission-critical requirements for the formal inspection.
- Risk-based sampling was used because inspecting the entire SRS within the available meeting time was not practical. Priority was given to requirements affecting grant submission, approval workflows, data integrity and security.
- Four inspection roles were assigned: Moderator, Reader, Recorder and Author Representative.
- The moderator organized the inspection scope and agenda, reviewed the moderator checklist and prepared to manage the meeting.
- The reader reviewed the selected requirements, normal flows, alternative flows and exceptions. Potential defects were prepared with their locations, classifications and severities.
- The author representative reviewed the selected functional and non-functional requirements and inspection guidelines to understand the document and prepare for the discussion.
- The recorder reviewed the selected sections and prepared the Inspection Issue Log to document each identified issue.
- The inspection aids included the SRS document, inspection checklists, meeting agenda and Inspection Issue Log.
- The main inspection criteria were completeness, correctness, consistency, clarity, feasibility, traceability and testability.

### Meeting Procedure

- The formal inspection meeting was conducted through Zoom on November 24, 2026, and lasted approximately one hour.
- All four group members participated in their assigned inspection roles.
- At the beginning of the meeting, participants introduced themselves, identified their roles and explained their preparation activities.
- The moderator introduced the inspection objectives, scope and procedures before beginning the review.
- The reader presented the selected requirements in order and explained their intended meaning to the group.
- After each requirement or section was presented, participants discussed potential defects and their impact on the system.
- The moderator managed turn-taking, encouraged participation and ensured that discussions remained focused on the selected requirements.
- The author representative listened to the feedback, acknowledged concerns and provided clarification where supported by the documentation.
- The recorder documented identified issues, including their locations, descriptions, classifications and severities.
- Related issues appearing in multiple sections were cross-referenced to avoid duplicate entries.
- Confirmed requirements, proposed requirements, assumptions and unresolved decisions were distinguished throughout the inspection.
- The meeting focused on identifying and recording defects rather than developing technical solutions.
- At the end of the meeting, the group reviewed the findings, discussed their severity and recommended reinspection following rework.

### Inspection Scope

| Sections | Inspection Focus |
| --- | --- |
| 1.2, 2.2, 2.4, 2.5 | Document conventions, user classes, constraints, assumptions and dependencies |
| 3.1.4–3.1.6 | Grant application submission, validation, correction and resubmission |
| 3.2.1–3.2.2 | Department Chair approval and rejection |
| 4.3 | Data acquisition, integrity, retention and disposal |
| 5.2 | External software interfaces |
| 6.5 | Security requirements |

These sections were selected because defects within them could significantly affect the operation, reliability and security of the Grants Management System.

Due to time limitations, the remaining sections and later grant evaluation processes were outside the main inspection scope. Therefore, the inspection does not establish that the uninspected requirements are free of defects.

## Summary of Issues

The main concerns identified during the inspection involved incomplete business rules, unclear system behavior, missing traceability and requirements that were difficult to verify.

| Location | Main Finding and Impact |
| --- | --- |
| 1.2; 3.1.4 | Missing stakeholder evidence references make it difficult to trace requirements back to their original sources. |
| 3.1.4 | Late-submission rules and document-validation criteria are incomplete, which may result in inconsistent application processing. |
| 3.1.5–3.1.6 | Correction, rejection and resubmission rules are incomplete, making application outcomes unclear. |
| 3.2.1–3.2.2 | The identification of authorized Department Chair approvers and the resulting application state after rejection remain unresolved. |
| 3.1.6; 3.2.2; 4.3 (DA-05, DI-04) | Approval validity after application changes is unclear. An updated application may incorrectly retain its previous approval. |
| 4.3; 6.5 | The starting event for the three-year retention period is unresolved, potentially resulting in premature deletion or excessive data retention. |
| 5.2 (SI-03) | The use cases requiring Student Information System verification are unclear, affecting interface traceability and testability. |
| 2.2; 6.5 | The authoritative source of role assignments and certain user permissions remain unresolved, creating potential authorization and confidentiality risks. |

Additional concerns discussed during the inspection included mandatory audit events, external interface failure behavior, recovery objectives, multifactor authentication and security testability.

Several recurring issues were identified across different sections, particularly approval validity, role assignments and data retention. These concerns were cross-referenced rather than recorded as separate duplicate defects.

The most significant findings affect essential system functions. Incomplete application rules could lead to inconsistent treatment of applicants, while unclear approval and authorization requirements could affect the integrity and security of the system.

The separate Inspection Issue Log contains the individual issue descriptions, requirement locations, classifications and severity levels.

## Product Appraisal

**RECOMMENDATION**

- [ ] Accepted as is
- [ ] Conditionally accepted upon verification
- [x] Reinspect following rework
- [ ] Inspection not completed

Our group recommends reinspection following rework because eight major issues were reported during the inspection. Several of these issues affect essential system functions, including grant application submission, Department Chair approval, user authorization and data retention.

Although the SRS provides a useful foundation for the Grants Management System, several requirements remain incomplete, unclear or difficult to verify. These issues could lead to inconsistent implementation, security risks and difficulties during system testing.

Reinspection is recommended to ensure that the identified issues are properly addressed before the SRS is accepted.

**OTHER COMMENTS**

The inspected SRS contains several positive features, including requirement identifiers, structured use cases, alternative flows, security requirement statuses and verification tables. These features helped our group locate requirements and identify related issues across different sections.

However, improvements are needed in requirements completeness, clarity, consistency, traceability and testability.

The original authoring group should review the Inspection Issue Log, address the identified defects and ensure that related requirements remain consistent throughout the document. Unresolved business rules and policy decisions should be clearly documented and supported by available stakeholder evidence.

Following rework, the corrected requirements should be inspected again to confirm that the identified issues have been addressed without introducing new inconsistencies.

Overall, the inspection helped our group identify important requirements defects and demonstrated the importance of reviewing related requirements across functional, data, interface and security sections.

---

*Copyright © 2001 by Karl E. Wiegers. Permission is granted to use, modify, and distribute this document.*
