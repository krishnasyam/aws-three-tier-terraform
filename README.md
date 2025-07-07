[10:47 am, 7/7/2025] +91 96067 71989: 🚀 OnFinance AI – Full Stack App Deployment on AWS EKS with Terraform
This project implements a sample full-stack application deployed on AWS EKS using Terraform, with a strong focus on high availability, logging, monitoring, and security best practices. It is designed as part of the Implementation Engineer Assignment for OnFinance AI.
[10:47 am, 7/7/2025] +91 96067 71989: 📌 Project Goals
✅ High-Level Architecture Design – Secure, scalable, multi-AZ deployment on AWS

✅ Infrastructure as Code (IaC) – Modular Terraform templates for complete AWS provisioning

✅ Kubernetes Deployment – EKS-based deployment of backend and frontend applications

✅ Logging & Monitoring – Centralized logging (CloudWatch), alerts (SNS), and metrics (HPA)

✅ CI/CD Integration (Bonus) – GitHub Actions pipeline + AWS ECR for Docker image management
[10:52 am, 7/7/2025] +91 96067 71989: | Stage     | Description                                | Status         | Completion |
| --------- | ------------------------------------------ | -------------- | ---------- |
| *1*     | High-Level Architecture Design             | ✅ Completed    | 100%       |
| *2*     | Terraform IaC – Networking + EKS + RDS     | ✅ Completed    | 100%       |
| *3*     | Kubernetes Deployment (Backend + Frontend) | ✅ Completed    | 100%       |
| *4*     | Centralized Logging + Monitoring + Alerts  | ✅ Completed    | 100%       |
| *5*     | External API Integration via Lambda (ETL)  | ⚙️ In Progress | 40%        |
| *Bonus* | CI/CD Pipeline with GitHub Actions + ECR   | ✅ Completed    | 100%       |
[10:53 am, 7/7/2025] +91 96067 71989: AWS-3-Tier-_with_Terraform/
├── terraform/
│   ├── vpc/                # VPC, subnets, route tables, IGW, NAT
│   ├── eks/                # EKS cluster, node groups
│   ├── rds/                # RDS database config
│   └── iam/                # IAM roles & policies
├── k8s/
│   ├── backend/            # Backend API Kubernetes manifests
│   ├── frontend/           # Frontend web app manifests
│   └── monitoring/         # Fluent Bit, CloudWatch agent, HPA config
├── lambda/                 # Data ingestion via API (ETL)
├── cicd/                   # GitHub Actions workflows
├── outputs/                # Screenshots, logs, sample output
└── README.md
[10:53 am, 7/7/2025] +91 96067 71989: 🔧 Prerequisites
AWS CLI configured (aws configure)

Terraform >= v1.3 installed

kubectl installed and configured

Docker installed

GitHub account with repository access

IAM user with permissions to create AWS resources
[10:55 am, 7/7/2025] +91 96067 71989: 🚀 Setup & Deployment Instructions
🏗️ Step 1: Clone Repository
bash
Copy
Edit
git clone https://github.com/ramankrishnan/AWS-3-Tier-_with_Terraform.git
cd AWS-3-Tier-_with_Terraform/
