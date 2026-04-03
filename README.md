# DevSecOps End-to-End Implementation

## Overview
This repository showcases hands-on implementation of a complete DevSecOps pipeline covering infrastructure provisioning, configuration management, containerization, orchestration, and CI/CD automation.

## Tech Stack
- AWS (EC2, EKS, ECR, VPC)
- Terraform
- Ansible
- Docker
- Kubernetes
- Jenkins
- Bash Scripting

## Architecture Flow
1. Infrastructure Provisioning (Terraform)
2. Configuration Management (Ansible)
3. Containerization (Docker)
4. Orchestration (Kubernetes – EKS)
5. CI/CD Pipeline (Jenkins)
6. Image Storage (Amazon ECR)

## Implementation Details

### Terraform
- Created VPC and EC2 infrastructure
- Used variables, loops, conditionals, and functions
- Implemented remote-exec and local-exec provisioners

### Ansible
- Automated server configuration using playbooks
- Deployed applications on provisioned VMs

### Docker
- Built custom Docker images using Dockerfiles
- Used core instructions: FROM, RUN, COPY, CMD, ENV

### Kubernetes
- Deployed applications using Pods, Deployments, Services
- Used StatefulSets with EBS/EFS volumes
- Implemented node affinity, pod affinity, and anti-affinity

### Jenkins CI/CD
- CI Pipeline:
  - Code scanning before build
  - Docker image build and push to ECR
- CD Pipeline:
  - Parameterized deployment trigger
  - Automated deployment to Kubernetes cluster

## Key Outcomes
- Automated end-to-end deployment pipeline
- Reduced manual intervention in deployments
- Implemented scalable and production-like architecture
