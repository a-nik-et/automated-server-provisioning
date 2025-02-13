# Automated Server Provisioning with Terraform & Ansible

## Introduction
This project automates the provisioning and configuration of an AWS EC2 instance using **Terraform** and **Ansible**. It also integrates **Amazon CloudWatch** for monitoring system performance.

## Features
- 🚀 **Automated Infrastructure Deployment** with Terraform
- 🛠️ **Configuration Management** using Ansible
- 📊 **AWS CloudWatch Integration** for Monitoring
- 🌐 **LAMP/LEMP Stack Setup** (Optional)
- ⚡ **Scalable & Reproducible** Infrastructure

## Tech Stack
- **Terraform** - Infrastructure as Code (IaC)
- **AWS EC2** - Virtual servers in the cloud
- **Ansible** - Configuration management
- **Amazon CloudWatch** - Monitoring & Logging
- **Linux (Ubuntu)** - Operating system

## Setup & Installation

### Prerequisites
- AWS Account
- Terraform installed (`terraform -v` to check)
- Ansible installed (`ansible --version` to check)
- AWS CLI configured (`aws configure`)

### Steps to Deploy
1. **Clone the repository**
   ```sh
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```
2. **Initialize Terraform**
   ```sh
   terraform init
   ```
3. **Create and Apply the Terraform Plan**
   ```sh
   terraform apply -auto-approve
   ```
4. **Run Ansible Playbook for Configuration**
   ```sh
   ansible-playbook -i inventory.ini playbook.yml
   ```

## AWS CloudWatch Monitoring Setup
- The **Amazon CloudWatch Agent** is installed and configured to collect **CPU, memory, disk, and network metrics**.
- The config is stored at `/opt/aws/amazon-cloudwatch-agent/bin/config.json`.
- Logs can be checked using:
  ```sh
  sudo tail -f /opt/aws/amazon-cloudwatch-agent/logs/amazon-cloudwatch-agent.log
  ```

## Cleanup (To Avoid AWS Charges)
- Destroy all resources created by Terraform:
  ```sh
  terraform destroy -auto-approve
  ```
- Verify that no EC2 instances, S3 buckets, or other AWS services remain active.

## Contributing
Feel free to fork this repository and make improvements! Contributions are welcome.

## License
This project is open-source.

## My Cloud Journey 🌩️
> "Every great cloud architect was once a beginner who never stopped learning. Keep building! 🚀"

 📢 Follow my journey on [LinkedIn](https://www.linkedin.com/in/aniket1308/) & Star ⭐ this repo if you found it useful!

