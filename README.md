# ALTSCHOOL-SECOND-SEMESTER-EXAMS
The future of AI powered Logistics
 AltSchool Cloud Engineering Project – Tinyuka 2024

## Project Title
*The Future of AI-Powered Logistics*

## About
This is a dynamic prototype landing page hosted on an Ubuntu Linux EC2 instance. It showcases my cloud engineering skills and project deployment techniques.

## Technologies Used
- AWS EC2
- Ubuntu 22.04 LTS
- Nginx Web Server
- Tailwind CSS
- Certbot (Let’s Encrypt SSL)

## Deployment Steps!
Provisioning the Server (AWS EC2)
Cloud Provider: Amazon Web Services (AWS)
Service Used: EC2 (Elastic Compute Cloud)
Operating System: Ubuntu Server 22.04 LTS (64-bit)
Instance Type: t2.micro (Free Tier eligible)
Storage: 20GB General Purpose SSD (gp2)

## Security Group Rules:

Port 22 (SSH) → Open to My IP or 0.0.0.0/0
Port 80 (HTTP) → Open to 0.0.0.0/0
Port 443 (HTTPS) → Open to 0.0.0.0/
ICMP all         → Open to 0.0.0.0/

1. Launched EC2 Ubuntu Instance.
   This was done in the AWS console page using ubuntu server 22.04 LTS ,afterwhich I connected a termius terminal to the AWS to create an AWS host on my local machine.
2. Installed Nginx.
   The main commands used to acheive this  are:
   sudo apt update && sudo apt install nginx -y
   sudo systemctl enable nginx
   sudo systemctl start nginx
   
3. Built custom HTML landing page
   
4. Secured server with UFW and SSL.
   Secure the Site with SSL (Let’s Encrypt via Certbot)
   Installed Snap as it was  not already installed:
     sudo apt install snapd -y
     sudo snap install core
     sudo snap refresh core
   Installed Certbot:
     sudo snap install --classic certbot
     sudo ln -s /snap/bin/certbot /usr/bin/certbot
  Ran Certbot with Nginx:
     sudo certbot --nginx -d naomionwuka.space -d www.naomionwuka.space
     Entered a valid email
     Agreed to the terms
    Choose to redirect HTTP to HTTPS
5. Hosted and accessed via public IP.
    purchased a Domain Name to EC2 on namecheap
    Domain Name: naomionwuka.space
    Registrar: Namecheap
    DNS Configuration:
    Type	Host	Value	TTL
     A	@	54.195.130.255	Auto
     A	www	54.195.130.255	Auto


## Hosted Page
https://naomionwuka.space 

![ex](https://github.com/user-attachments/assets/a14f44db-0001-410d-8d18-6991657f1b26)



## Author
Naomi Onwuka – Lead Cloud Engineer
