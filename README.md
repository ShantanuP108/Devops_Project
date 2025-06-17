# CI/CD Pipeline with Jenkins, Docker, and Kubernetes (Kind)

## Overview
This project demonstrates a full CI/CD pipeline for a Node.js web application using Jenkins, Docker, and Kubernetes (Kind cluster). It automates build, test, Docker image creation, and Kubernetes deployment — making it ideal for production-grade DevOps workflows.

## Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Setup](#setup)
- [How to Run](#how-to-run)
- [CI/CD Flow](#cicd-flow)
- [License](#license)

## Tech Stack

- **Node.js** – App backend
- **Docker** – Containerization
- **Jenkins** – CI/CD Orchestration
- **Kubernetes (Kind)** – Container orchestration
- **kubectl** – Cluster interaction

## Setup

Make sure the following tools are installed:
- Docker
- kubectl
- Jenkins (with Docker + Kubernetes plugins)

Start Jenkins with:
```bash
sudo systemctl start jenkins
```

## How to Run

```bash
./scripts/build.sh
./scripts/deploy.sh
```

## CI/CD Flow

1. Code is committed to the repository.
2. Jenkins pulls the code and runs tests.
3. Docker image is built and pushed (if needed).
4. Jenkins deploys the image to the Kubernetes cluster.

## License
This project is licensed under the MIT License.
