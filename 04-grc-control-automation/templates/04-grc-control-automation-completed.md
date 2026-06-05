# GRC Control Automation Design: Automated User Access Review

## Project Overview

This project simulates the design and implementation of an automated User Access Review (UAR) control for a SaaS organization preparing for SOC 2 Type II and ISO 27001 certification audits.

The objective was to replace a manual quarterly access review process with a continuous compliance monitoring solution that automatically identifies access violations, generates audit evidence, and reduces operational risk.

---

# Skills Demonstrated

- Governance, Risk & Compliance (GRC)
- SOC 2 Controls
- ISO 27001 Controls
- Identity & Access Management (IAM)
- Compliance Automation
- Continuous Controls Monitoring (CCM)
- Audit Readiness
- Security Operations
- Risk Assessment
- Security Architecture

---

# Business Scenario

## Organization Profile

**Organization:** CloudTrack Technologies Pvt. Ltd.

CloudTrack is a cloud-native SaaS company with:

- 250 employees
- AWS infrastructure
- Azure Active Directory
- GitHub Enterprise
- Jira Cloud
- Multi-tenant SaaS application

The organization performs quarterly user access reviews to satisfy:

- SOC 2 CC6 Controls
- ISO 27001 Access Control Requirements
- Customer Security Assessments

---

## Business Challenge

The existing review process was entirely manual.

Managers received spreadsheets containing employee access rights and were required to manually verify:

- Active employees
- Role appropriateness
- Privileged access assignments
- Terminated user accounts

The process required approximately 80 hours per quarter and frequently produced incomplete evidence for auditors.

---

# Control Objective

## Original Control

> User access rights shall be reviewed periodically to ensure that access remains appropriate and aligned with business requirements.

---

## Control Intent

### Primary Objective

Prevent unauthorized access to sensitive systems.

### Secondary Objective

Identify excessive privileges and orphaned accounts.

### Compliance Objective

Provide evidence supporting:

- SOC 2 CC6
- ISO 27001 Control 5.18
- Customer Due Diligence Requests

---

# Current State Assessment

## Existing Process

```text
HR System
   │
   ▼
Export Employee List
   │
   ▼
Export Access Reports
   │
   ▼
Merge Data in Excel
   │
   ▼
Manager Review
   │
   ▼
Collect Sign-Off
   │
   ▼
Store Evidence
```

---

## Key Challenges

### Finding 01 — Manual Data Collection

**Observation**

Access reports are manually extracted from multiple systems.

**Risk**

Incomplete or outdated data may be reviewed.

**Impact**

High

---

### Finding 02 — Delayed Reviews

**Observation**

Reviews occur quarterly.

**Risk**

Unauthorized access may remain active for months.

**Impact**

High

---

### Finding 03 — Evidence Gaps

**Observation**

Evidence is stored manually in shared folders.

**Risk**

Auditors may challenge evidence completeness.

**Impact**

Medium

---

# Proposed Automation Design

## Future State Architecture

```text
HRIS (Workday)
        │
        ▼
Identity Provider (Azure AD)
        │
        ▼
Compliance Automation Engine
        │
 ┌──────┼─────────┐
 ▼      ▼         ▼
Rule   Alert    Evidence
Engine Engine   Repository
 │
 ▼
Compliance Dashboard
```

---

# Data Sources

| System | Data Collected |
|----------|----------|
| Workday | Employee Status |
| Azure AD | User Accounts |
| AWS IAM | Cloud Permissions |
| GitHub Enterprise | Repository Access |
| Jira Cloud | Project Permissions |

---

# Automated Detection Logic

## Rule 01 — Orphaned Account Detection

### Logic

```yaml
rule_id: UAR-001
name: Orphaned User Detection

condition:
  employee_status: terminated
  account_status: active

action:
  severity: high
  alert: security-team
```

### Purpose

Detect active accounts belonging to terminated employees.

---

## Rule 02 — Excessive Privilege Detection

### Logic

```yaml
rule_id: UAR-002
name: Excessive Privilege Detection

condition:
  role: employee
  access_level: administrator

action:
  severity: high
  alert: compliance-team
```

### Purpose

Identify privilege escalation risks.

---

## Rule 03 — Dormant Account Detection

### Logic

```yaml
rule_id: UAR-003
name: Dormant Account Detection

condition:
  last_login: >90_days

action:
  severity: medium
  alert: manager
```

### Purpose

Identify inactive accounts requiring review.

---

# Automated Evidence Generation

## Generated Evidence

| Evidence | Format | Frequency |
|----------|----------|----------|
| Access Review Report | PDF | Monthly |
| User Inventory | CSV | Daily |
| Rule Violations | JSON | Real-Time |
| Manager Approvals | PDF | On Demand |
| Compliance Dashboard Export | PDF | Monthly |

---

## Auditor-Ready Outputs

### Monthly Access Review Report

Contains:

- Total Users
- Privileged Users
- Orphaned Accounts
- Dormant Accounts
- Access Exceptions
- Manager Sign-Off

---

### Quarterly Compliance Package

Contains:

- Access Review Summary
- Exception Reports
- Remediation Evidence
- Approval Records

---

# Human Decision Points

Automation does not eliminate human judgment.

The following decisions remain manual:

| Activity | Owner |
|----------|----------|
| Approve access exceptions | Manager |
| Accept residual risk | GRC Team |
| Approve privileged access | Security Team |
| Terminate user access | System Owner |

---

# Technology Stack

| Component | Selected Technology |
|----------|----------|
| HR System | Workday |
| Identity Provider | Azure AD |
| Cloud Platform | AWS |
| Automation Platform | Python + AWS Lambda |
| Data Storage | Amazon S3 |
| Dashboards | Power BI |
| Alerting | Microsoft Teams |
| Evidence Repository | SharePoint |

---

# Risk Reduction Analysis

## Before Automation

| Risk | Rating |
|---------|---------|
| Orphaned Accounts | High |
| Missed Reviews | High |
| Evidence Gaps | Medium |
| Delayed Detection | High |

---

## After Automation

| Risk | Rating |
|---------|---------|
| Orphaned Accounts | Low |
| Missed Reviews | Low |
| Evidence Gaps | Low |
| Delayed Detection | Low |

---

## Estimated Risk Reduction

**72% reduction in access governance risk**

---

# Compliance Mapping

| Framework | Control |
|------------|------------|
| ISO 27001 | 5.15 Access Control |
| ISO 27001 | 5.18 Access Rights |
| SOC 2 | CC6.1 |
| SOC 2 | CC6.2 |
| SOC 2 | CC6.3 |
| NIST CSF | PR.AC |
| CIS Controls | Control 6 |

---

# Implementation Roadmap

## Phase 1

- Connect data sources
- Build access inventory

**Duration:** 4 Weeks

---

## Phase 2

- Deploy rule engine
- Configure alerts

**Duration:** 3 Weeks

---

## Phase 3

- Generate audit evidence
- Deploy dashboards

**Duration:** 3 Weeks

---

## Phase 4

- User Acceptance Testing
- Auditor Validation

**Duration:** 2 Weeks

---

# Success Metrics

| Metric | Before | Target |
|----------|----------|----------|
| Review Effort | 80 Hours | 8 Hours |
| Detection Time | 90 Days | <24 Hours |
| Evidence Coverage | 70% | 100% |
| Orphaned Accounts | 12 | 0 |
| Audit Readiness | Medium | High |

---

# Lessons Learned

- Compliance controls should be continuously monitored rather than periodically reviewed.
- Automation improves evidence quality and audit readiness.
- Human oversight remains essential for risk acceptance decisions.
- Identity governance is one of the most impactful areas for compliance automation.
- Continuous Controls Monitoring (CCM) significantly reduces operational compliance risk.

---

# Final Outcome

The proposed automation solution transforms a quarterly manual control into a continuously monitored control with automated evidence generation and real-time detection capabilities.

The design improves audit readiness, reduces operational effort, and strengthens compliance with SOC 2 and ISO 27001 requirements.

---

# Author

**Swayam Nandi**

Governance, Risk & Compliance (GRC) Portfolio

SOC 2 | ISO 27001 | Compliance Automation | Continuous Controls Monitoring
