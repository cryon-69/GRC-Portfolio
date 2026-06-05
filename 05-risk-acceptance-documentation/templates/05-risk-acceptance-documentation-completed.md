# Risk Acceptance Assessment: Legacy VPN Without MFA

## Project Overview

This project simulates a formal risk acceptance assessment conducted for a legacy VPN service that does not support Multi-Factor Authentication (MFA).

The objective was to evaluate the security, operational, financial, and compliance implications of maintaining the legacy solution, assess available remediation options, and provide an executive recommendation.

This project demonstrates practical understanding of:

- Risk Management
- Risk Acceptance
- Security Governance
- Cost-Benefit Analysis
- Executive Decision Making
- ISO 27001 Risk Treatment
- Cybersecurity Risk Assessment

---

# Skills Demonstrated

- Risk Assessment
- Risk Treatment Planning
- Risk Acceptance Process
- Governance, Risk & Compliance (GRC)
- Executive Reporting
- Business Impact Analysis
- ISO 27001 Risk Management
- Security Governance

---

# Business Scenario

## Organization Profile

**Organization:** CloudTrack Technologies Pvt. Ltd.

CloudTrack operates a hybrid workforce supporting customers across North America, Europe, and Asia.

Remote employees connect to internal resources through a legacy VPN appliance deployed more than six years ago.

The VPN platform currently supports:

- Username/password authentication
- Active Directory integration
- Session logging

However, it does not support:

- Multi-Factor Authentication (MFA)
- Conditional Access Policies
- Modern Identity Federation

---

## Business Challenge

The organization identified the absence of MFA as a significant security concern.

A replacement solution is available but requires:

- New licensing
- Infrastructure migration
- User retraining
- Temporary operational disruption

Management requested a formal risk assessment to determine whether the risk should be accepted temporarily while migration planning is completed.

---

# Risk Statement

## Risk Description

Unauthorized users may gain access to corporate systems through compromised VPN credentials because the current VPN platform does not enforce Multi-Factor Authentication.

---

## Potential Scenarios

### Scenario 1 — Credential Theft

An employee enters credentials into a phishing page.

The attacker successfully authenticates to the VPN using stolen credentials.

---

### Scenario 2 — Password Reuse

An employee reuses a password from another service that becomes compromised.

Attackers use credential stuffing techniques against the VPN portal.

---

### Scenario 3 — Insider Misuse

A former employee's credentials remain active longer than expected.

Unauthorized access occurs before account deactivation.

---

# Risk Assessment

## Likelihood Analysis

| Factor | Assessment |
|----------|----------|
| Threat Actor Interest | High |
| Attack Complexity | Low |
| Detection Capability | Medium |
| Historical Industry Incidents | High |

---

### Likelihood Rating

**Moderate-High**

### Rationale

Credential theft and password attacks remain among the most common attack vectors observed globally.

The absence of MFA significantly increases the probability of successful account compromise.

---

## Impact Analysis

| Impact Area | Potential Consequence |
|-------------|----------------------|
| Data Breach | Exposure of customer information |
| Financial Loss | Incident response and recovery costs |
| Regulatory Action | Potential GDPR implications |
| Reputation | Loss of customer trust |
| Business Disruption | Service interruption and investigation activities |

---

### Estimated Impact

| Scenario | Estimated Cost |
|------------|------------|
| Minor Incident | $25,000 |
| Moderate Incident | $150,000 |
| Major Breach | $500,000+ |

---

### Most Likely Financial Impact

**$150,000**

---

# Existing Controls Assessment

## Controls Currently Implemented

| Control | Status |
|----------|----------|
| Password Complexity | Implemented |
| Active Directory Integration | Implemented |
| Endpoint Protection | Implemented |
| Security Awareness Training | Implemented |
| VPN Logging | Implemented |

---

## Missing Controls

| Control | Risk Impact |
|----------|----------|
| Multi-Factor Authentication | High |
| Conditional Access | Medium |
| Device Trust Validation | Medium |

---

## Overall Control Effectiveness

**Adequate but Incomplete**

The organization has implemented several foundational controls, but the lack of MFA remains a significant security gap.

---

# Options Analysis

## Option A — Immediate Replacement

### Description

Replace the VPN solution immediately and deploy MFA across the organization.

### Cost

$80,000

### Timeline

2 Months

### Residual Risk

Low

### Advantages

- Strongest security posture
- Compliance improvement
- Reduced credential attack risk

### Disadvantages

- High implementation cost
- Operational disruption

---

## Option B — Phased Migration

### Description

Deploy MFA-capable VPN infrastructure gradually over six months.

### Cost

$45,000

### Timeline

6 Months

### Residual Risk

Medium

### Advantages

- Lower disruption
- Controlled rollout
- Reduced implementation risk

### Disadvantages

- Risk remains during transition

---

## Option C — Accept Risk

### Description

Continue operating the existing VPN without changes.

### Cost

$0

### Residual Risk

High

### Advantages

- No immediate expenditure

### Disadvantages

- Elevated security risk
- Potential audit findings
- Increased breach probability

---

## Option D — Temporary Acceptance with Compensating Controls

### Description

Maintain the legacy VPN while implementing additional security controls.

### Cost

$12,000

### Timeline

30 Days

### Residual Risk

Medium-High

### Compensating Controls

- Enhanced monitoring
- VPN anomaly detection
- Weekly privileged account reviews
- Security awareness campaign

---

# Recommendation

## Selected Option

### Option D — Temporary Acceptance with Compensating Controls

---

## Rationale

### Reason 1

Immediate replacement is not feasible due to budget and operational constraints.

### Reason 2

Compensating controls significantly reduce risk while migration planning continues.

### Reason 3

The approach balances security, cost, and business continuity requirements.

---

# Immediate Actions

## Within 30 Days

- [ ] Enable enhanced VPN monitoring
- [ ] Conduct privileged account review
- [ ] Launch phishing awareness campaign
- [ ] Implement VPN access alerting

---

# Future Commitments

| Action | Timeline |
|---------|----------|
| Select replacement VPN solution | 90 Days |
| Pilot MFA deployment | 120 Days |
| Complete migration | 180 Days |

---

# Residual Risk Assessment

Even after compensating controls are implemented, certain risks remain.

| Residual Risk | Reason |
|--------------|---------|
| Credential Theft | MFA still unavailable |
| Password Reuse Attacks | Authentication remains single-factor |
| Human Error | User behavior cannot be fully controlled |

---

# Compliance Impact

## ISO 27001

Relevant Controls:

- 5.15 Access Control
- 5.17 Authentication Information
- 8.5 Secure Authentication

Impact:

Temporary deviation accepted with documented justification.

---

## SOC 2

Relevant Controls:

- CC6.1
- CC6.2

Impact:

Compensating controls required to maintain acceptable assurance.

---

# Risk Acceptance Decision

## Final Decision

### ACCEPT TEMPORARILY WITH COMPENSATING CONTROLS

---

## Expiration Date

31 December 2026

---

## Re-Assessment Triggers

This acceptance must be reviewed if:

- Security incident occurs
- Regulatory requirements change
- VPN vendor support ends
- MFA deployment becomes available
- Risk appetite changes

---

# Lessons Learned

- Not every risk should be immediately remediated.
- Security decisions must consider business realities.
- Risk acceptance requires documented ownership.
- Compensating controls can reduce risk while long-term solutions are implemented.
- Effective governance requires balancing security, cost, and operational impact.

---

# Final Outcome

The organization accepted the VPN authentication risk temporarily while implementing compensating controls and planning a phased migration to a modern MFA-capable solution.

The decision reduced operational disruption while maintaining risk within acceptable tolerance levels.

---

# Author

**Swayam Nandi**

Governance, Risk & Compliance (GRC) Portfolio

Risk Management | Risk Acceptance | Security Governance | ISO 27001

