# terraform-docker-project
Provision a Docker container using Terraform (IaC)
# 🐳 Terraform Docker Project

This repository demonstrates deploying a **Docker Nginx container** using **Terraform** on Windows. 

---

## 📌 Task Objective

Use Terraform to automate the deployment of an Nginx Docker container:

- Initialize Terraform.  
- Create a Docker image for Nginx.  
- Launch a container from that image.  
- Expose the container on port 8080.  
- Test the container using `docker ps`.  
- Destroy the infrastructure after testing.  

✅ All requirements are satisfied.

---

## 🛠️ Tools Used

| Tool | Version |
|------|---------|
| Terraform | v1.13.4 |
| Docker | 28.5.1 |
| Nginx | latest |

---

## ⚡ Steps

1. **Clone the repository**  

git clone https://github.com/rakshita-madival/terraform-docker-project.git
cd terraform-docker-project
Initialize Terraform


terraform init
Terraform downloaded the required Docker provider.

Check Terraform plan


terraform plan
Shows resources to be created (Docker image + container).

Apply Terraform configuration


terraform apply
Type yes when prompted.

Terraform created:

Docker image: nginx:latest

Docker container: terraform-nginx on port 8080

Verify running container


docker ps
Output shows terraform-nginx is running and mapped to port 8080.

Destroy infrastructure after testing


terraform destroy
Type yes to remove all resources.

Ensures clean environment.

📁 Project Structure
csharp

terraform-docker-project/
├─ main.tf                 # Terraform configuration
├─ terraform.tfstate       # Terraform state file
├─ terraform.tfstate.backup
├─ .terraform/             # Terraform internal files
├─ .terraform.lock.hcl     # Provider lock file
└─ README.md
✅ Outcome
Terraform successfully created the Nginx Docker image.

A Docker container was deployed and exposed on port 8080.

Infrastructure was destroyed successfully after testing.

🎯 Key Learnings
Terraform workflow: init → plan → apply → destroy.

Managing Docker containers using Terraform.

Understanding state files and provider configuration.

