# Flask App with CI/CD on AWS EC2

## Overview

This is a simple Flask application designed to demonstrate basic CRUD operations with a MySQL database. It includes user registration, login, and the ability to add and show records. It is deployed on an AWS EC2 instance using a CI/CD pipeline with Jenkins.

## Technologies Used

- Flask (Python web framework)
- Docker (Containerization)
- AWS EC2 (Virtual server)
- AWS ECR (Container registry)
- Jenkins (CI/CD automation)
- Ansible (Configuration management)
- GitHub (Version control)

## Features

- Automates deployment using Jenkins
- Builds and pushes Docker images to AWS ECR
- Deploys the application on an EC2 instance using Ansible


## CI/CD Pipeline

### Jenkins Pipeline

The Jenkins pipeline is defined in the `Jenkinsfile`. It performs the following steps:

1. Logs into AWS ECR
2. Checks out the latest code from GitHub
3. Determines the new version for the Docker image
4. Builds and pushes the Docker image to AWS ECR
5. Deploys the app to EC2 using Ansible

### Ansible Playbook

The `playbook.yaml` file is used for deploying the application on EC2. It:

- Pulls the latest Docker image from AWS ECR
- Runs the Flask app inside a Docker container

<br>
<br>
![screenshot](https://github.com/user-attachments/assets/ed8f83bc-ba19-4e19-803d-b07be0c45f17)

