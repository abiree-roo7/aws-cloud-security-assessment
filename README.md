<img width="993" height="1584" alt="Network-diagram" src="https://github.com/user-attachments/assets/48c2a828-f356-412d-bda1-70423ddfb58d" />
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

```

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
---

# Week 2 — Network & EC2 Security Assessment

## Objective

The second phase focused on the security posture of the AWS network and compute environment.

The assessment covered VPC architecture, subnet placement, Security Groups, EC2 hardening, Instance Metadata Service configuration, and encryption at rest.

## Activities Performed

During the assessment, I:

- Inventoried EC2 instances and VPC resources.
- Reviewed VPC and subnet architecture.
- Mapped EC2 instances to their associated subnets.
- Reviewed Security Group ingress and egress rules.
- Identified publicly exposed administrative services.
- Investigated database network exposure.
- Reviewed the default Security Group configuration.
- Assessed EC2 Instance Metadata Service configuration.
- Verified whether IMDSv2 was enforced.
- Reviewed EBS volume encryption.
- Collected configuration evidence using AWS CLI and AWS Config.
- Created an annotated network topology.
- Documented findings and remediation recommendations.

## Network Architecture

The assessed environment contained a VPC with public and private subnets distributed across multiple Availability Zones.

The assessment examined how Internet-facing resources, internal resources, Security Groups, and routing components interacted with one another.

The network diagram included in this repository is a **sanitized representation** of the assessed architecture.

![AWS Network Security Topology](diagrams/aws-network-security-topology.png)

## Key Security Findings

The assessment identified several network and EC2 security weaknesses, including:

| Category | Finding | Severity |
|---|---|---|
| Security Group | Public SSH exposure | Critical |
| Security Group | Public database access | Critical |
| Security Group | Public SSH/RDP exposure on a legacy jumpbox | Critical |
| Security Group | Insecure default Security Group configuration | High |
| EC2 Hardening | IMDSv1 remained permitted on a legacy instance | High |
| Encryption | EBS volume was not encrypted at rest | High |

All resource identifiers and environment-specific values have been removed or anonymized from this public portfolio.

## EC2 Hardening

One of the assessment checks focused on the EC2 Instance Metadata Service.

The review compared the `HttpTokens` configuration across instances to determine whether IMDSv2 was enforced.

The assessment identified a legacy instance where:

```text
HttpTokens = optional
