# DevSecOps End-to-End Implementation

## Overview
This repository demonstrates a complete end-to-end DevSecOps implementation covering infrastructure provisioning, configuration management, containerization, orchestration, and CI/CD automation using real-world microservices (RoboShop – Catalogue service).

## Tech Stack
- AWS (EC2, VPC, EKS, ECR, IAM)
- Terraform
- Ansible
- Docker
- Kubernetes
- Jenkins
- Helm
- Bash Scripting

---

## Architecture Flow
1. Infrastructure Provisioning using Terraform  
2. Configuration Management using Ansible  
3. Application Containerization using Docker  
4. Orchestration using Kubernetes (EKS)  
5. CI/CD Pipeline using Jenkins  
6. Image Storage using Amazon ECR  
7. Deployment using GitOps/CI-CD trigger  

---

## Implementation Details

### Terraform – Infrastructure Provisioning
- Designed and provisioned complete AWS infrastructure including VPC, subnets, route tables, IGW, NAT, and EC2 instances  
- Developed reusable Terraform modules for EC2 and VPC  
- Used variables, tfvars, loops (count, for_each), conditionals, functions, and dynamic blocks  
- Implemented remote-exec and local-exec provisioners for bootstrapping  
- Managed multiple environments using workspaces  
- Configured remote state management and state security  

---

### Ansible – Configuration Management
- Automated configuration of application components using Ansible playbooks  
- Converted RoboShop setup into reusable Ansible roles  
- Used variables, facts, loops, conditions, and tags for modular automation  
- Implemented dynamic inventory for EC2 instances  
- Integrated Ansible with Terraform for post-provisioning automation  

---

### Docker – Containerization
- Built Docker images for RoboShop microservices using optimized Dockerfiles  
- Used multi-stage builds and minimal base images for efficiency  
- Implemented Docker networking and volume management  
- Containerized all services including Catalogue, User, Cart, Payment, and Frontend  

---

### Kubernetes – Orchestration (EKS)
- Deployed microservices using Pods, Deployments, ReplicaSets, and Services  
- Implemented StatefulSets with persistent storage using EBS and EFS  
- Configured static and dynamic provisioning using PV, PVC, and Storage Classes  
- Used Headless Services for Stateful applications  
- Implemented Horizontal Pod Autoscaling (HPA)  
- Applied advanced scheduling:
  - Taints & Tolerations  
  - Node Affinity & Anti-Affinity  
  - Pod Affinity & Anti-Affinity  
- Managed namespaces, ConfigMaps, and Secrets  
- Exposed services using ClusterIP, NodePort, LoadBalancer, and Ingress Controller  
- Packaged applications using Helm charts  

---

### Jenkins – CI/CD & DevSecOps
- Built Freestyle and Pipeline-based CI/CD jobs  
- Designed CI pipeline for Catalogue microservice:
  - Code scan before build  
  - Docker image build  
  - Push to Amazon ECR  
- Implemented CD pipeline:
  - Parameterized builds for controlled deployment  
  - Triggered downstream pipelines  
  - Deployed application to Kubernetes cluster  
- Integrated infrastructure creation into pipelines  
- Implemented security:
  - ECR image scanning  
  - Quality gates  
  - DAST testing using Veracode  
  - Vulnerability detection and remediation  

---

## End-to-End Flow
1. Infrastructure provisioned using Terraform  
2. EC2 instances configured using Ansible  
3. Application containerized using Docker  
4. Images built and pushed to ECR via Jenkins CI  
5. Deployment triggered via Jenkins CD pipeline  
6. Application deployed to Kubernetes (EKS)  
7. Scaling, networking, and storage managed via Kubernetes  

---

## Key Outcomes
- Built complete DevSecOps pipeline from scratch  
- Automated infrastructure provisioning and application deployment  
- Reduced manual deployment effort using CI/CD automation  
- Implemented scalable and highly available microservices architecture  
- Integrated security practices into deployment pipeline  

---

## Use Case
Deployed RoboShop Catalogue microservice using a complete DevSecOps workflow:
Code → Jenkins CI → Docker → ECR → Jenkins CD → Kubernetes (EKS)

---

## Screenshots (Add these for maximum impact)
- Jenkins pipeline execution  
- Docker image build logs  
- ECR repository images  
- Kubernetes pods and services (`kubectl get pods`)  
- Terraform apply output  
