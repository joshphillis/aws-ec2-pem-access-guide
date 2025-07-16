# aws-ec2-pem-access-guide

# 🔐 AWS EC2 Instance Deployment & PEM File SSH Access

## Overview  
This project demonstrates launching an EC2 instance on **AWS** using a community-provided AMI, configuring security groups for HTTP and SSH access, and securely connecting to the instance via **PEM key-based authentication**. It serves as a foundational exercise in provisioning virtual machines, establishing secure connectivity, and understanding basic AWS networking principles.

## 🛠️ Tools & Technologies
- **Amazon EC2** – Cloud-hosted virtual machine service  
- **Community AMI (`ami-06d5e0de6baf595ca`)** – Linux-based image for instance deployment  
- **Security Groups** – Inbound rules for ports 22 (SSH) and 80 (HTTP)  
- **Key Pair (.pem)** – RSA-based authentication for secure instance access  
- **AWS Console** – Instance provisioning and configuration  
- **Windows Command Line / PowerShell** – SSH command execution

## 📦 Project Workflow
1. Logged into AWS Console and selected **EC2 > Launch Instance**  
2. Chose a Community AMI and configured a **t2.micro** instance  
3. Created a new **security group** allowing TCP traffic on:
   - Port `22` for SSH
   - Port `80` for HTTP  
4. Generated an **RSA PEM key pair** and downloaded the `.pem` file  
5. Successfully launched the instance and verified status (2/2 checks passed)  
6. Connected via SSH using the command:

```bash
ssh -i "pgpcc-key1.pem" ec2-user@<Public-IP-Address>

## 🧪 Validation
- Verified shell access to Amazon Linux terminal  
- Confirmed instance details using `kubectl` and AWS Console  
- Tested public IP in browser and confirmed inbound traffic permissions  
- Ensured key fingerprint recognition and secure host listing

## ✅ Outcomes
- Gained experience launching and accessing EC2 instances securely  
- Practiced PEM-based authentication and SSH command structure  
- Configured security group rules and validated firewall behavior  
- Strengthened AWS fundamentals in networking and compute provisioning


## 👨‍💻 About the Author  
Created by **Joshua Phillis**, a transitioning cloud engineer with deep roots in logistics, strategy, and security. Passionate about building resilient, scalable cloud infrastructure and sharing lessons learned through practical demos and veteran-focused cloud coaching.

