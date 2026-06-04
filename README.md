# Identity Governance Lab

## Hybrid Identity, Joiner-Mover-Leaver Automation, Microsoft Entra ID, Active Directory, VMware, and Auth0

### Project Overview

This project demonstrates the design, deployment, and administration of a complete Identity and Access Management (IAM) environment built from the ground up using VMware Workstation, Windows Server, Active Directory, Microsoft Entra ID, Microsoft Entra Connect, Auth0, and PowerShell automation.

The lab simulates a real-world enterprise identity environment by implementing Hybrid Identity, Role-Based Access Control (RBAC), Joiner-Mover-Leaver (JML) lifecycle automation, Multi-Factor Authentication (MFA), Enterprise Applications, App Registrations, and Identity Governance concepts aligned with Zero Trust principles.

---

# Environment Architecture

## Infrastructure

### VMware Workstation

* Created Windows Server 2019 Virtual Machine
* Created Windows 11 Virtual Machine
* Configured virtual networking
* Configured DNS
* Configured Active Directory Domain Services
* Promoted Windows Server to Domain Controller

### Domain Information

```text
Domain Name: corp.nicklab.local
NetBIOS Name: CORP
```

---

# Active Directory Implementation

## Organizational Units (OU)

```text
Corporate
├── Users
├── Groups
├── Servers
├── Workstations
├── Service Accounts
├── Admins
├── HR
├── Finance
├── IT
└── Security
```

## Security Groups

Implemented Role-Based Access Control (RBAC) using security groups:

* HR_Users
* Finance_Users
* IT_Users
* Security_Analysts
* Entra-Admins

## Group Policy Objects (GPO)

Configured:

* Password Policy
* Account Lockout Policy
* Security Settings
* Domain-Wide Policy Enforcement

---

# Microsoft Entra ID Integration

## Hybrid Identity

Implemented Microsoft Entra Connect synchronization between:

```text
Active Directory
        ↕
Microsoft Entra ID
```

### Features Configured

* Password Hash Synchronization (PHS)
* Hybrid Identity Administrator Role
* Microsoft Entra Connect Sync
* User Synchronization
* Enterprise Applications
* App Registrations
* Authentication Configuration
* Microsoft Graph Permissions

---

# Enterprise Application

Created:

```text
NickLab-HR-Portal
```

Configured:

* Enterprise Application
* User Assignments
* Authentication Settings
* Redirect URI Configuration

---

# App Registration

Created:

```text
NickLab Employee Portal API
```

Configured:

* OpenID Connect (OIDC)
* OAuth 2.0
* API Permissions
* Microsoft Graph Integration
* Client Secret
* Token Configuration

---

# Identity Lifecycle Management (JML)

## Joiner Automation

Developed PowerShell automation to:

* Read user data from CSV files
* Create Active Directory users
* Assign department attributes
* Assign security groups
* Generate audit logs

### Example

```text
Michael Brown
Sarah Johnson
Barbara Taylor
```

---

## Mover Automation

Automated employee role changes.

### Scenario

```text
Michael Brown
HR → Finance
```

Automation performed:

* Department change
* Title change
* Removal of previous access
* Assignment of new access
* Group membership updates
* Audit logging

---

## Leaver Automation

Automated employee offboarding.

### Actions Performed

* Disable user account
* Remove group memberships
* Revoke access
* Generate termination logs

### Security Benefit

Prevents orphaned accounts and reduces unauthorized access risks.

---

# Auth0 Identity Platform

Configured Auth0 as a cloud identity provider.

## Users Imported

* Sarah Johnson
* Michael Brown
* Barbara Taylor

## Roles Created

* Admin
* Employees
* Finance
* HR
* IT Admin
* Manager
* Security

## RBAC Implementation

Assigned roles based on job function and business requirements.

Examples:

```text
Sarah Johnson → HR
Michael Brown → Finance
Barbara Taylor → Security
```

---

# Security Concepts Demonstrated

## Role-Based Access Control (RBAC)

Implemented role-based permissions through Active Directory groups and Auth0 roles.

## Least Privilege

Users receive only the permissions required for their assigned role.

## Separation of Duties

Separated access between:

* HR
* Finance
* Security
* IT

## Identity Governance

Implemented:

* Joiner Processes
* Mover Processes
* Leaver Processes
* Access Management
* User Provisioning
* User Deprovisioning

## Zero Trust Principles

Applied:

* Verify Explicitly
* Least Privilege Access
* Assume Breach

---

# Skills Demonstrated

### Identity & Access Management

* Identity Governance
* Identity Administration
* User Lifecycle Management
* Joiner-Mover-Leaver (JML)
* Access Provisioning
* Access Deprovisioning
* Role-Based Access Control (RBAC)

### Microsoft Technologies

* Active Directory
* Group Policy
* Microsoft Entra ID
* Microsoft Entra Connect
* Microsoft Graph
* Enterprise Applications
* App Registrations

### Authentication & Authorization

* OAuth 2.0
* OpenID Connect (OIDC)
* Multi-Factor Authentication (MFA)
* Authentication
* Authorization

### Automation

* PowerShell
* CSV-Based Provisioning
* Lifecycle Automation
* Administrative Scripting

### Infrastructure

* VMware Workstation
* Windows Server 2019
* Windows 11
* DNS
* Active Directory Domain Services

### Cloud Identity

* Auth0
* RBAC
* Identity Federation
* Workforce Identity Management

---

# Key Takeaways

This project demonstrates the ability to design, deploy, secure, and automate a complete hybrid identity environment using Active Directory, Microsoft Entra ID, Auth0, VMware, and PowerShell.

The lab provides hands-on experience with identity governance, lifecycle management, access control, authentication, authorization, automation, and hybrid identity integration commonly found in enterprise IAM environments.

---

# Interview Questions

## What is the difference between Authentication and Authorization?

Authentication verifies who a user is.

Authorization determines what resources the authenticated user can access.

---

## What is RBAC?

Role-Based Access Control assigns permissions based on job function rather than assigning permissions directly to individual users.

---

## What is the purpose of a Joiner-Mover-Leaver process?

The JML process automates onboarding, role changes, and offboarding while ensuring appropriate access throughout the user lifecycle.

---

## What is the difference between a Client ID and Client Secret?

The Client ID identifies an application.

The Client Secret authenticates the application when requesting tokens from an identity provider.

---

## What is Hybrid Identity?

Hybrid Identity integrates on-premises Active Directory with Microsoft Entra ID to provide centralized identity management across environments.

---

## What is Microsoft Entra Connect?

Microsoft Entra Connect synchronizes users, groups, and identity information between Active Directory and Microsoft Entra ID.

---

## What is OAuth 2.0?

OAuth 2.0 is an authorization framework that allows applications to obtain limited access to protected resources on behalf of users.

---

## What is OpenID Connect?

OpenID Connect is an authentication layer built on top of OAuth 2.0 that verifies user identities and provides profile information.
