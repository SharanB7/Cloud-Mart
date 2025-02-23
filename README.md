# CloudMart - AI-Powered Multi-Cloud Web Application

## Overview
CloudMart is a cloud-based e-commerce web application designed to leverage AI-powered assistants for enhanced customer experience. This project integrates AWS, Google Cloud, and Azure services for scalability, reliability, and AI-driven automation. The backend is deployed using Kubernetes, while a CI/CD pipeline ensures seamless development and deployment processes.

## Architecture & Flow
### 1. Infrastructure Setup:
- Provisioned AWS resources using Terraform, including S3, EC2, IAM Roles, and DynamoDB tables.
- Configured IAM roles and policies to provide necessary permissions.

### 2. Containerization & Deployment:
- Dockerized the frontend (React) and backend (Node.js, Express) applications.
- Pushed Docker images to AWS Elastic Container Registry (ECR).
- Deployed applications using AWS Elastic Kubernetes Service (EKS).
- Kubernetes manifests (YAML) were created for managing deployments and services.

### 3. CI/CD Pipeline:
- GitHub repository maintained for version control.
- AWS CodePipeline used to automate build, test, and deployment.
- AWS CodeBuild configured to build Docker images and push them to ECR.
- AWS CodeDeploy used to roll out application updates to Kubernetes.

### 4. AI Assistants Integration:
- Amazon Bedrock used for AI-powered product recommendations.
- OpenAI GPT-4 integrated as a customer support assistant.
- Azure Text Analytics implemented for sentiment analysis of customer reviews.

### 5. Database & Data Processing:
- AWS DynamoDB used to store product, order, and customer information.
- Google Cloud BigQuery utilized for analytics and order insights.
- AWS Lambda function implemented to transfer data from DynamoDB to BigQuery in real time.

## Tools & Technologies Used
- Cloud Platforms: AWS, Google Cloud, Azure
- Infrastructure as Code (IaC): Terraform
- Containerization: Docker
- Orchestration: Kubernetes (EKS)
- CI/CD: GitHub, AWS CodePipeline, CodeBuild, CodeDeploy
- Database: AWS DynamoDB, Google BigQuery
- AI & NLP: Amazon Bedrock (Claude 3), OpenAI GPT-4, Azure Text Analytics
- Backend: Node.js, Express
- Frontend: React, Vite
- Security & IAM: AWS IAM Roles & Policies