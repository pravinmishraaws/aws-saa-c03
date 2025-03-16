### **AWS IAM Identity Center (AWS Single Sign-On) - Key Points for AWS SAA-C03 Exam**

#### **1. Overview**
- Centralized identity and access management for AWS accounts and cloud applications.
- Supports authentication via AWS Managed Directory, external Identity Providers (IdPs) like Okta, Azure AD, and Google Workspace.
- Works with AWS Organizations for managing multi-account access.
- Provides Single Sign-On (SSO) without creating IAM users in each AWS account.

#### **2. AWS IAM Identity Center vs. AWS IAM**
| Feature | AWS IAM Identity Center | AWS IAM |
|---------|------------------------|---------|
| Best for | Centralized identity & access management | Managing permissions within a single AWS account |
| Users | Uses federated users (SSO) | Uses IAM users & roles |
| Authentication | Supports MFA, AD, SAML, OpenID | IAM credentials, IAM roles |
| Authorization | Assigns permissions via Permission Sets | Uses IAM policies & roles |
| AWS Organizations Integration | Yes | No |

#### **3. Key Components**
- **Identity Source**: AWS IAM Identity Center Directory, AWS Managed AD, or External IdPs.
- **Permission Sets**: Define user/group permissions for AWS account access.
- **Applications**: Enables SSO for AWS accounts and third-party applications.
- **Multi-Account Management**: Works with AWS Organizations for centralized access.

#### **4. Authentication Methods**
- AWS IAM Identity Center Directory (default).
- AWS Managed Active Directory (for on-prem AD integration).
- External IdPs via SAML/OpenID Connect (Okta, Azure AD, Google Workspace).
- Does not support IAM users.

#### **5. Common Exam Scenarios**
- **Providing centralized access across multiple AWS accounts** → Use AWS IAM Identity Center with AWS Organizations.
- **Federated authentication with external IdPs** → Use SAML 2.0 integration.
- **Assigning different permissions to different users in the same AWS account** → Use Permission Sets.
- **Enforcing MFA for all users** → Configure MFA settings in AWS IAM Identity Center.

#### **6. Exam Tips**
- AWS IAM Identity Center replaces AWS SSO.
- Users access AWS accounts via **federated login**, not IAM roles.
- Permission Sets control AWS account access, replacing direct IAM policies.
- Does not support cross-account IAM roles.
- Requires manual MFA configuration.
- Best suited for organizations needing centralized identity management.

