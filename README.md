# Okta IAM Project – SSO, MFA & Group Based Access

## Objective
To implement Identity and Access Management (IAM) using Okta with Single Sign-On (SSO), Multi-Factor Authentication (MFA), and group-based access control.

## Features
- Centralized user management
- Group-based access (HR, Finance)
- Multi-Factor Authentication (MFA)
- Single Sign-On (SSO)
- User deactivation removes access automatically

## Tools Used
- Okta Developer Console

## Groups
- HR_Group
- Finance_Group

## Implementation Steps

### 1. User Creation
- Created users:
  - hr.user@test.com
  - finance.user@test.com

### 2. Group Creation
- Created groups:
  - HR_Group
  - Finance_Group

### 3. User to Group Assignment
- HR user assigned to HR_Group
- Finance user assigned to Finance_Group

### 4. Application Creation
- Created OIDC Web Application:
  - Name: IAM-Demo-App

### 5. Group to Application Assignment
- Assigned HR_Group and Finance_Group to IAM-Demo-App

### 6. MFA Configuration
- Enabled Okta Verify and Email Authentication
- Enforced MFA using authentication policy

### 7. Testing
- Verified user login with MFA
- Verified only assigned groups can access app
- Tested user deactivation blocks access

## Outcome
Successfully implemented IAM using Okta with secure authentication and controlled access.

## Screenshots
Refer to the screenshots folder for:
- User list
- Groups
- Group membership
- Application configuration
- MFA policy
- Successful login
