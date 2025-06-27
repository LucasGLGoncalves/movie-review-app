# 🎬 Movie Review App - CI/CD DevOps Pipeline

This project demonstrates a complete CI/CD pipeline implementation for a .NET-based movie review application. The focus is on DevOps best practices, automation, and cloud-native deployment using Azure Kubernetes Service (AKS).

## 📌 Objectives

- Automate the software delivery process.
- Ensure high code quality and security.
- Enable scalable and reliable deployments on AKS.
- Demonstrate real-world DevOps tooling and workflow.

## 🧱 Tech Stack

- **Backend**: ASP.NET Core (.NET)
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Quality Tools**: SonarQube, Trivy
- **Deployment**: Kubernetes (AKS), Docker Hub
- **Other**: YAML, Helm, Azure CLI

## 🔁 CI/CD Pipeline Overview

The CI/CD workflow is triggered by code commits and follows this sequence:

### 📦 Build Stage

- Restore and build the solution using `dotnet build`

### ✅ Test & QA Stage

- Unit Tests
- Integration Tests
- Code Analysis using SonarQube

### 🔍 Image Validation

- Dockerfile Linting
- Docker Image Build
- Vulnerability Scan using Trivy

### 🚀 Delivery

- Docker Push to Docker Hub
- Staging Deployment on AKS
  - Smoke/Integration Tests
- Production Deployment (manual or automated)

## 🚢 Kubernetes Deployment

Kubernetes manifests are located in the `k8s/` directory and include:

- Deployment
- Service
- Ingress

Ensure your AKS context is set before deploying:

```bash
kubectl apply -f k8s/deployment.yaml
```

🔐 Security & Quality
SonarQube is used for static code analysis.

Trivy scans container images for vulnerabilities.

Code quality gates must pass before proceeding to deploy stages.

🛠️ Future Enhancements
Helm chart packaging

Blue/Green or Canary deployment strategy

Monitoring with Prometheus/Grafana

Secret management with Azure Key Vault

🧑‍💻 Author
This project is part of a DevOps portfolio by Lucas Gonçalves (LucasGLGoncalves). Feel free to explore the source, suggest improvements, or fork it for learning purposes.

Feel free to reach out if you’d like to collaborate or have feedback.
