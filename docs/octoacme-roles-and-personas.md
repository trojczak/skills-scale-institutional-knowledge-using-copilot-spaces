# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

## How to use this document

- **Ownership assignment**: When creating artifacts (One-pager, backlog, risk register, release notes), refer to the role definitions below to assign a clear owner. Every artifact should have exactly one owner.
- **Decision gates**: At each phase gate (go/no-go to planning, release readiness), confirm the required roles have reviewed and signed off as described in each persona's responsibilities.
- **Escalation paths**: When a blocker or risk surfaces, use the interaction notes in each persona to identify the correct escalation contact. Default path: Developer → PM → PdM → Sponsor.
- **Copilot Spaces**: Each persona can be used as a persona prompt in Copilot Spaces to shape role-specific guidance and context.

See also: [Role Interactions & RACI](octoacme-role-interactions-and-raci.md) for a full ownership matrix and handoff checklist.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## UX Designer / User Researcher

### Role Summary
UX Designers and User Researchers advocate for the end user throughout the product lifecycle. They ensure that features are usable, desirable, and aligned with real user needs before and during development.

### Responsibilities
- Plan and conduct user research (interviews, usability tests, surveys)
- Create wireframes, prototypes, and interaction specifications
- Collaborate with PdM to validate problem statements and success criteria
- Contribute user insights to backlog refinement and acceptance criteria
- Review implemented features for usability before QA sign-off

### Goals
- Reduce rework by validating designs before development begins
- Ensure released features meet user expectations
- Build a shared understanding of user needs across the team

### Typical Communication
- Design reviews with Developers and PdM before sprint start
- Usability findings shared in sprint demos and written summaries
- Asynchronous feedback via design tools (e.g., Figma comments) and PR reviews

### Key Interactions & Hand-offs
- → **PdM**: shares research insights to inform backlog priorities and acceptance criteria
- → **Developers**: provides specs and answers design questions during implementation
- → **QA Lead**: flags usability concerns discovered during QA that may need design input
- → **PM**: raises timeline risks if research reveals major design pivots are needed

---

## QA Lead / Quality Owner

### Role Summary
The QA Lead defines and enforces quality standards across the delivery lifecycle. They coordinate testing efforts, manage the Definition of Done, and are the final gate before features are marked ready for release.

### Responsibilities
- Define and maintain the Definition of Done (DoD) and acceptance testing standards
- Coordinate manual and automated test coverage across the sprint
- Facilitate bug triage and ensure defects are prioritized and resolved before release
- Validate that all acceptance criteria are met before moving items to Done
- Sign off on release readiness from a quality perspective

### Goals
- Prevent quality regressions from reaching production
- Ensure consistent, repeatable testing across all feature work
- Make the go/no-go release decision clear and evidence-based

### Typical Communication
- QA status updates in weekly delivery syncs
- Bug triage sessions with Developers and PM
- Go/no-go recommendation shared with PM and DevOps Engineer before each release

### Key Interactions & Hand-offs
- → **Developers**: receives completed features for testing; sends defect reports back
- → **PdM**: confirms acceptance criteria coverage and flags ambiguous requirements
- → **PM**: escalates blocking defects that threaten the release timeline
- → **DevOps Engineer**: coordinates smoke test execution during staging deployment
- → **UX Designer**: escalates usability defects that require design input

---

## DevOps Engineer / Release Manager

### Role Summary
DevOps Engineers own the delivery pipeline, deployment infrastructure, and release process. They ensure changes move safely and efficiently from development to production and that incidents are resolved quickly.

### Responsibilities
- Design, maintain, and improve CI/CD pipelines and deployment automation
- Define and enforce deployment runbooks and rollback procedures
- Lead release ceremonies: staging deployments, go/no-go checkpoints, and production deploys
- Monitor production health post-release and coordinate incident response
- Maintain and update the deployment checklist and rollback playbook

### Goals
- Make deployments safe, repeatable, and low-risk
- Minimize mean time to recovery (MTTR) when incidents occur
- Continuously improve pipeline speed and reliability

### Typical Communication
- Release readiness check with QA Lead and PM before each deployment
- Post-deploy status announcement to stakeholders
- Incident communications following the template in [Risks & Communication](octoacme-risks-and-communication.md)

### Key Interactions & Hand-offs
- → **PM**: confirms deployment window and communicates go/no-go status
- → **QA Lead**: coordinates smoke tests in staging; waits for QA sign-off before production deploy
- → **Developers**: reviews PR pipelines; assists with environment and deployment issues
- → **Stakeholders**: sends release announcements and post-incident summaries

---

## Role Interactions & Ownership

Use the tables below to quickly identify who owns what across key artifacts, ceremonies, and decision gates.  
**Legend**: O = Owner (accountable, one per row), R = Reviewer / Contributor, I = Informed only

### Artifacts

| Artifact | PM | PdM | Developer | UX Designer | QA Lead | DevOps Engineer |
|---|---|---|---|---|---|---|
| Project One-pager | O | R | I | I | I | I |
| Roadmap & Release Plan | R | O | I | R | I | I |
| Sprint Backlog | R | O | R | R | R | I |
| Acceptance Criteria | R | O | R | R | R | I |
| Definition of Done | R | R | R | R | O | R |
| Risk Register | O | R | R | I | R | R |
| Release Notes | R | R | R | I | R | O |
| Deployment Checklist | I | I | R | I | R | O |
| Usability / Research Summary | I | R | I | O | I | I |

### Ceremonies

| Ceremony | PM | PdM | Developer | UX Designer | QA Lead | DevOps Engineer |
|---|---|---|---|---|---|---|
| Project Kickoff | O | R | R | R | R | R |
| Sprint Planning | O | R | R | R | R | I |
| Daily Standup | R | I | R | R | R | R |
| Design Review | I | R | R | O | I | I |
| Sprint Demo / Review | O | R | R | R | R | I |
| Bug Triage | R | I | R | I | O | R |
| Release Go/No-Go | O | I | I | I | R | R |
| Retrospective | O | R | R | R | R | R |

### Decision Gates

| Decision Gate | Owner | Required Input From |
|---|---|---|
| Go to Planning (problem validated) | PdM | PM, UX Designer, Stakeholders |
| Sprint Start (backlog ready) | PM | PdM, QA Lead |
| Feature → Done (AC met) | QA Lead | Developer, PdM, UX Designer |
| Release Readiness (go/no-go) | PM | QA Lead, DevOps Engineer, PdM |
| Incident Resolved | DevOps Engineer | PM, QA Lead |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

