
# GitOps CI/CD Pipeline: GitHub Actions & ArgoCD

## 📋 Overview
This repository demonstrates a modern **GitOps** workflow using **Kubernetes**, **GitHub Actions** for CI, and **ArgoCD** for CD. The project focuses on automating the deployment lifecycle of a multi-tier Java web application within a containerized environment.

## 🚀 Key Features
- **CI/CD Integration**: Automated image builds and pushes via GitHub Actions.
- **GitOps Methodology**: Declarative infrastructure management using ArgoCD.
- **Containerization**: Standardized Docker images for application components.
- **Scalability**: Managed deployment on a local Kubernetes cluster (Minikube).

## 🛠 Tech Stack
- **Orchestration**: Kubernetes (Minikube)
- **CI/CD**: GitHub Actions
- **Continuous Deployment**: ArgoCD
- **Containerization**: Docker
- **OS**: Linux Mint

## 🏗 Architecture
1. **Developer** pushes code to the `main` branch.
2. **GitHub Actions** triggers:
   - Build Docker Image.
   - Push to Container Registry.
   - Update Deployment Manifests in the repository.
3. **ArgoCD** detects the change in the repository and synchronizes the cluster state.

## 📂 Project Structure
```text
.
├── .github/workflows/   # CI/CD Pipeline configurations
├── kubernetes/          # K8s manifests (Deployments, Services)
├── src/                 # Application source code
└── Dockerfile           # Multi-stage Docker build
