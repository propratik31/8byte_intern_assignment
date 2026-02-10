# DevOps Intern Assignment – 8byte AI

## Project Overview

This project demonstrates an end-to-end DevOps workflow where a Node.js application is containerised using Docker, deployed on AWS EC2 using Terraform, and automated using GitHub Actions.

The assignment covers **Infrastructure as Code, containerization, cloud deployment, and CI/CD automation**.

---

## Technology Stack

Cloud Provider: AWS
Infrastructure as Code: Terraform
Containerization: Docker
CI/CD: GitHub Actions
Application: Node.js (Express)
Operating System: Ubuntu 22.04


## Architecture Overview

VPC with public subnet
Internet Gateway and Route Table
Security Group allowing ports **22 (SSH)** and **3000 (Application)**
EC2 instance with Docker installed using Terraform `user_data`
Dockerized Node.js application running on EC2
CI pipeline triggered on GitHub push


## Run Application Locally

### Install dependencies
npm install


### Run application
node app.js


## Dockerize the Application

### Build Docker image
docker build -t 8byte-intern-app .


### Run Docker container
docker run -p 3000:3000 8byte-intern-app


## Provision AWS Infrastructure Using Terraform

### Initialize Terraform
terraform init


### View execution plan
terraform plan

### Apply infrastructure
terraform apply


### Terraform provisions:

VPC
Public Subnet
Internet Gateway
Route Table
Security Group
EC2 instance with Docker installed


## Deploy Application on EC2

Connect to EC2 instance


### Clone repository
git clone https://github.com/propratik31/8byte_intern_assignment.git
cd 8byte_intern_assignment


### Build Docker image
docker build -t 8byte-intern-app .

### Run Docker container
docker run -d -p 3000:3000 8byte-intern-app


### Application URL:- http://13.233.127.51:3000

### CI/CD with GitHub Actions
Workflow file location:- .github/workflows/ci.yml


### Screenshots
Terraform apply output:- <img width="1276" height="747" alt="terraform output" src="https://github.com/user-attachments/assets/23404187-5521-4bcf-bc0f-05e8bd1a9204" />

Docker Image and Container:- <img width="1853" height="277" alt="docker image and container" src="https://github.com/user-attachments/assets/044c15e1-bf88-442f-93ab-be2cc5798f5f" />
 
Application running in browser:- <img width="1917" height="256" alt="Final output" src="https://github.com/user-attachments/assets/813f7b13-915d-4425-87c7-88794861f37f" />

Successful GitHub Actions workflow:- <img width="1916" height="713" alt="workflow" src="https://github.com/user-attachments/assets/033b6f68-68e3-49c0-aa5b-9b4110a39d14" />


### Conclusion

This project demonstrates the successful deployment of a Dockerized Node.js application on AWS using Terraform, with CI automation implemented through GitHub Actions, following DevOps best practices.


