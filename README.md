🚀 OnFinance AI – Full Stack App Deployment on AWS EKS with Terraform
This sample full-stack application—deployed on AWS EKS using Terraform—showcases high availability, logging, monitoring, and security best practices. It’s built as part of the Implementation Engineer Assignment for OnFinance AI.

📌 Project Goals
✅ High‑Level Architecture Design
Secure, scalable multi-AZ deployment on AWS.

✅ Infrastructure as Code (IaC)
Modular Terraform templates to provision networking, EKS, RDS, IAM, etc.

✅ Kubernetes Deployment
EKS-based deployment of both backend and frontend applications.

✅ Logging & Monitoring
Centralized logging (CloudWatch), alerts (SNS), and metrics (HPA).

⚙️ External API Integration via Lambda (ETL)
Building an external data ingestion pipeline. (In progress)

✅ CI/CD Integration (Bonus)
GitHub Actions pipeline + AWS ECR for Docker image management.

🛠️ Project Status
Stage	Description	Status	Completion
1	High-Level Architecture Design	✅ Completed	100%
2	Terraform IaC – Networking + EKS + RDS	✅ Completed	100%
3	Kubernetes Deployment (Backend + Frontend)	✅ Completed	100%
4	Centralized Logging + Monitoring + Alerts	✅ Completed	100%
5	External API Integration via Lambda (ETL)	⚙️ In Progress	40%
Bonus	CI/CD Pipeline with GitHub Actions + ECR	✅ Completed	100%

📁 Project Structure
graphql
Copy
Edit
AWS-3-Tier_with_Terraform/
├── terraform/
│   ├── vpc/        # VPC, subnets, route tables, IGW, NAT
│   ├── eks/        # EKS cluster, node groups
│   ├── rds/        # RDS database config
│   └── iam/        # IAM roles & policies
├── k8s/
│   ├── backend/    # Backend API Kubernetes manifests
│   ├── frontend/   # Frontend web app manifests
│   └── monitoring/ # Fluent Bit, CloudWatch agent, HPA config
├── lambda/         # Data ingestion via API (ETL)
├── cicd/           # GitHub Actions workflows
├── outputs/        # Screenshots, logs, sample output
└── README.md       # This file
🔧 Prerequisites
Ensure the following are installed and configured:

AWS CLI (aws configure)

Terraform v1.3+

kubectl

Docker

GitHub account with repo access

IAM user with AWS provisioning permissions

🚀 Setup & Deployment Instructions
🏗️ Step 1: Clone the Repository
bash
Copy
Edit
git clone https://github.com/ramankrishnan/AWS-3-Tier-_with_Terraform.git
cd AWS-3-Tier_with_Terraform/
🧩 Step 2: Provision Infrastructure
bash
Copy
Edit
cd terraform/vpc
terraform init && terraform apply -auto-approve

cd ../eks
terraform init && terraform apply -auto-approve

cd ../rds
terraform init && terraform apply -auto-approve

cd ../iam
terraform init && terraform apply -auto-approve
☸️ Step 3: Deploy Kubernetes Resources
bash
Copy
Edit
cd ../../k8s
kubectl apply -f backend/
kubectl apply -f frontend/
kubectl apply -f monitoring/
🧪 Step 4: Setup Observability
Verify CloudWatch logs and metrics

Check SNS alerts on threshold breaches

🔄 (Optional) Step 5: Trigger Lambda ETL
bash
Copy
Edit
cd ../../lambda
# package and deploy your Lambda function
🤖 Bonus: CI/CD Pipeline
Your GitHub Actions workflows (in cicd/) automate build, Docker push (to ECR), and apply deployments.

✅ Outputs
Screenshots, logs, and sample outputs are in the outputs/ directory to validate deployment steps.

📝 Contributing
Contributions are welcome! To contribute:

Fork the repo

Create a feature branch: git checkout -b feature/my-feature

Commit your changes: git commit -m "Add my feature"

Push the branch: git push origin feature/my-feature

Open a Pull Request

Follow standard Git workflow and code review guidelines.

📄 License
This project is released under the MIT License. See the LICENSE file for details.

🙏 Acknowledgements
OpenAI for the GPT model

AWS for cloud infrastructure

Terraform and Kubernetes communities

StackOverflow for invaluable support

