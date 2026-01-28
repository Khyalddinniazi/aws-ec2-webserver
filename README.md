# aws-ec2-webserver

## Overview
This project demonstrates deploying a public web server on AWS using Amazon EC2 inside a custom VPC.
The web server runs Apache and is accessible via a public IP address.


## Architecture
![Architecture Diagram](architecture/Architecture.png)


## AWS Services Used
- Amazon EC2
- Amazon VPC
- Security Groups
- Apache HTTP Server
- AWS Amplify

## What Was Built
- Custom VPC with public subnet
- EC2 instance (t3.micro)
- Apache web server
- Public IP & DNS access
- Frontend deployment using AWS Amplify

## Screenshots

### Web Server Output
![Web Server](screenshots/WEB-server.png)
![Web Server Status](screenshots/WEB-S.png)

### EC2 Instance
![EC2 Instance](screenshots/EC2.png)

### VPC Configuration
![VPC](screenshots/VPC.png)

### AWS Amplify
![AWS Amplify](screenshots/AWS-Amplify.png)
![Amplify Deployment](screenshots/Amplify.png)

## Cost Awareness
All resources were deleted after testing to avoid ongoing AWS charges.
