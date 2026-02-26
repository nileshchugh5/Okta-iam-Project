# Okta IAM Project – SSO, MFA & Group-Based Access

## Objective
To implement Identity and Access Management (IAM) using Okta with Single Sign-On (SSO), Multi-Factor Authentication (MFA), group-based access control, and REST API-based user lifecycle management.

---

## Tools & Technologies
- Okta Developer Console
- Okta REST APIs
- Postman
- OIDC (OpenID Connect)

---

## Features
- Centralized user management
- Group-based access control (HR & Finance)
- Multi-Factor Authentication (MFA)
- Single Sign-On (SSO)
- User deactivation automatically removes access
- User lifecycle automation using APIs

---

## Groups
- HR_Group
- Finance_Group

---

## Module 1: User Management APIs (Using Okta REST API)

### Implemented APIs
- Create User
- Get User
- Update User Profile
- Suspend User
- Unsuspend User
- Reset User Password

### APIs Used
GET /api/v1/users/{id}  
POST /api/v1/users  
POST /api/v1/users/{id}  
POST /api/v1/users/{id}/lifecycle/suspend  
POST /api/v1/users/{id}/lifecycle/unsuspend  
POST /api/v1/users/{id}/lifecycle/reset_password  

### Successful Outcome
- Successfully created and managed users using Okta Users API.
- Updated user attributes such as name and email.
- Controlled user access using suspend and unsuspend lifecycle APIs.
- Reset user passwords using admin reset password API.
- Verified user status using GET API responses.
- All API calls returned successful HTTP status codes (200/201).

Screenshots available in:
screenshots/basic-user-apis

---

## Module 2: Group Management

### Implementation Steps
1. Created users:
   - hr.user@test.com  
   - finance.user@test.com  

2. Created groups:
   - HR_Group  
   - Finance_Group  

3. Assigned users to groups:
   - HR user → HR_Group  
   - Finance user → Finance_Group  

### APIs Used
POST /api/v1/groups  
PUT /api/v1/groups/{groupId}/users/{userId}  
GET /api/v1/groups/{groupId}/users  

Screenshots available in:
screenshots/group-apis

---

## Module 3: Application Integration (SSO)

### Implementation Steps
4. Created OIDC Web Application:
   - Name: IAM-Demo-App  

5. Assigned groups to application:
   - HR_Group  
   - Finance_Group  

### Result
- Only users belonging to assigned groups can access the application.
- Achieved Single Sign-On using Okta OIDC integration.

Screenshots available in:
screenshots/app-apis

---

## Module 4: Multi-Factor Authentication (MFA)

### Configuration
- Enabled Okta Verify
- Enabled Email Authentication
- Enforced MFA using authentication policy

### Testing
- Verified user login with MFA challenge.
- Confirmed MFA is required during authentication.

Screenshots available in:
screenshots/mfa-apis

---

## Testing & Validation
- Verified successful login with MFA.
- Verified group-based access control.
- Tested user deactivation blocks application access.
- Validated API responses for each lifecycle operation.

---

## Outcome
Successfully implemented a complete IAM solution using Okta with:
- Secure authentication (MFA)
- Controlled authorization (Groups)
- Automated user lifecycle management (APIs)
- Centralized access control (SSO)

This project demonstrates practical knowledge of Okta IAM, REST API integration, and identity security best practices.

---

## Author
Nilesh
