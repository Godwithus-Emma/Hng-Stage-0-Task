# Project Overview

This project is the HNG DevOps Stage 0 task, Where I was tasked with setting up and configuring NGINX on a fresh Ubuntu server hosted on AWS.

# Prerequisites

- AWS ACCOUNT
- EC2 INSTANCE RUNNING UBUNTU
- KEY PAIR
- WEB BROWSER

# STEP 1: Setting Up The AWS Account

The first step was to launch an Ubuntu server on AWS. I navigated to the AWS Management Console, selected an Ubuntu 22.04 LTS AMI, and configured a t2.micro instance to stay within the free tier. I ensured the security group allowed SSH access (port 22) from my IP and HTTP traffic (port 80) from anywhere. After launching the instance, I connected to it using EC2 Instance Connect

# STEP 2: Installing Nginx

Once connected to the server, I updated the package list and installed NGINX using the following commands:
```
sudo apt update
sudo apt install nginx -y
```

I verified the installation by checking the status of the NGINX service:
```
sudo systemctl status nginx
```

# STEP 3: Configuring the Custom HTML Page

The next step was to replace the default NGINX welcome page with a custom HTML page. I edited the default HTML file located at /var/www/html/index.html and added the following content:
```
<!DOCTYPE html>
<html>
<head>
    <title>Welcome to DevOps Stage 0</title>
</head>
<body>
    <h1>Welcome to DevOps Stage 0 - Emmanuel Yisa/Emmantayz</h1>
</body>
</html>
```

After saving the file, I restarted NGINX to apply the changes:
```
sudo systemctl restart nginx
```

# STEP 4: Testing the Setup

Finally, I opened my browser and navigated to the public IP of my EC2 instance. Seeing the custom message, "Welcome to DevOps Stage 0 - Emmanuel Yisa/Emmantayz," was a satisfying confirmation that the setup was successful.

# Deployed Website Link
![image](https://github.com/user-attachments/assets/96b05d06-9b13-40f4-b859-eba538aef2d6)
Link: http://13.60.85.224/

# Challenges Faced
I encountered permission errors while trying to edit the default NGINX HTML page. I resolved this by using sudo to edit the file and gained a better understanding of file ownership and permission management in Linux


# How This Task Contributes to My Learning and Professional Goals

It helped me:
- Gain hands-on experience with AWS EC2 instances.
- Understand the basics of NGINX configuration.
- Develop problem-solving skills by troubleshooting SSH and NGINX issues.


# References

•   DevOps Engineers - https://hng.tech/hire/devops-engineers
•   Cloud Engineers - https://hng.tech/hire/cloud-engineers
•	Site Reliability Engineers - https://hng.tech/hire/site-reliability-engineers
•	Platform Engineers - https://hng.tech/hire/platform-engineers
•	Infrastructure Engineers - https://hng.tech/hire/infrastructure-engineers
•	Kubernetes Specialists - https://hng.tech/hire/kubernetes-specialists
•	AWS Solutions Architects - https://hng.tech/hire/aws-solutions-architects
•	Azure DevOps Engineers - https://hng.tech/hire/azure-devops-engineers
•	Google Cloud Engineers - https://hng.tech/hire/google-cloud-engineers
•	CI/CD Pipeline Engineers - https://hng.tech/hire/ci-cd-pipeline-engineers
•	Monitoring/Observability Engineers - https://hng.tech/hire/monitoring-observability-engineers
•	Automation Engineers - https://hng.tech/hire/automation-engineers
•	Docker Specialists - https://hng.tech/hire/docker-specialists
•	Linux Developers - https://hng.tech/hire/linux-developers
•	PostgreSQL Developers - https://hng.tech/hire/postgresql-developers
