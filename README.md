## IAM (Identity and Access Management)

**Identity and Access Management (IAM)** is a framework of policies, technologies, and processes that ensures the right individuals have appropriate access to resources in an organization. It helps control **who is authenticated (identity)** and **what they are authorized to access (permissions)**.

---

### **Key Components of IAM:**

* **Authentication**: Verifying a user's identity (e.g., passwords, biometrics, MFA).
* **Authorization**: Granting access based on user roles or policies.
* **User Management**: Creating, updating, and deleting user accounts and roles.
* **Access Control**: Applying rules (like role-based access control) to limit access.
* **Audit & Compliance**: Logging access events for monitoring and security compliance.

---

### **Benefits:**

* Enhances **security** by preventing unauthorized access.
* Supports **compliance** with regulations (e.g., GDPR, HIPAA).
* Improves **efficiency** through automation of user provisioning and access.



### **AWS IAM (Identity and Access Management)**

**AWS Identity and Access Management (IAM)** is a service provided by Amazon Web Services that allows you to securely manage access to AWS services and resources.

---

### **Key Features:**

* **Users and Groups**: Create IAM users (individual accounts) and groups (collections of users) to manage permissions.
* **Roles**: Define roles with specific permissions that can be assumed by users, services, or applications.
* **Policies**: JSON-based documents that define permissions (what actions are allowed or denied on which resources).
* **Granular Permissions**: Control access at a very detailed level (e.g., allow read-only access to a specific S3 bucket).
* **Temporary Credentials**: Issue short-term credentials using IAM roles (useful for applications or federated users).

---

### **Common Use Cases:**

* Granting developers read-only access to specific services.
* Allowing an EC2 instance to access an S3 bucket.
* Enabling third-party apps to access AWS without sharing long-term credentials.
* Managing user access for AWS accounts using **IAM Identity Center (formerly AWS SSO)**.

---

### **Security Best Practices:**

* Use **least privilege** principle (grant only necessary permissions).
* Enable **multi-factor authentication (MFA)**.
* Regularly **rotate credentials**.
* Monitor with **AWS CloudTrail** for IAM activity logging.

## project on IAM AWS
### 📌 Aim of the project:
**Setting up an Iam user for John who is a backend developer and Mary a data Analyst. While John requires EC2 instance, Mary requires S3 bucket service.**

1. Loging to Aws console and navigate to IAM dashboard
![captions](img/1.%20IAM%20dashboard.jpg)

## Navigate to Policy
1. click on policy
![captions](img/2.%20create%20policy.jpg)
2. Then select service. choose the service you want like EC2, S3 etc.
![captions](img/3.%20select%20EC2.jpg)
3. Select all to allow all the service permission
![captions](img/4.%20permission%20of%20EC2%20services.jpg)
4. Go to Review and create, This is where you give the policy created a name
![captions](img/6.%20Reviews%20and%20create.jpg)

5. Then create policy 
![captions](img/7.%20create%20policy.jpg)

## Navigate to user group
1. on user policy
 ![captions](img/8.%20user%20group.jpg)

2. name the group
 ![captions](img/9.%20Name%20group.jpg)

 3. Attach the group to a policy you created
  ![captions](img/10.%20Attach%20permisiion%20of%20developers.jpg)
## Navigate to user
  1. On the users board
  ![captions](img/11.%20create%20a%20user.jpg)

2. Name the user then choose i want to create an IAM user![captions](img/12.%20create%20user%20name%20John.jpg)

3. select a user group that you need for your user and click creat user
![captions](img/13.%20add%20user%20to%20group.jpg)

4. You can download the .csv file which contains user login details
![captions](img/15.%20download%20user%20%20file.jpg)

## Log into the IAM user console

1. Log in into IAM user console
![captions](img/26.%20Mary%20login.jpg)

2. Choose the service that is permitted for the user(for John have EC2 instance permission)
![captions](img/20.%20Ec2%20dashboard.jpg)

3. Launch EC2 instance for John
![captions](img/21.%20creating%20Ec2%20instance%20for%20john.jpg)

4. After creating instance then you can launch ![captions](img/23.%20launch%20instance%20john.jpg)

5. Log into the instance to confirm it's running ![captions](img/25.%20successful%20login%20ec2.jpg)

6. For Mary who has access to S3 bucket can be able to work on the S3 buckets only
![captions](img/29.%20succesfully%20delete%20s3.jpg)

## Setting up MFA for user (Multi factor Authenticator)

1. click on the user
![captions](img/30.%20user%20john.jpg)

2. click console acces and enable MFA

![captions](img/32.%20enable%20mfa.jpg)

3. Name the MFA

![captions](img/33.%20John%20Mfa.jpg)

3. using Authenticator app or other suituable options for your user
![captions](img/34.%20authenticator%20app.jpg)

4. for authenticator app you will scan the code with you phone app

![captions](img/35.%20scan%20code.jpg)

5. Then get a successful response

![captions](img/36.%20successful%20mfa.jpg)

Now whenever the user wants to sign into console it will require MFA.