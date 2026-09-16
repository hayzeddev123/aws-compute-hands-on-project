# AWS Compute Hands-On Project
# AWS Compute Hands-On Project

**Name:** Abdulazeez Adeniyi  
**Role:** Student  
**Project:** AWS Compute Hands-On Project

## 1. Introduction

The AWS Compute Hands-On Project was designed to provide practical experience with different AWS compute services. The project involved deploying and managing EC2 instances, connecting to an EC2 instance, configuring Auto Scaling and Load Balancing, deploying a serverless Lambda function, and preparing an application for deployment with AWS Elastic Beanstalk.

The project helped me understand how AWS compute services can be used to build applications that are scalable, available, and easier to manage.

## 2. Objectives

The main objectives of the project were to:

- Launch and manage an Amazon EC2 instance.
- Connect to an EC2 instance using SSH.
- Configure an Auto Scaling Group and Load Balancer.
- Deploy and test a serverless AWS Lambda function.
- Understand application deployment using AWS Elastic Beanstalk.
- Gain practical experience using the AWS Management Console.

## 3. EC2 Instance Deployment

I started by navigating to the Amazon EC2 service in the AWS Management Console. I launched an EC2 instance using an appropriate Amazon Machine Image and instance type.

I configured a key pair for secure access and created a security group that allowed the required traffic, including SSH on port 22 and HTTP on port 80 where necessary.

**Security group:** `project2-app-sg`

The inbound rule allowed TCP traffic on port **80**. The outbound rule allowed all traffic to `0.0.0.0/0`.

![Security group project2-app-sg inbound and outbound rules](./Screenshot%202026-08-30%20143021.png)

After launching the instance, I monitored its status to confirm that it was running successfully.

## 4. Connecting to the EC2 Instance

After launching the EC2 instance, I connected to it using SSH and the configured key pair.

I verified that the connection was successful by running:

```bash
uname -a
