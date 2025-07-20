# Group-Role-Enumeration-in-AWS


## 1. Understanding Group & Role Enumeration
Enumerating groups and roles in AWS means systematically identifying and listing all IAM (Identity and Access Management) groups and roles that exist within your AWS account. This is important for:

Auditing and compliance.
Managing user access and permissions.
Identifying misconfigurations or excessive privileges.
Ensuring least privilege principles are followed.

## 2. Prerequisites
Before you begin, ensure the following:

You have an AWS account with IAM administrative privileges.
You have access to the AWS Management Console .
(Optional) The AWS CLI is installed and configured on your machine.

## 3. Enumerating Groups in AWS
## Step 1: List All IAM Groups
Use the following methods to list all IAM groups:


<img width="895" height="547" alt="AWS_ENUM1" src="https://github.com/user-attachments/assets/3c145870-10ac-40ac-89cc-a7c7ec2aa041" />



## Step 2: View Group Details
For each group listed, you can view additional details such as attached policies and users associated with the group.

Method 1: AWS Management Console
Select a group from the list.
Review details on the group's Summary, Permissions, and Users tabs.
Method 2: AWS CLI
To get detailed information about a group:

<img width="857" height="341" alt="AWS_ENUM2" src="https://github.com/user-attachments/assets/484679e7-0d50-4d37-b01a-28ea12beaf23" />

<img width="886" height="717" alt="AWS_ENUM3" src="https://github.com/user-attachments/assets/0ef89725-f32e-460d-9088-6f22200b8e0f" />

## 4. Enumerating Roles in AWS

## Step 1: List All IAM Roles
Use the following methods to list all IAM roles:

Method 1: AWS Management Console
Navigate to IAM > Roles.
On the Roles page, you will see a list of all roles in your account.
Method 2: AWS CLI


<img width="933" height="821" alt="AWS_ENUM4" src="https://github.com/user-attachments/assets/6c89be61-d977-4c28-ac2b-b12a44b8fcc3" />


## Step 2: View Role Details

For each role listed, you can view its permissions and trust relationships.

Method 1: AWS Management Console
Select a role from the list.
Review details on the role's Summary, Permissions, and Trust Relationships tabs.
Method 2: AWS CLI
To get detailed information about a role:



## 5. Understanding Policies Attached to Groups and Roles

Both groups and roles can have inline policies or managed policies attached. Enumerating these is critical for understanding the permissions they grant.

## Step 1: List Inline Policies
aws iam list-group-policies --group-name "GroupName"





## 6. Best Practices for Group & Role Enumeration

Regularly audit groups and roles to ensure they align with your organization's security policies.
Remove unused or unnecessary groups and roles to minimize attack surfaces.
Ensure that roles follow the principle of least privilege (PoLP).
Use AWS IAM Access Analyzer to automatically identify over-permissive permissions.

## 7. Common Scenarios

Identifying roles created by AWS services (e.g., EC2, Lambda).
Checking for cross-account roles used in shared environments.
Ensuring compliance with regulatory requirements like GDPR or HIPAA.
