# Implementing Self-Service Password Reset (SSPR) and Azure AD Identity Protection

## Overview
This project demonstrates the implementation of **Self-Service Password Reset (SSPR)** and **Azure AD Identity Protection** to enhance organizational security. It includes enabling secure password reset options, enforcing Multi-Factor Authentication (MFA) for high-risk users, and protecting against risky sign-ins using Identity Protection and Conditional Access Policies.

## Goals
1. Secure user accounts with self-service password reset capabilities.  
2. Enforce MFA for medium- and high-risk users.  
3. Block access from untrusted locations to mitigate potential threats.  
4. Integrate Identity Governance for access reviews and role-based access control (RBAC).  

---

## Environment Setup
### Test Users
- Five test users were created with varying roles to simulate different levels of access:
  - Admin
  - Standard User
  - Helpdesk User
  - HR Department
  - Finance Department

### Test MFA
- MFA was enabled for three users (Standard User, Helpdesk User, and Finance User) to simulate real-world security scenarios.

**Screenshots**:  
1. Screenshot of test users created in Azure AD.  
2. Screenshot of MFA setup for selected users.

---

## Self-Service Password Reset (SSPR) Configuration
### SSPR Setup
- Configured SSPR for all users, enabling:
  - Email recovery.
  - Mobile phone verification.
  - Security questions for password reset.

### Steps:
1. Navigate to **Azure AD** > **Password Reset** > **Properties**.  
2. Enable SSPR for all users.  
3. Configure authentication methods (email, mobile phone, security questions).  

**Screenshots**:  
1. Screenshot of SSPR configuration.  
2. Screenshot of the password reset process.

---

## Identity Protection Policies
### User Risk Policy
- Enforced MFA for users flagged with medium or high user risk.

### Sign-In Risk Policy
- Blocked access for users flagged with high-risk sign-ins.  

### Steps:
1. Navigate to **Security** > **Identity Protection**.  
2. Configure and enable **User Risk Policy** and **Sign-In Risk Policy**.  

**Screenshots**:  
1. Screenshot of User Risk Policy settings.  
2. Screenshot of Sign-In Risk Policy settings.

---

## Conditional Access Policies
### MFA for High-Risk Sign-Ins
- Created a Conditional Access Policy requiring MFA for users flagged with high-risk sign-ins.

### Block Access from Untrusted Locations
- Configured a Conditional Access Policy to block access from specific countries/regions.

### Steps:
1. Navigate to **Security** > **Conditional Access**.  
2. Create and assign policies for high-risk sign-ins and location-based access.  

**Screenshots**:  
1. Screenshot of Conditional Access Policy setup.  
2. Screenshot showing policy enforcement (e.g., blocked access).

---

## Governance Features
### Access Reviews
- Configured quarterly access reviews for SSPR users to ensure appropriate access.
- Reviewers: Assigned group owners and managers to review access eligibility.

### Entitlement Management
- Created **Access Packages** for SSPR users with role assignments:
  - Roles: Helpdesk User, Self-Service User.
  - Approval Workflow: Automated role assignment requests with IT Manager approval.

**Screenshots**:  
1. Screenshot of Access Review setup.  
2. Screenshot of Access Package configuration.

---

## Testing and Results
### Simulated Risk Events
- Triggered:
  - Multiple failed login attempts to simulate medium- and high-risk sign-ins.
  - VPN-based logins to simulate risky locations.

### Policy Enforcement
- Verified:
  - MFA was required for medium-risk users.
  - High-risk users were blocked from untrusted locations.

**Screenshots**:  
1. Screenshot of MFA prompt during a simulated risk event.  
2. Screenshot of blocked access message for high-risk users.

---

## Results
1. Reduced unauthorized access by enforcing strong authentication methods.  
2. Enhanced security with automated governance features, including Access Reviews and RBAC.  
3. Improved user experience with self-service password reset capabilities.  

---

## Documentation
For a detailed guide and configuration steps, refer to the [Full Project Documentation](docs/SSPR_and_Identity_Protection.pdf).

---

## Contact
For questions or more information, reach out to me:
- **Email**: rlass8908@gmail.com  
- **LinkedIn**: [Roman Lassiter](https://linkedin.com/in/roman-lassiter)  

---
