# OctoAcme — Role Interactions & RACI

This document operationalizes the role definitions in [Roles and Personas](octoacme-roles-and-personas.md) by providing a RACI matrix, a cross-phase handoff checklist, and a meeting cadence ownership table.

**Legend**: O = Owner (accountable, one per row), R = Reviewer / Contributor, I = Informed only

---

## RACI Matrix by Phase

### Initiation

| Activity | PM | PdM | Developer | UX Designer | QA Lead | DevOps Engineer |
|---|---|---|---|---|---|---|
| Draft Project One-pager | O | R | I | I | I | I |
| Identify & confirm stakeholders | O | R | I | I | I | I |
| Define success metrics | R | O | I | R | I | I |
| Schedule kickoff meeting | O | R | R | R | R | R |

### Planning

| Activity | PM | PdM | Developer | UX Designer | QA Lead | DevOps Engineer |
|---|---|---|---|---|---|---|
| Create & prioritize backlog | R | O | R | R | R | I |
| Write acceptance criteria | R | O | R | R | R | I |
| Define Definition of Done | R | R | R | R | O | R |
| Estimate effort | R | R | O | R | R | R |
| Plan release timeline | O | R | R | I | R | R |
| User research / design specs | I | R | I | O | I | I |

### Execution & Tracking

| Activity | PM | PdM | Developer | UX Designer | QA Lead | DevOps Engineer |
|---|---|---|---|---|---|---|
| Daily standup facilitation | R | I | R | R | R | R |
| Feature implementation | I | I | O | I | I | I |
| Design review & feedback | I | R | R | O | I | I |
| PR review & merge | I | I | O | I | I | R |
| Manual QA & acceptance testing | I | I | R | R | O | I |
| Update risk register | O | R | R | I | R | R |
| Escalate blockers | O | R | R | R | R | R |

### Release & Deployment

| Activity | PM | PdM | Developer | UX Designer | QA Lead | DevOps Engineer |
|---|---|---|---|---|---|---|
| Release readiness check (go/no-go) | O | I | I | I | R | R |
| Draft release notes | R | R | R | I | R | O |
| Staging deployment & smoke tests | I | I | R | I | R | O |
| Production deployment | I | I | R | I | I | O |
| Post-deploy verification | R | I | R | I | R | O |
| Stakeholder release announcement | O | R | I | I | I | R |

### Retrospective

| Activity | PM | PdM | Developer | UX Designer | QA Lead | DevOps Engineer |
|---|---|---|---|---|---|---|
| Facilitate retrospective | O | R | R | R | R | R |
| Capture action items | O | R | R | R | R | R |
| Track improvement backlog items | O | R | R | R | R | R |

---

## Cross-Role Handoff Checklist

Use this checklist at each key handoff point to prevent gaps.

### Design → Development Handoff
- [ ] Wireframes and/or prototypes finalized and linked in the ticket
- [ ] Acceptance criteria include UX expectations (layout, interactions, error states)
- [ ] UX Designer available for questions during the sprint
- [ ] Any open design decisions noted in the ticket

### Development → QA Handoff
- [ ] PR merged to integration branch; CI passing
- [ ] Developer has self-tested against acceptance criteria
- [ ] Known edge cases documented in the ticket
- [ ] Environment and test data notes added by Developer

### QA → Release Handoff
- [ ] All acceptance criteria verified and marked Done by QA Lead
- [ ] No open P0/P1 defects; P2+ defects logged with agreed disposition
- [ ] QA sign-off recorded in the release ticket or release notes draft
- [ ] Smoke test scripts reviewed with DevOps Engineer

### Release → Post-Deploy Handoff
- [ ] Production deployment completed; pipeline green
- [ ] Smoke tests passing in production
- [ ] Monitoring dashboards reviewed (errors, latency, usage)
- [ ] Stakeholder announcement sent by PM / DevOps Engineer
- [ ] Any incident response actions noted for retrospective

---

## Meeting Cadence Ownership

| Meeting | Frequency | Facilitator | Required Attendees | Optional |
|---|---|---|---|---|
| Project Kickoff | Once at project start | PM | PM, PdM, Developers, UX Designer, QA Lead, DevOps Engineer | Stakeholders |
| Sprint Planning | Per sprint | PM | PM, PdM, Developers, QA Lead | UX Designer, DevOps Engineer |
| Daily Standup | Daily | PM or rotating | All delivery team members | PdM, Stakeholders |
| Design Review | As needed (pre-sprint) | UX Designer | UX Designer, PdM, Developers | PM, QA Lead |
| Weekly PM + PdM Sync | Weekly | PM | PM, PdM | — |
| Bug Triage | Weekly or as needed | QA Lead | QA Lead, Developers, PM | DevOps Engineer |
| Sprint Demo / Review | Per sprint | PM | All delivery team, Stakeholders | PdM, Sponsor |
| Release Go/No-Go | Per release | PM | PM, QA Lead, DevOps Engineer | PdM |
| Retrospective | Per sprint or release | PM | All delivery team | Stakeholders |
| Monthly Stakeholder Update | Monthly | PM | PM, PdM, Stakeholders | Sponsor |

---

## Escalation Quick Reference

| Situation | First Contact | Escalate To | Final Escalation |
|---|---|---|---|
| Technical blocker | Developer | PM | PdM / Sponsor |
| Defect blocking release | QA Lead | PM | PdM |
| Deployment failure | DevOps Engineer | PM | Sponsor |
| Scope / requirements conflict | PdM | PM | Sponsor |
| Security incident | DevOps Engineer + Security on-call | PM | Sponsor |
| User research invalidates design | UX Designer | PdM | PM |

---

*See also: [Roles and Personas](octoacme-roles-and-personas.md) · [Risks & Communication](octoacme-risks-and-communication.md) · [Release & Deployment](octoacme-release-and-deployment.md)*
