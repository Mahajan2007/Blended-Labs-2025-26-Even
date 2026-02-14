# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: ___MahaJanani.R_____________________________
* **Register Number**: ___212224230147__________________
* **Date of Submission**: _______14.02.26___________

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1.First, I created a new VPC
I created a Virtual Private Cloud (VPC) to have a private network inside AWS.
While creating the VPC, I assigned a CIDR block of 10.0.0.0/16 and gave it a meaningful name.
This VPC acts as an isolated network where all my AWS resources are placed.

2.Next, I created a public subnet inside the VPC
Inside the VPC, I created a public subnet with the CIDR block 10.0.1.0/24.
I enabled the option Auto-assign public IPv4 address so that any EC2 instance launched in this subnet can get a public IP address and be accessed from the internet.

3.Then, I created and attached an Internet Gateway
I created an Internet Gateway and attached it to the VPC.
This Internet Gateway allows the VPC resources, especially the EC2 instance, to communicate with the internet.

4.After that, I configured the route table
I created a new route table and added a route with destination 0.0.0.0/0 pointing to the Internet Gateway.
I associated this route table with the public subnet so that traffic from the subnet can reach the internet.

5.Next, I created a security group
I created a security group to act as a firewall for the EC2 instance.
I added inbound rules to allow:

SSH access on port 22 for remote login

HTTP access on port 80 to access the web server from a browser

6.Then, I launched an EC2 instance
I launched an EC2 instance using Amazon Linux 2 AMI and selected the t2.micro instance type.
I launched it inside the public subnet and attached the security group and key pair created earlier.

7.Finally, I installed and configured the web server
I connected to the EC2 instance using SSH and installed the Apache HTTPD web server.
After starting the Apache service, I created a simple HTML webpage.
I verified the setup by opening the public IP address of the EC2 instance in a web browser, and the webpage was displayed successfully.

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c33f9357-2b93-4d98-8f68-32214a08ba25" />


### Screenshot 2: EC2 Instance Running

![WhatsApp Image 2026-02-14 at 11 25 20 AM](https://github.com/user-attachments/assets/ff6fada2-1ded-4296-bc05-15a45363d476)


### Screenshot 3: Web Server Output in Browser

![WhatsApp Image 2026-02-07 at 11 43 47 AM](https://github.com/user-attachments/assets/5ec4e7da-3ebf-4b27-be76-e96267520530)

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
