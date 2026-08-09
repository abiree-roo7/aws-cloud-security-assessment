# AWS Cloud Security Assessment

## 1-Month Cybersecurity Internship Project

**Organization:** Elysium Cyber  
**Role:** Cybersecurity Intern  
**Duration:** 1 Month  
**Focus:** AWS Cloud Security, IAM, EC2, VPC, Network Security, Detection & Compliance

---

## Overview

This repository presents a sanitized portfolio version of a one-month cybersecurity internship project focused on assessing the security posture of an AWS environment.

The project involved reviewing cloud configurations, identifying security gaps, collecting technical evidence, mapping findings to security controls, and developing practical remediation recommendations.

The assessment covered four main areas:

- Identity and Access Management (IAM)
- EC2 and VPC security
- Network and Security Group configuration
- Security monitoring and detection

The work was performed using AWS security services and the AWS CLI, with findings assessed using a risk-based methodology and NIST security controls.

> **Note:** All client-specific identifiers, account information, infrastructure IDs, credentials, IP addresses, ARNs, and other sensitive information have been removed or anonymized from this public portfolio.
## Project Objectives

The main objectives of the assessment were to:

1. Review the security configuration of key AWS resources.
2. Identify configuration weaknesses and potential security risks.
3. Collect evidence using AWS CLI and AWS security services.
4. Assess findings against relevant security controls and benchmarks.
5. Prioritize findings according to severity and business risk.
6. Develop practical remediation recommendations.
7. Build a 30/60/90-day remediation roadmap.
8. Document the assessment in a professional security findings format.

---

## Assessment Methodology

The assessment followed a structured security review process:

```text
AWS Resource Inventory
        ↓
Configuration Review
        ↓
Evidence Collection
        ↓
Security Gap Identification
        ↓
Risk & Severity Assessment
        ↓
NIST / CIS Alignment
        ↓
Remediation Recommendations
        ↓
Before / After Validation
        ↓
30/60/90-Day Remediation Roadmap

---

# Week 1 — IAM Security Assessment

## Objective

The first phase of the engagement focused on reviewing the AWS Identity and Access Management (IAM) posture.

The objective was to identify weaknesses related to authentication, authorization, account access, and excessive permissions, and to assess whether IAM configurations followed security best practices.

## Activities Performed

During the IAM assessment, I:

- Reviewed IAM users, groups, and roles.
- Examined authentication and MFA configuration.
- Reviewed access keys and their status.
- Investigated inactive or unnecessary credentials.
- Reviewed IAM policies and permissions.
- Identified excessive or potentially unnecessary access.
- Collected configuration evidence using AWS CLI and AWS Config.
- Assessed findings against relevant NIST security controls.
- Assigned severity levels based on security impact.
- Developed remediation recommendations.

## Assessment Areas

| Area | Assessment |
|---|---|
| Authentication | Reviewed account authentication controls |
| MFA | Checked MFA enrollment and enforcement |
| Access Keys | Reviewed credential status and usage |
| Authorization | Examined IAM permissions and policies |
| Least Privilege | Identified excessive or unnecessary permissions |
| IAM Lifecycle | Reviewed inactive or unnecessary identities |
| Evidence | Collected AWS configuration and activity evidence |

## Evidence & Analysis

The assessment used AWS-native evidence to validate IAM findings rather than relying solely on configuration assumptions.

Configuration evidence was used to establish the state of IAM resources, while audit activity from AWS logging services was used where available to provide additional context.

Sensitive account identifiers, usernames, access keys, ARNs, and other environment-specific information have been removed from the public version of this project.

## Security Framework Alignment

The IAM assessment was mapped primarily to NIST security controls related to:

- **AC — Access Control**
- **IA — Identification and Authentication**

The findings were prioritized according to severity, affected scope, and remediation effort.

## Key Takeaways

This phase demonstrated the importance of:

- Enforcing strong authentication controls.
- Applying least-privilege principles.
- Managing credentials throughout their lifecycle.
- Regularly reviewing IAM permissions.
- Using multiple evidence sources when validating security findings.

### Skills Demonstrated

`AWS IAM` `MFA` `Access Control` `Least Privilege` `AWS CLI` `AWS Config` `NIST 800-53` `Security Assessment`
