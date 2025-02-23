# AWS-Based Honeypot for Threat Intelligence

## 🚀 Project Overview
This project aims to deploy an **AWS-based honeypot** to collect, analyze, and gain insights into potential cyber threats. The honeypot will be designed to attract malicious actors and log their activity for further research and defense strategies.

## 🎯 Objectives
- Deploy a **cloud-based honeypot** on AWS using **EC2 instances**.
- Capture and analyze malicious traffic using **logging & monitoring tools**.
- Implement **Dockerized services** for easy deployment and scaling.
- Use **threat intelligence feeds** to correlate findings.
- Follow an **Agile development process (6 sprints)** with Jira for tracking.

## 🏗️ Architecture & Tech Stack
- **Cloud Provider:** AWS (EC2, S3, CloudWatch, IAM)
- **Networking:** VPC, Security Groups, Firewalls
- **Logging & Monitoring:** AWS CloudWatch, Elastic Stack (ELK)
- **Containerization:** Docker
- **Threat Intelligence:** MISP, Suricata, Snort
- **CI/CD & Automation:** GitHub Actions, Terraform (optional)

## 📅 Agile Development (6 Sprints)
We are following an **Agile Scrum approach** with **2-week sprints**:

| Sprint # | Goals |
|----------|------------------------------------------------------------|
| Sprint 1 | Set up AWS environment, deploy initial EC2 instance, configure SSH access |
| Sprint 2 | Install honeypot services (Cowrie, Dionaea, or Snort) & set up logging |
| Sprint 3 | Implement data collection & forwarding to a SIEM system |
| Sprint 4 | Automate deployment using Docker & Infrastructure as Code |
| Sprint 5 | Integrate threat intelligence feeds & develop dashboards |
| Sprint 6 | Testing, optimization, and final documentation review |

## 🚀 Getting Started
### Prerequisites
- AWS Free Tier account
- SSH access to the EC2 instance
- Docker installed on the instance

### Setup Instructions
1. **Launch an EC2 Instance:**
   ```sh
   aws ec2 run-instances --image-id ami-12345678 --instance-type t2.micro --key-name my-key --security-groups my-security-group
   ```
2. **Connect via SSH:**
   ```sh
   ssh -i my-key.pem ec2-user@your-instance-ip
   ```
3. **Clone this repository:**
   ```sh
   git clone https://github.com/your-repo/aws-honeypot.git
   ```
4. **Run the setup script (if available):**
   ```sh
   chmod +x setup.sh && ./setup.sh
   ```

## 📊 Logging & Analysis
All honeypot activity is logged and can be analyzed using **AWS CloudWatch** or exported to an **ELK stack** for visualization.

## 🤝 Contributing
- Use Jira for sprint planning & issue tracking.
- Create feature branches before committing.
- Submit pull requests for code review.

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
_This project is actively developed as part of an academic research initiative on cloud security and threat intelligence._

