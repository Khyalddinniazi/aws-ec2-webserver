# Deployment Notes – AWS EC2 Web Server

## Project Goal
The goal of this project was to deploy a simple, publicly accessible web server on AWS in order to understand core cloud concepts such as networking, compute, and security.

## Architecture Decisions

### Why EC2?
EC2 was chosen to gain hands-on experience with managing virtual servers, security groups, and networking rather than using fully managed services.

### Why a Custom VPC?
A custom VPC was created instead of using the default VPC to better understand:
- CIDR blocks
- Subnet design
- Routing
- Internet Gateways

### Why a Public Subnet?
The EC2 instance needed to be publicly accessible over HTTP, so it was placed in a public subnet with a route to an Internet Gateway.

## Security Considerations
- Security groups were configured to allow inbound traffic only on port 80 (HTTP).
- SSH access was restricted and not exposed publicly after setup.
- Only necessary ports were opened.

## Web Server Setup
Apache HTTP Server was installed on the EC2 instance to serve a basic web page.
Successful deployment was verified by accessing the public IP address in a browser.

## AWS Amplify Usage
AWS Amplify was used to deploy a simple frontend and observe a basic CI/CD-style deployment workflow.
This helped demonstrate how changes can be deployed automatically.

## Challenges Faced
- Understanding how routing tables affect public access
- Ensuring the correct security group rules were applied
- Verifying DNS vs public IP access

## Lessons Learned
- Networking configuration is critical for public access
- Security groups act as a firewall at the instance level
- Small misconfigurations can prevent connectivity
- Proper cleanup is essential to avoid unexpected costs

## Future Improvements
- Rebuild the infrastructure using Terraform
- Add an Application Load Balancer
- Enable Auto Scaling
- Add monitoring using Amazon CloudWatch
