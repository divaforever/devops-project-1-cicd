# DevOps Project 1 - CI/CD Pipeline using Jenkins, Docker and GitHub

## Project Overview

This project demonstrates a complete CI/CD pipeline using Jenkins, Docker, Git, and GitHub.

The application is a simple static website hosted using Nginx inside a Docker container.

Jenkins automatically:

- Pulls source code from GitHub
- Builds Docker image
- Stops old container
- Deploys new container
- Verifies deployment

---

## Architecture

## CI/CD Architecture

text
Developer
    ↓
GitHub
    ↓
Jenkins Pipeline
    ↓
Docker Build
    ↓
Container Deployment
    ↓
Web Application


## Tools Used

- Git
- GitHub
- Docker
- Jenkins
- Linux (Ubuntu)
- Nginx

---

## Project Workflow

### 1. Source Code Management

Source code stored in GitHub repository.

### 2. Continuous Integration

Jenkins checks out latest code from GitHub.

### 3. Docker Build

Jenkins builds Docker image:

```bash
docker build -t germany-app:v1 .
```
