PROJECT: WEBSITE DEPLOYMENT ON AWS EC2 USING APACHE WEB SERVER

Project Overview
This project demonstrates how to deploy and host a static eCommerce website on an AWS EC2 instance using the Apache Web Server.
The main objective was to launch an Ubuntu Linux server on AWS, configure network security, install Apache, transfer website files securely, and make the website accessible through a public IP address.

Technologies Used
•	AWS EC2: Cloud server hosting
•	Ubuntu Linux: Operating system
•	Apache2: Web server
•	AWS Security Groups: Network access configuration
•	SCP: Secure file transfer
•	Linux Commands: Server and file management

Project Implementation
Step by step Deployment Process :

•	Step 1: EC2 Instance Creation 

•	Launched an AWS EC2 instance with Ubuntu Server  t3.micro instance.
•	 AWS Console → EC2 → Launch Instance
•	 EC2 Name: web-hosting-mini-project
•	  Instance Type: t3.micro
•	  Key Pair: xyz-key-ec2.pem
 

Step 2: Security Group Configuration
Configured inbound rules to allow SSH access on port 22 and HTTP traffic on port 80.
 
Security Group Inbound Rules
Rule type         Protocol             Port Range
HTTP	TCP	80

Step 3: Server Connection
Connected to the EC2 instance using  EC2 Instance Connect
 
Step 4: Apache Installation
Updated the Ubuntu package repository and installed the Apache2 web server.
Commands:
sudo apt update
sudo apt install apache2 -y
 

Apache server successfully installed
Step 5: Website File Transfer
Transferred the eCommerce website ZIP file from the (Command prompt)local machine to the EC2 instance using SCP.
 

Step 6: Extract Website Files
Installed the unzip utility and extracted the website project files on the EC2 server.
 
 



Step 7: Website Deployment
Copied the extracted website files into the Apache default web directory.
sudo rm  index.html
sudo cp  . -r  /var/www/html/
We removed the default index.html file from the Apache web server and copied all the project files into the Apache document root directory (/var/www/html). Then, we successfully deployed the project.

 
Step 8: Deployment Verification :
Opened the EC2 public IPv4 address in a web browser to verify that the Zay eCommerce website was accessible or not.
 
Project Outcome
Successfully deployed and hosted a static eCommerce website on an AWS EC2 Ubuntu instance using Apache Web Server.
The website was accessible through the EC2 public IP address over HTTP.

Skills Demonstrated
•	AWS EC2 instance provisioning
•	Linux server administration
•	Apache web server configuration
•	AWS Security Group management
•	SSH authentication and SCP file transfer
•	Static website deployment
•	Basic deployment troubleshooting
Conclusion
This project provided practical experience in deploying a website on AWS cloud infrastructure, configuring Linux servers, managing network access, and hosting web applications using Apache.




