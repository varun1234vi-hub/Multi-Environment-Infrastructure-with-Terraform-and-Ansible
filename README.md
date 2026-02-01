**🌍 DevOps Project: Multi-Environment Infrastructure with Terraform & Ansible**



**📌 Project Overview**

This project demonstrates how to build and manage a production-ready, multi-environment infrastructure using Terraform for infrastructure provisioning and Ansible for configuration management.

The setup follows DevOps best practices by automating infrastructure creation, environment separation, configuration management, and clean teardown across development (dev), staging (stg), and production (prod) environments.


**🎯 Objectives Achieved**

-Designed multi-environment infrastructure (dev, stg, prod) using Terraform modules

-Implemented Infrastructure as Code (IaC) with reusable and scalable patterns

-Used remote backend with S3 and DynamoDB for state storage and locking

-Automated server configuration using Ansible roles

-Created dynamic inventories by fetching EC2 IPs from Terraform outputs

-Installed and configured Nginx automatically on all environments

-Ensured cost optimization by destroying infrastructure after use


**🛠️ Tools & Technologies Used**

Terraform – Infrastructure provisioning

Ansible – Configuration management

AWS – EC2, S3, DynamoDB, IAM

Ansible Galaxy – Role management

Shell Scripting – Dynamic inventory automation

Linux (Ubuntu)


**🧱 Architecture Summary**

Separate environments: Dev / Staging / Production

Terraform modules used for reusability

Remote backend:

S3 → Terraform state storage

DynamoDB → State locking

Ansible role to install and manage Nginx

Dynamic inventory generation using Terraform outputs


**project Diagram**
![Project-design](https://github.com/user-attachments/assets/45059179-6be5-40ab-92d9-a4f231cc1eb0)



**🚀 Terraform Workflow**

1️⃣ Initialize Terraform
terraform init

2️⃣ Review Execution Plan
terraform plan

3️⃣ Apply Infrastructure
terraform apply


🔹 Run Ansible Playbook
ansible-playbook -i inventories/dev install_nginx_playbook.yml
ansible-playbook -i inventories/stg install_nginx_playbook.yml
ansible-playbook -i inventories/prod install_nginx_playbook.yml


✔️ Installs and configures Nginx on all servers
✔️ Deploys a custom HTML page


**🧹 Infrastructure Cleanup (Cost Saving)**
terraform destroy --auto-approve


This safely removes:

EC2 instances

S3 buckets

DynamoDB tables

⚠️ Note: This action is irreversible.


**📈 Key Learnings**

-Real-world multi-environment DevOps design

-Terraform state management & locking

-Infrastructure modularization

-Dynamic Ansible inventory automation

End-to-end IaC + configuration workflow

