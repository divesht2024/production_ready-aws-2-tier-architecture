# 🚀 Production-Ready AWS 2-Tier Architecture on AWS

This project demonstrates a **production-style 2-tier web application architecture** built on AWS using core cloud services. It is designed with **high availability, scalability, security, and monitoring** best practices.

The application layer runs on **Amazon EC2 instances** managed by an **Auto Scaling Group**, while the database layer uses **Amazon RDS**. Incoming traffic is distributed using an **Application Load Balancer (ALB)**.

---

## ☁️ AWS Services Used

* Amazon VPC
* Public & Private Subnets
* Internet Gateway
* NAT Gateway
* Route Tables
* Amazon EC2
* Launch Template
* Auto Scaling Group
* Application Load Balancer (ALB)
* Target Group
* Amazon RDS
* IAM Roles
* AWS Systems Manager (SSM)
* Amazon CloudWatch
* Security Groups

---

## 🎯 Key Features

* Multi-AZ highly available architecture
* Public ALB with private application servers
* Auto Scaling based on CPU utilization
* Secure RDS database in private subnet
* IAM role-based access (no hardcoded credentials)
* CloudWatch monitoring and alarms
* SSM Session Manager access without SSH
* Scalable and production-ready network design

---

## 🌐 Application Flow

```text
User Request
   ↓
Application Load Balancer
   ↓
EC2 Instances (Auto Scaling Group)
   ↓
Amazon RDS Database
```

---

## 🔐 Security Implementation

* Application servers deployed in **private subnets**
* Database is **not publicly accessible**
* Security groups restrict inbound traffic
* IAM Roles used instead of access keys
* Session Manager used for secure administration

---

## 📈 Auto Scaling Configuration

| Setting           | Value           |
| ----------------- | --------------- |
| Minimum Instances | 2               |
| Desired Instances | 2               |
| Maximum Instances | 4               |
| Scaling Metric    | CPU Utilization |
| Target Value      | 70%             |

---

## 🗄️ Database Layer

* Amazon RDS (MySQL/PostgreSQL)
* Private subnet deployment
* Secure connectivity from EC2 instances
* Backup and high availability ready

---

## 📊 Monitoring & Alerts

Configured using Amazon CloudWatch:

* EC2 CPU Utilization
* ALB Request Count
* Healthy/Unhealthy Targets
* RDS CPU / Connections
* Monitoring Dashboard

---

## 🧠 Skills Demonstrated

* AWS Cloud Architecture
* VPC Networking
* Load Balancing
* Auto Scaling
* High Availability Design
* Cloud Security
* Linux Administration
* Database Deployment
* Monitoring & Alerting

---

## 🚀 Deployment Steps (High Level)

1. Created VPC with public/private subnets
2. Configured Internet Gateway and NAT Gateway
3. Launched EC2 instances using Launch Template
4. Created Auto Scaling Group across two AZs
5. Configured ALB and Target Group
6. Created RDS instance in private subnet
7. Connected EC2 to RDS securely
8. Enabled CloudWatch monitoring and alarms

---

## 💼 Real-World Use Cases

* E-commerce websites
* SaaS platforms
* Startup production infrastructure
* Internal business portals
* Scalable web applications

---

## 🔮 Future Improvements

* Custom domain with Route53
* HTTPS using ACM SSL certificate
* Terraform Infrastructure as Code
* CI/CD with GitHub Actions / Jenkins
* AWS WAF integration
* Redis caching layer
* Containerization using ECS / Kubernetes

---

## 👨‍💻 Author

**Divesh Tayade**
AWS Engineer | Cloud Engineer | Junior DevOps Engineer

If you found this project useful, consider giving it a ⭐ on GitHub.
