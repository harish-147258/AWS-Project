# AWS-Project
An end-to-end AWS cloud for hosting a small web application using a custom VPC, Linux EC2, S3, IAM roles and least privilege access, CloudWatch monitoring, SNS email alerts, an EBS snapshot backup, and AWS cost control. The design avoids higher-risk resources such as NAT Gateway, ALB, RDS, Auto Scaling, and multi-AZ production architecture.
# Portfolio of Internship Projects

**Author:** Harish Kalakonda  
**Focus:** Cloud Architecture (AWS) & Quality Assurance / Test Optimization

## AWS Cloud Internship: Free-Tier Architecture & Automated Operations

### Overview
A secure, cost-controlled, Free Tier-compliant AWS environment hosting a Student Portal web application. The design implements least privilege, automated operational alarms, cloud storage synchronization, and log analytics without incurring costs.

### Key Architecture & Implementation Details
- **Networking:** Custom VPC (`10.0.0.0/16`), public subnet (`10.0.1.0/24`), Internet Gateway, and custom route tables.
- **Compute:** EC2 Linux micro-instance running Apache/Nginx with SSH restricted to administrative IP.
- **IAM Security:** EC2 Instance Profile with least-privilege policies scoped exclusively to bucket `aws-internship-project-2026-847291`—eliminating hardcoded credentials.
- **Monitoring & Alerts:** CloudWatch alarms monitoring CPU utilization (>70%) and status checks, integrated with SNS email alerts.
- **Storage & Backup:** Automated S3 log synchronization and root EBS snapshot recovery plan.
- **Data Analytics:** Python-based log parser analyzing access logs for peak traffic, HTTP error distributions, and unique visitor IPs.
