# AWS ECS CI/CD Pipeline with Terraform

A complete End-to-End DevOps project demonstrating the automated deployment of a containerized Python Flask application to **AWS ECS Fargate** (Serverless) using **Terraform** for Infrastructure as Code (IaC) and **GitHub Actions** for CI/CD.

## 🏗 Architecture & Tech Stack

* **Application:** Python Flask (Stateless Web API)
* **Containerization:** Docker
* **Infrastructure as Code:** Terraform
* **Cloud Provider:** AWS (ECR, ECS Fargate, IAM, CloudWatch, VPC)
* **CI/CD:** GitHub Actions

## 🚀 Key Features

* **Infrastructure as Code:** Fully automated provisioning of AWS resources (ECR Repository, ECS Cluster, Task Definitions, IAM Roles, Security Groups) using Terraform.
* **Containerization:** Optimized Dockerfile for Python application.
* **Automated Pipeline:** GitHub Actions workflow triggers on `git push`:
    1.  Builds the Docker image.
    2.  Pushes the image to AWS ECR.
    3.  Updates the ECS Service with zero-downtime rolling updates.
* **Serverless Compute:** Utilizes AWS Fargate to run containers without managing underlying EC2 instances.

## 🛠️ Quick Start

### 1. Prerequisites
* AWS CLI configured with appropriate permissions.
* Terraform installed.
* Docker installed.

### 2. Infrastructure Provisioning
Initialize and apply Terraform configuration to create AWS resources:
```bash
cd ecs-terraform
terraform init
terraform apply