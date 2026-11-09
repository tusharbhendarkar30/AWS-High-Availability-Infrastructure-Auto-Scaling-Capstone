# AWS High Availability Infrastructure & Auto Scaling Capstone

## 🚀 Overview
Production-grade, multi-AZ cloud infrastructure deployed on AWS engineered for high availability, secure network isolation, automated load balancing, and self-healing auto-scaling capabilities.

## 🏗️ Architecture Design
* **Custom VPC:** Divided into public and private subnets across multiple Availability Zones.
* **Bastion Host:** Deployed in the public subnet for encrypted SSH management of internal nodes.
* **NAT Gateway:** Provides outbound internet connectivity for private EC2 instances without opening inbound public access.
* **Application Load Balancer (ALB):** Public-facing load balancer with target group health checks routing traffic to backend Apache instances.
* **Auto Scaling Group (ASG):** Launch template automation (Apache via User Data) maintaining a baseline capacity of 2 instances with automatic failover.

## 🛠️ Tech Stack
* **Cloud:** AWS (VPC, EC2, ALB, ASG, NAT Gateway, IAM, Security Groups)
* **OS & Web Server:** Ubuntu Linux, Apache2
* **Scripting:** Shell / Bash User Data automation

## ⚙️ How to Deploy & Test
1. **Network Provisioning:** Deploy custom VPC, public/private subnets, Internet Gateway, and route table associations.
2. **Compute & Security:** Launch Bastion Host in public subnet. Provision private EC2 instances with Apache.
3. **Load Balancer Setup:** Create target groups, attach private instances, configure HTTP health checks, and initialize ALB.
4. **Auto Scaling Configuration:** Define Launch Template with User Data script and attach target group to ASG.
5. **Failover Verification:** Terminate an active EC2 instance via AWS CLI/Console and observe ASG replacing the instance dynamically.

## 👤 Author
* **Tushar Bhendarkar** — [LinkedIn](https://linkedin.com/in/tusharbhendarkar) | [GitHub](https://github.com/tusharbhendarkar30)
```[cite: 1]

---

Let me know when you are ready, and I will provide the documentation package for your **second project (AWS Blue-Green Deployment)**!
