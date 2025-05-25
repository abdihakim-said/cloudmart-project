# Cloud Mart – AI-Driven Multi-Cloud E-Commerce Platform with DevOps Transformation

**Cloud Mart** is a cutting-edge, AI-powered e-commerce platform designed to compete with market leaders like **Klarna** by leveraging multi-cloud capabilities and advanced DevOps practices. As a **DevOps Consultant **, I led the transformation of Cloud Mart’s legacy system into a scalable, fully automated, and intelligent platform that significantly reduces operational costs and improves customer experience.

---

<img width="1440" alt="Screenshot 2025-05-24 at 23 56 43" src="https://github.com/user-attachments/assets/8342fc35-cf75-4e2e-9fec-9d6b3611cf9f" />


##  Stack Used
<img width="764" alt="Screenshot 2025-05-21 at 20 29 33" src="https://github.com/user-attachments/assets/dc770a7e-57b4-49f9-9470-78063a6a6c4a" />


## 💼 Business Challenges

Cloud Mart faced numerous operational hurdles:

- ⚠️ High operational costs due to manual customer service workflows and inefficient backend systems  
- ⌛ Slow and risky release cycles caused by monolithic and tightly coupled legacy architecture  
- 📉 Scalability and availability issues resulting in frequent downtime during peak sales periods  
- 👩‍💼 Loss of key engineering talent unable to adapt to cloud-native and AI technologies  
- 🛠️ Fragmented tooling and siloed development processes causing inefficiencies and bottlenecks  
- 🤖 Pressure to rapidly innovate and automate workflows to keep pace with competitors like Klarna using AI-driven customer engagement  
- 🔐 Security gaps and compliance risks due to manual infrastructure management and inconsistent standards  

Cloud Mart needed a modern, cloud-native, AI-enabled platform that would accelerate deployment, scale reliably, and enhance customer and business insights.

---

## 🎯 Solution Overview

We designed and implemented a comprehensive solution combining AWS, Azure, and Google Cloud services with advanced AI and DevOps:

### Cloud Infrastructure & Automation

- 🏗️ Modular **Terraform** Infrastructure-as-Code for repeatable provisioning across AWS, Azure, and GCP environments (Dev/QA/Stage/Prod)  
- 🐳 Containerized microservices deployed on **Amazon EKS** for scalability and resilience  
- 🔁 Automated CI/CD pipelines via **GitHub Actions**, **AWS CodePipeline**, and **CodeBuild** for continuous delivery and fast rollback capability  
- ☁️ Multi-region AWS architecture ensuring high availability and failover resilience  

---

## 🏗️ Terraform Infrastructure Details

### Amazon EKS Cluster Provisioning

- Terraform scripts provision a highly available **EKS cluster** across multiple availability zones  
- Managed node groups using AWS Auto Scaling Groups to handle container workloads dynamically  
- Kubernetes namespaces and IAM roles configured for fine-grained security and isolation  
- Integration with AWS IAM for Service Accounts (IRSA) to allow pods to securely call AWS services  

### DynamoDB Provisioning

- Created scalable **Amazon DynamoDB** tables to manage e-commerce **orders**, **inventory**, and **customer sessions**  
- DynamoDB Streams enabled for triggering event-driven workflows  

### AWS Lambda Functions

- Developed event-driven **AWS Lambda functions** written in **Python** to process DynamoDB Streams, handle order workflows, send notifications, and update inventory in real-time  
- Lambda functions integrated with API Gateway for secure external access and invoked asynchronously for backend processing  
- All Lambda function code and deployment packages maintained in the repository under `/lambda` folder and deployed automatically via CI/CD pipelines  

### Containerization

- Microservices packaged as Docker containers  
- Container images pushed to **Amazon Elastic Container Registry (ECR)** using automated build pipelines  
- Kubernetes manifests and Helm charts deployed to EKS clusters via CI/CD pipelines  

### CI/CD Pipeline with AWS CodeBuild and CodePipeline

- **AWS CodeBuild** configured to build and test Docker images and Lambda packages on every commit  
- **AWS CodePipeline** orchestrates the deployment process:  
  - Source stage from GitHub or CodeCommit repository  
  - Build stage using CodeBuild for container image creation, Lambda packaging, and pushing to ECR  
  - Deploy stage with Kubernetes manifests applied to EKS cluster and Lambda functions updated via AWS CLI/SDK  
- Automated rollback on deployment failure for minimal downtime  
- Notifications configured via SNS or Slack integration  

---

## AI & Analytics Integration

- 🤖 **Amazon Bedrock** and **OpenAI** models powering generative AI chatbots for **automated customer support and personalized recommendations**, drastically reducing manual customer service overhead  
- 🔍 **Azure Language AI** performing sentiment analysis on customer feedback, enabling real-time insights for marketing and product teams  
- 📊 **Google BigQuery** integrated as a cloud data warehouse to aggregate and analyze large-scale transactional and behavioral data for business intelligence dashboards  
- 🛒 **DynamoDB** used as the fast, scalable NoSQL database backend to manage **e-commerce orders and inventory** with seamless integration to AWS Lambda workflows  
- ⚙️ Event-driven **AWS Lambda functions (Python)** orchestrating order processing, inventory updates, and real-time notification services  

---

## Security & Compliance

- 🔐 Implemented IAM role-based access control, infrastructure standardization, and automated compliance scanning  
- 🛡️ Adopted secure DevOps practices and continuous security monitoring  

---

## Agile & Collaboration

- 🤝 Cross-functional Agile Scrum process with daily standups, sprint planning, and retrospectives  
- 📈 Continuous feedback loops between development, QA, and operations teams for rapid issue resolution and iterative improvement  

---

## 🧱 Architecture Highlights

<img width="1274" alt="Screenshot 2025-05-21 at 20 27 43" src="https://github.com/user-attachments/assets/ba75a998-73bc-4d0e-9ccc-1c9d40440e62" />

- **Multi-cloud integration:** AWS for core compute and AI services, Azure for advanced NLP and sentiment analysis, Google Cloud for analytics  
- **Microservices:** Deployed on Amazon EKS with automated scaling and fault isolation  
- **AI-driven customer engagement:** Chatbots and recommendation engines powered by Amazon Bedrock and OpenAI  
- **Serverless event processing:** Lambda functions handle order workflows and notifications  
- **Data pipeline:** Real-time data flows into BigQuery for business insights dashboards  

---

## 📂 Repository Structure

