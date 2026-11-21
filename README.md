# Velvet Matte Lipstick – AWS Cloud Deployment Project

## Project Overview

This project demonstrates the deployment of a static makeup product webpage using **HTML and CSS** on Amazon Web Services (AWS).

The webpage showcases the **Velvet Matte Lipstick by Maison Petal**, featuring a clean and elegant product presentation. The website is hosted on an Amazon EC2 instance using the Apache web server.

The project also implements AWS monitoring through Amazon CloudWatch and secure AWS resource access using an IAM role.

## AWS Services Used

This project uses exactly three AWS services:

| AWS Service | Purpose |
|---|---|
| **Amazon EC2** | Hosts the static website using Apache web server. |
| **Amazon CloudWatch** | Monitors CPU utilization and provides alarms and dashboards. |

##  Project Architecture

1. HTML and CSS are used to create the makeup product webpage.
2. The `index.html` file is deployed to an Amazon EC2 instance.
3. Apache web server serves the webpage over HTTP.
4. An IAM role named `EC2-CloudWatch-Role` provides secure permissions to the EC2 instance.
5. Amazon CloudWatch monitors CPU utilization.
6. A CloudWatch alarm triggers when CPU utilization exceeds 70%.
7. A CloudWatch dashboard displays CPU monitoring metrics.

## AWS Configuration

### Amazon EC2

- **Instance Name:** `makeup-web-server`
- **Region:** Mumbai (`ap-south-1`)
- **Web Server:** Apache HTTP Server
- **Operating System:** Linux
- **Website URL:** http://13.201.75.64

**Security Group Rules:**

| Type | Port | Purpose |
|---|---:|---|
| HTTP | 80 | Allows users to access the website. |
| SSH | 22 | Allows secure remote server administration. |



### Amazon CloudWatch

Configured CloudWatch monitoring with the following resources:

**CloudWatch Alarm**
- Alarm Name: `makeup-web-high-cpu`
- Metric: CPU Utilization
- Threshold: Greater than 70%
- Purpose: Monitors high CPU utilization on the EC2 instance.

**CloudWatch Dashboard**
- Dashboard Name: `makeup-web-dashboard`
- Displays EC2 CPU utilization.
- Helps visualize server performance.
- Provides an overview of server monitoring metrics.

## Deployment Steps

1. Created a static makeup product webpage using HTML and CSS.
2. Launched an EC2 instance in the Mumbai region.
3. Configured the security group to allow HTTP (80) and SSH (22).
4. Connected to the EC2 instance using SSH.
5. Installed and started the Apache web server.
6. Uploaded the `index.html` file to the Apache web root directory.
7. Accessed the webpage using the EC2 public IPv4 address.
8. Created and attached the `EC2-CloudWatch-Role` IAM role.
9. Configured a CloudWatch CPU utilization alarm with a 70% threshold.
10. Created a CloudWatch dashboard to visualize CPU activity.

## Security and Monitoring

- Configured security group rules to control inbound traffic.
- Enabled CPU utilization monitoring through CloudWatch.
- Created a CloudWatch alarm to identify high CPU usage.
- Used a CloudWatch dashboard to monitor server performance.

## Project Objectives

- Understand AWS EC2 instance creation and configuration.
- Learn how to deploy a static website on an AWS server.
- Understand Apache web server installation and configuration.
- Monitor EC2 performance using Amazon CloudWatch.
- Configure CloudWatch alarms and dashboards.

## Skills Demonstrated

- Amazon EC2
- AWS IAM Roles
- Amazon CloudWatch
- Linux Server Administration
- Apache Web Server
- HTML
- CSS
- Website Deployment
- Cloud Monitoring
- AWS Security Best Practices
