# Wordpress
Install Wordpress on EC2 Instance

# WordPress on AWS EC2

A guide and automation script for deploying a high-availability WordPress site on an Amazon Web Services (AWS) EC2 instance.

## Prerequisites

- An active [AWS account](https://aws.amazon.com/)
- A registered domain name
- An SSH client (e.g., OpenSSH, PuTTY)
- Basic familiarity with the Linux command line and AWS EC2 dashboard

## Quick Start Deployment

### 1. Launch an EC2 Instance
1. Navigate to the **EC2 Dashboard** in the AWS Console.
2. Click **"Launch Instance"**.
3. **Name** your instance (e.g., `wordpress-server`).
4. **Choose an AMI:** Select **Ubuntu Server 22.04 LTS** (or the latest stable version).
5. **Choose an Instance Type:** For testing, use `t2.micro` (eligible for the Free Tier).
6. **Create or select a key pair** to securely connect via SSH. Download the `.pem` file.
7. **Network Settings:**
   - Ensure **"Allow SSH traffic from"** is set to `My IP`.
   - Click **"Allow HTTP traffic from the internet"** and **"Allow HTTPS traffic from the internet"**.
8. **Launch** the instance.

### 2. Connect to Your Instance
Use SSH to connect to your instance using its Public DNS name or IP address.

```bash
ssh -i /path/to/your-key.pem ubuntu@your-instance-public-ip

