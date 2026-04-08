# AWS EC2 Nginx Web Deployment (Single Server to Load Balanced & Auto Scaling Architecture)

This project demonstrates my hands-on learning process of deploying a static website on AWS, starting from a single EC2 instance and evolving into a load balanced and scalable architecture using Auto Scaling.

---

## Project Overview

The project began with a basic single-server setup and was later extended into a multi-instance architecture behind an Application Load Balancer.  
Finally, Auto Scaling was introduced to automatically manage instances and simulate a dynamic cloud environment.

---

## Version 1 - Single Server Setup

- Launched an EC2 instance (Ubuntu)
- Connected via SSH
- Installed and configured Nginx
- Deployed a static HTML website
- Enabled public access via Security Groups

---

## Version 2 - Load Balanced Architecture

- Created multiple EC2 instances
- Configured Nginx on each instance
- Deployed different HTML responses for testing
- Created a Target Group and registered instances
- Set up an Application Load Balancer (ALB)
- Configured HTTP listener and routing
- Enabled health checks
- Troubleshot networking and availability zone issues

---

## Version 3 - Auto Scaling Integration

- Created a Launch Template based on EC2 configuration
- Configured an Auto Scaling Group (ASG)
- Connected ASG to the existing Target Group
- Defined minimum, desired, and maximum instance capacity
- Observed automatic instance creation and replacement
- Debugged unhealthy instance behavior and scaling issues

---

## Architecture

Components used:

- EC2 instances running Ubuntu
- Nginx web server
- Application Load Balancer (ALB)
- Target Group with health checks
- Auto Scaling Group (ASG)
- Security Groups for network control

Traffic flow:

User → Load Balancer → Auto Scaling Group → EC2 Instances


## Screenshots

### Website
![Website](Screenshots/website.png)

### EC2 Instances
![EC2](Screenshots/ec2.png)

### Load Balancer
![Load Balancer](Screenshots/load-balancer.png)

## What I Learned

- Deploying and managing EC2 instances
- Connecting to Linux servers via SSH
- Installing and configuring Nginx
- Understanding Security Groups and networking
- Setting up Application Load Balancer
- Using Target Groups and health checks
- Implementing Auto Scaling Groups
- Understanding scaling behavior and instance lifecycle
- Troubleshooting real-world AWS issues

---

## Result

The final system distributes traffic across multiple EC2 instances using a Load Balancer and supports automatic scaling with Auto Scaling Group.

The architecture ensures:
- Load distribution across servers
- Automatic replacement of unhealthy instances
- Dynamic scaling based on defined capacity
- Improved availability and resilience

---

## Notes

- The application is accessed via the Load Balancer DNS
- Direct access via EC2 public IP is not required in this architecture
- The project demonstrates a simplified production-like scalable system
