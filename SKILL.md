---
name: operations-cx-super-skill
description: >
  Comprehensive operations and customer experience skill merging Perplexity Computer's 5 CX skills
  with Claude Code's project management, file organization, invoice processing, scrum methodology,
  and verification workflows. Use for support ticket triage, customer response drafting, escalation
  management, knowledge base articles, customer research, project management, sprint planning, file
  organization, invoice processing, or any operations and CX work.
license: MIT
metadata:
  author: get-zeked
  version: '1.0'
---

# Operations & CX Super-Skill

A unified operations and customer experience reference covering support excellence, project delivery,
agile execution, file and financial document management, and quality verification. Merge of
Perplexity Computer's five CX skills and five Claude Code operations skills.

---

## Gap Analysis

| Domain | Source Skill | Coverage Here |
|--------|-------------|---------------|
| Ticket triage & classification | cx-ticket-triage | Section 2 — priority matrix, routing rules, SLA table |
| Customer response drafting | cx-response-drafting | Section 3 — tone spectrum, templates, channel guidelines |
| Escalation management | cx-escalation | Section 4 — structured format, reproduction steps, impact |
| Customer research & confidence scoring | cx-customer-research | Section 5 — five-tier source hierarchy, synthesis structure |
| Knowledge base management | cx-knowledge-management | Section 6 — article types, maintenance cadence, taxonomy |
| Portfolio & senior PM | senior-pm | Section 7 — WSJF/RICE/ICE, RAG status, risk EMV |
| Sprint & agile operations | scrum-master | Section 8 — health scoring, velocity, ceremony guides |
| File & document organization | file-organizer | Section 9 — analysis workflow, naming conventions |
| Invoice & financial document processing | invoice-organizer | Section 10 — extraction, filename format, CSV reporting |
| Operational quality & verification | verification-before-completion | Section 11 — iron law, gate function, red flags |

**Cross-domain gaps filled by this merge not present in any single source skill:**
- Triage -> escalation -> KB article pipeline in one workflow
- Sprint velocity data feeding PM portfolio risk scoring
- Invoice categorization aligned with project cost-center taxonomy
- Verification gates applied to customer-facing content, not just code
- Perplexity Computer integration capabilities for CX workflows (CRM, email, calendar)

---

## Section 2 — Ticket Triage & Classification

### Category Taxonomy (9 Categories)

| Category | Signal Words |
|----------|--------------|
| **Bug** | error, broken, crash, not working, unexpected, wrong, failing |
| **How-to** | how do I, can I, where is, setting up, configure, help with |
| **Feature Request** | would be great if, wish I could, any plans to, requesting |
| **Billing** | charge, invoice, payment, subscription, refund, upgrade, downgrade |
| **Account** | login, password, access, permission, SSO, locked out, can't sign in |
| **Integration** | API, webhook, integration, connect, OAuth, sync, third-party |
| **Security** | data breach, unauthorized, compliance, GDPR, SOC 2, vulnerability |
| **Data** | missing data, export, import, migration, incorrect data, duplicates |
| **Performance** | slow, timeout, latency, down, unavailable, degraded |

**Category determination rules:**
- Root cause drives the primary category, not the surface symptom
- Bug AND feature request present -> Bug is primary
- Can't log in due to a bug -> Bug (not Account)
- "It used to work and now it doesn't" -> Bug
- "I want it to work differently" -> Feature Request
- When in doubt, lean Bug — better to investigate than dismiss

### Priority Framework (P1–P4)

| Priority | Criteria | Response SLA | Update Cadence |
|----------|----------|-------------|----------------|
| **P1 Critical** | Production down, data loss/corruption, security breach, all/most users | 1 hour | Every 1–2 hours until resolved |
| **P2 High** | Major feature broken, no workaround, many users affected | 4 hours | Every 4 hours |
| **P3 Medium** | Feature partially broken, workaround available, small group affected | 1 business day | Update within 3 business days |
| **P4 Low** | Cosmetic issue, general question, feature request | 2 business days | Resolution at normal pace |

### Priority Triage Matrix

| Impact / Breadth | All Users | Many Users | Small Group | Single User |
|------------------|-----------|-----------|-------------|-------------|
| **Production Down** | P1 | P1 | P2 | P2 |
| **Core Feature Broken** | P1 | P2 | P2 | P3 |
| **Major Feature Broken** | P2 | P2 | P3 | P3 |
| **Minor Feature Broken** | P2 | P3 | P3 | P4 |
| **Cosmetic / How-to** | P3 | P4 | P4 | P4 |

### Auto-Escalation Triggers

Bump priority up when:
- Customer waited longer than SLA allows
- 3+ customers report the same issue (pattern detected)
- Customer mentions executive involvement
- A previously working workaround stops working
- Issue expands in scope (more users, more data, new symptoms)

### Routing Rules

| Route to | When |
|----------|------|
| Tier 1 (frontline) | How-to, known issues with documented solutions, billing, password resets |
| Tier 2 (senior support) | Bugs needing investigation, complex config, integration troubleshooting |
| Engineering | Confirmed bugs needing code fixes, infrastructure, performance degradation |
| Product | Feature requests with demand, design decisions, workflow gaps |
| Security | Data access concerns, vulnerability reports, compliance questions |

---

## Section 3 — Customer Response Drafting

### Tone Spectrum

| Customer State | Tone | Avoid |
|----------------|------|-------|
| Frustrated / Angry | Warm, empathetic, decisive | Defensive language, jargon, excuses |
| Confused / Lost | Patient, clear, step-by-step | Assumptions, unexplained technical terms |
| Neutral / Informational | Professional, concise | Overly formal, unnecessary padding |
| Escalating | Calm, accountable, specific | Dismissing urgency, vague timelines |
| Satisfied / Follow-up | Friendly, confirmatory | Over-selling, unnecessary follow-up requests |

### Channel-Specific Guidelines

| Channel | Length | Tone | Special Notes |
|---------|--------|------|---------------|
| Email | Medium (3–6 paragraphs) | Professional-warm | Full context, subject line precision |
| Live chat | Short bursts | Conversational | Respond in < 2 minutes; chunk complex answers |
| Community forum | Medium-long | Helpful, public-facing | No account specifics — visible to all users |
| Slack / Teams (internal) | Short | Direct | Use threads; tag only who needs to act |
| Status page | Very brief | Factual | Three-part: what, impact, status + ETA |

### Response Templates

**Bug — Initial Response:**
```
Thank you for reporting this. I can see how [specific impact] would be disruptive.

I've logged this as a [priority] issue and our team is investigating.
[If workaround exists: "In the meantime, you can [workaround]."]

I'll update you within [SLA timeframe] with what we find.
```

**Feature Request — Initial Response:**
```
Thank you for this suggestion — I can see why [capability] would be valuable
for your workflow.

I've documented this and shared it with our product team. While I can't commit
to a specific timeline, your feedback directly informs our roadmap priorities.

[If alternative exists: "In the meantime, you might find [alternative] helpful."]
```

**Outage Notification:**
```
We're aware of an issue affecting [product/feature].

What happened: [Clear, non-technical explanation]
Impact: [How it affects them specifically]
Status: [Investigating / Identified / Fixing / Resolved]
ETA: [Specific time, or "we'll update every X hours"]

[If applicable: "In the meantime, you can [workaround]."]
I'm tracking this and will update you as soon as we have a resolution.
```

### Follow-up Cadence

| Situation | Follow-up Timing |
|-----------|------------------|
| Unanswered question | 2–3 business days |
| Open critical support issue | Daily until resolved |
| Open standard support issue | Every 2–3 days |
| After delivering bad news | 1 week to check sentiment |

---

## Section 4 — Escalation Management

### Escalation Tiers

| From | To | When |
|------|----|------|
| L1 | L2 | Deeper investigation needed, specialized knowledge required |
| L2 | Engineering | Confirmed bug, infrastructure issue, code change needed |
| L2 | Product | Feature gap causing pain, design decision needed |
| Any | Security | Potential data exposure — bypass normal tiers, escalate immediately |
| Any | Leadership | High-revenue customer at churn risk, SLA breach on critical account |

### Structured Escalation Format

```
ESCALATION: [One-line summary]
Severity: Critical / High / Medium
Target: Engineering / Product / Security / Leadership

IMPACT
- Customers affected: [Number and names]
- Workflow impact: [What's broken]
- Revenue at risk: [If applicable]
- SLA status: Within SLA / At risk / Breached

ISSUE DESCRIPTION
[3-5 sentences: what's happening, when it started, scope]

REPRODUCTION STEPS (for bugs)
1. [Specific step with exact values]
2. [Step]
Expected: [X]  |  Actual: [Y]
Environment: [Browser, OS, account type, plan level, feature flags]

WHAT'S BEEN TRIED
1. [Action] -> [Result]

CUSTOMER COMMUNICATION
- Last update: [Date — what was said]
- Customer expectation: [What they expect and by when]

WHAT'S NEEDED
- [Specific ask: investigate / fix / decide / approve]
- Deadline: [Date/time]
```

### Business Impact Assessment

| Dimension | Questions |
|-----------|----------|
| Breadth | How many customers/users affected? Is it growing? |
| Depth | How severely impacted? Blocked vs. inconvenienced? |
| Duration | How long has this been going on? |
| Revenue | What ARR is at risk? Pending deals affected? |
| Reputation | Could this become public? Reference customer? |
| Contractual | SLAs being breached? Contractual obligations? |

---

## Section 5 — Customer Research & Investigation

### Five-Tier Source Hierarchy

| Tier | Sources | Confidence |
|------|---------|------------|
| 1 — Official Internal | Product docs, KB, policy docs, API references | **High** |
| 2 — Organizational Context | CRM records, support tickets, internal docs, meeting notes | Medium-High |
| 3 — Team Communications | Chat history, email threads, calendar notes | Medium |
| 4 — External Sources | Web search, community forums, third-party docs | Low-Medium |
| 5 — Inferred / Analogical | Similar situations, analogous customers, best practices | **Low** |

### Answer Synthesis Structure

```
Direct Answer: [Bottom-line answer — lead with this]

Confidence: High / Medium / Low

Supporting Evidence:
- [Source 1]: [What it says]
- [Source 2]: [Corroborates or adds nuance]

Caveats:
- [Limitations or conditions on the answer]

Recommendation:
- [Ready to share with customer? Verification steps?]
```

### When to Escalate vs. Answer Directly

**Answer directly** when: official docs clearly address it; multiple sources corroborate;
question is factual and non-sensitive; no commitments, timelines, or pricing involved.

**Escalate or verify** when: roadmap commitments or timelines; pricing, legal, or contract terms;
security, compliance, or data handling; contradictory sources; custom customer configuration.

---

## Section 6 — Knowledge Base Management

### Article Types

| Type | Purpose | Trigger |
|------|---------|----------|
| How-to Guide | Step-by-step instructions | Recurring "how do I" questions |
| Troubleshooting | Diagnose and fix a specific problem | Bug resolved with reproducible steps |
| Reference | Comprehensive feature documentation | Feature launch or significant update |
| FAQ | Short answers to common questions | 3+ tickets with the same question |
| Release Notes | What changed and why | Every product release |
| Runbook | Internal process documentation | Operational procedures |

### KB Article Structure

```markdown
# [Title — action-oriented, searchable]

**Last Updated:** YYYY-MM-DD
**Applies To:** [Product version, plan, user role]

## Summary
[One-paragraph answer — readable without the full article]

## Prerequisites
- [What the user needs before starting]

## Steps
1. [Step with specific UI path]
2. [Step]

## Troubleshooting
| Symptom | Cause | Fix |
|---------|-------|-----|

## Related Articles
- [Link 1]
```

### Maintenance Cadence

| Trigger | Action |
|---------|--------|
| Product release | Review all affected articles within 48 hours |
| 3+ tickets cite article but problem persists | Rewrite article — it's not solving the problem |
| Article marked outdated | Review within 1 week |
| Quarterly audit | Verify all articles against current product behavior |

---

## Section 7 — Portfolio & Project Management

### Prioritization Frameworks

**WSJF (Weighted Shortest Job First)** — use for Agile/SAFe programs:
```
WSJF = (Business Value + Time Criticality + Risk Reduction) / Job Size
```
Score each dimension 1–10. Higher WSJF = higher priority.

**RICE** — use for product feature backlog:
```
RICE = (Reach x Impact x Confidence) / Effort
```
Reach: users/month; Impact: 0.25–3x multiplier; Confidence: 0–100%; Effort: person-months.

**ICE** — use for quick scoring when data is sparse:
```
ICE = Impact x Confidence x Ease
```
Score each 1–10. Sort descending.

### Portfolio RAG Status

| Status | Criteria |
|--------|----------|
| GREEN | On track — schedule, scope, and budget within tolerance |
| YELLOW | At risk — one dimension off-track but recoverable |
| RED | Critical — multiple dimensions at risk or action needed from leadership |

### Risk Expected Monetary Value (EMV)

```
EMV = Probability x Financial Impact
Total Portfolio Risk Reserve = Sum of all EMV values
```

---

## Section 8 — Sprint & Agile Operations

### Sprint Health Scoring

Score each dimension 1–5:

| Dimension | 1 (Poor) | 3 (Acceptable) | 5 (Excellent) |
|-----------|---------|----------------|---------------|
| Velocity stability | > 30% variance | 15–30% variance | < 15% variance |
| Sprint goal achievement | < 60% | 60–80% | > 80% |
| Scope churn | > 30% of sprint changed | 10–30% changed | < 10% changed |
| Bug injection rate | Increasing sprint-over-sprint | Flat | Decreasing |
| Team morale | Low/disengaged | Neutral | High/energized |

Sprint health = average of all dimensions. Score < 2.5 = retrospective required.

### Ceremony Guides

| Ceremony | Frequency | Duration | Owner | Output |
|---------|-----------|---------|-------|--------|
| Sprint Planning | Start of sprint | 2–4 hours | Product Owner + Scrum Master | Sprint backlog, sprint goal |
| Daily Standup | Daily | 15 min | Team | Impediment log update |
| Sprint Review | End of sprint | 1–2 hours | Product Owner | Stakeholder feedback, backlog update |
| Retrospective | End of sprint | 1–1.5 hours | Scrum Master | Action items for next sprint |
| Backlog Refinement | Weekly | 1 hour | Product Owner | Groomed backlog, story points |

---

## Section 9 — File & Document Organization

### File Analysis Workflow

```
1. Inventory — list all files with names, sizes, dates, types
2. Cluster — group by project, date range, content type
3. Identify duplicates — same name different path, same content different name
4. Flag anomalies — files in wrong location, unusual sizes
5. Propose structure — suggest target directory tree
6. Generate rename/move plan — show before/after for each file
7. Execute with confirmation — never auto-delete; always show plan first
```

### Naming Convention Standards

**General documents:**
```
YYYY-MM-DD_[project-or-client]_[description]_v[N].[ext]
Example: 2026-03-01_acme-corp_onboarding-checklist_v2.docx
```

**Reports / deliverables:**
```
[YYYY-MM]_[report-type]_[entity].[ext]
Example: 2026-02_monthly-report_product-team.pdf
```

**Meeting notes:**
```
[YYYY-MM-DD]_meeting_[participants-or-topic].[ext]
Example: 2026-03-01_meeting_q1-planning.md
```

**Avoid:** spaces in filenames (use hyphens), version suffixes like `_final_FINAL`,
date formats other than ISO-8601 (YYYY-MM-DD).

---

## Section 10 — Invoice & Financial Document Processing

### Invoice Data Extraction Fields

| Field | Notes |
|-------|-------|
| invoice_number | From document; `UNKNOWN` if missing |
| invoice_date | ISO-8601 format (YYYY-MM-DD) |
| due_date | ISO-8601; infer from payment terms if not explicit |
| vendor_name | Legal name from document |
| vendor_address | Full address block |
| line_items | Array: description, qty, unit_price, total |
| subtotal | Pre-tax amount |
| tax_amount | All tax line items combined |
| total_amount | Final amount due |
| currency | ISO-4217 code (USD, EUR, GBP) |
| payment_terms | Net 30, Net 60, Due on receipt, etc. |

### Invoice Filename Format

```
[YYYY-MM-DD]_[VendorName]_[InvoiceNumber]_[Amount][Currency].[ext]
Example: 2026-03-01_Acme-Corp_INV-2026-0042_1250.00USD.pdf
```

### CSV Output Columns

`invoice_number`, `invoice_date`, `due_date`, `vendor_name`, `total_amount`, `currency`,
`payment_terms`, `line_item_count`, `source_file`, `processing_date`

---

## Section 11 — Verification & Quality Gates

### The Iron Law

> **Never mark a task complete until you have verified the output matches the requirement.**

This applies equally to code, customer-facing content, financial documents, and deliverables.
"Done" means verified, not "I think it's done."

### Verification Gate Function

Before marking anything complete:

```
1. Re-read the original requirement (the actual text — not your memory of it)
2. Compare output to requirement line by line
3. Test the happy path
4. Test at least one edge case or failure mode
5. Check for regressions — did you break anything adjacent?
6. If sharing externally: grammar, tone, accuracy, brand compliance check
```

### Red Flags That Require Re-verification

- [ ] "I'm pretty sure this is right"
- [ ] Output generated in under 30 seconds for a complex task
- [ ] No test or review step was performed
- [ ] Requirement was interpreted, not read verbatim
- [ ] Task was marked done before observing the actual result
- [ ] Dependencies were assumed to be stable without checking

### Verification for Customer-Facing Content

Additional checks before sending to customers:
- [ ] Facts verified against primary sources (not memory)
- [ ] Commitments (timelines, features, pricing) approved before sending
- [ ] Tone matches customer's current sentiment and priority level
- [ ] No jargon the customer hasn't used first
- [ ] No confidential internal information included

---

## Section 12 — Perplexity Computer Capabilities for CX/Ops

### Connected Integration Categories for CX

| Integration | CX/Ops Use Case |
|-------------|------------------|
| Gmail / Outlook | Read customer emails, draft and send responses, search ticket history |
| Slack / Teams | Post internal updates, read support channels, manage escalation threads |
| CRM (Salesforce, HubSpot) | Pull account context, log interactions, update opportunity notes |
| Calendar | Schedule follow-ups, track SLA deadlines, book post-incident reviews |
| Google Sheets / Airtable | Pull ticket metrics, update status dashboards, log invoice data |
| Notion / Confluence | Create KB articles, update runbooks, document decisions |
| Jira / Linear | Create bug tickets, link support tickets, update sprint board |

### Scheduled CX Monitoring

Use scheduled agents for:
- **Daily SLA sweep:** check all open P1/P2 tickets -> alert if past SLA
- **Weekly ticket trend:** compare category distribution week-over-week -> flag spikes
- **Monthly KB audit:** check article view-to-ticket ratio -> flag underperforming articles
- **Sprint health report:** auto-generate velocity, scope churn, goal achievement metrics

---

## Appendix A: Cross-Domain Workflow — Triage to Resolution to KB Article

```
Step 1: TRIAGE (Section 2)
  -> Assign category + priority
  -> Set SLA clock
  -> Route to correct team

Step 2: INVESTIGATE (Section 5)
  -> Search 5-tier source hierarchy
  -> Assign confidence level to findings

Step 3: RESPOND (Section 3)
  -> Draft response using appropriate template
  -> Channel-appropriate length and tone
  -> Verify before sending (Section 11)

Step 4: ESCALATE IF NEEDED (Section 4)
  -> Use structured escalation format
  -> Include reproduction steps and business impact

Step 5: RESOLVE & DOCUMENT (Section 6)
  -> After resolution: does this warrant a KB article?
    - Recurring question (3+)? -> FAQ article
    - Bug with steps? -> Troubleshooting article
    - New process? -> How-to guide
  -> Write article, publish, link from ticket
```

## Appendix B: Prioritization Quick Reference

| Framework | Formula | When to Use |
|-----------|---------|-------------|
| WSJF | (BV + TC + RR) / JobSize | Agile/SAFe programs, comparing epics |
| RICE | (Reach x Impact x Confidence) / Effort | Product feature backlog |
| ICE | Impact x Confidence x Ease | Quick scoring with sparse data |
| P1-P4 matrix | Impact x Breadth table | Support ticket prioritization |

## Appendix C: Naming Convention Quick Reference

| Document Type | Format | Example |
|---------------|--------|--------|
| General document | `YYYY-MM-DD_client_description_vN.ext` | `2026-03-01_acme_proposal_v2.docx` |
| Monthly report | `YYYY-MM_report-type_entity.ext` | `2026-02_monthly-report_eng-team.pdf` |
| Meeting notes | `YYYY-MM-DD_meeting_topic.ext` | `2026-03-01_meeting_q1-planning.md` |
| Invoice | `YYYY-MM-DD_Vendor_InvNumber_AmountCCY.ext` | `2026-03-01_Acme_INV-0042_1250USD.pdf` |

---

*Operations & CX Super-Skill v1.0 — authored by get-zeked*
