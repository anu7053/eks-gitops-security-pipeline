# EKS GitOps & Cloud Security Pipeline

Production-grade Infrastructure as Code, Kubernetes orchestration, and automated security scanning pipeline built for Amazon EKS.

## 🏗️ Architecture & Tech Stack
* **Cloud Infrastructure:** Amazon Web Services (AWS), EKS, VPC, IAM
* **Infrastructure as Code (IaC):** Terraform
* **GitOps & Orchestration:** Kubernetes, Helm / ArgoCD
* **Security & Compliance:** Trivy (Container Vulnerability Scanning), Checkov (IaC Security Scanning)
* **CI/CD Automation:** GitHub Actions with OIDC secure authentication

## 🛡️ Security Gates
1. **IaC Scanning:** Checkov scans Terraform configurations for misconfigurations and security compliance gaps prior to deployment.
2. **Container Scanning:** Trivy scans container images for critical and high vulnerabilities before pushing to the cluster.
3. **Automated Reporting:** Pipeline validation results and scan summaries are published directly to `$GITHUB_STEP_SUMMARY`.
