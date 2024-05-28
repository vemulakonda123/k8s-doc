
```
Authentication: Verifies who you are. In EKS, it can be managed through IAM roles/users,
 Kubernetes service accounts, and other mechanisms like OIDC.
Authorization: Verifies what you can do. In EKS, this is managed primarily through
Kubernetes RBAC and can be augmented with IAM roles via IRSA.
```


Here IAM OIDC connect act as meditatior between EKS and AWS IAM
Here we associate OIDC to  integrate EKS with OIDC to utlize AWS IAM USERS 
And that user will have some roles and policyes..
that means EKS cluster can utlize that roles(which contains list of policies) and create resources in AWS for cluster usage (means pods 

can ultize EBS volumes )(services can create application load balancers ) and also S3 buckets 
```
This is a necessary step for integrating your EKS cluster with AWS IAM (Identity and Access Management) for Kubernetes RBAC (Role-
Based Access Control) and other authentication purposes.
```
S3 Buckets: Used for persistent object storage, backups, logging, Helm chart repositories, and application data.
EBS Volumes: Provide persistent block storage for pods, support stateful applications, and facilitate dynamic storage provisioning.
ELB Resources: Enable load balancing for both external and internal traffic, supporting high availability and scalable traffic 

management through services and Ingress controllers.

Ingress Controllers: Ingress controllers manage HTTP and HTTPS traffic to the Kubernetes services. AWS ALB Ingress Controller 

integrates ALB with EKS, enabling advanced routing features such as host-based or path-based routing, SSL termination, and Web 

Application Firewall (WAF) integration.
```
### eksctl utils associate-iam-oidc-provider
```
