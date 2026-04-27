# Jenkins + Docker CI/CD Pipeline

Complete CI/CD pipeline integrating Jenkins with Docker to automate the build, test, and deployment of containerized applications. Demonstrates a real-world pipeline from code commit to running container.

---

## 🛠️ Tech Stack

- **Jenkins** — CI/CD automation server
- **Docker** — containerization and image management
- **Jenkinsfile** — declarative pipeline as code
- **GitHub** — source code management and webhook triggers

---

## 🏗️ Pipeline Overview

```
GitHub Push → Jenkins Webhook → Pipeline Triggered
    → Checkout Code
    → Docker Build
    → Docker Test
    → Docker Push to Registry
    → Deploy Container
```

---

## 📁 Project Structure

```
jenkins-docker/
├── Jenkinsfile             # Declarative pipeline definition
├── Dockerfile              # Container image build instructions
├── app/                    # Application source code
└── docker-compose.yml      # Local development environment
```

---

## ⚙️ Jenkinsfile Pipeline Stages

```groovy
pipeline {
    agent any
    stages {
        stage('Checkout') { ... }      // Pull code from GitHub
        stage('Build') { ... }         // docker build
        stage('Test') { ... }          // Run tests inside container
        stage('Push') { ... }          // Push to Docker registry
        stage('Deploy') { ... }        // Run updated container
    }
}
```

---

## 🚀 Getting Started

### Prerequisites
- Jenkins server with Docker plugin installed
- Docker installed on Jenkins agent
- Docker Hub or ECR credentials configured in Jenkins

### Setup

1. Create a new Jenkins Pipeline job
2. Point it to this repository
3. Jenkins reads the `Jenkinsfile` automatically
4. Configure GitHub webhook to trigger on push

---

## 💡 Key Concepts Demonstrated

- **Pipeline as Code** — entire CI/CD workflow defined in `Jenkinsfile`, version controlled with the app
- **Webhook triggers** — pipeline runs automatically on every GitHub push
- **Docker inside Jenkins** — build and run containers as pipeline steps
- **Credential management** — registry credentials stored in Jenkins credentials store, never hardcoded
- **Stage-based pipeline** — clear separation of build, test, push, deploy phases

---

## 🔗 Related Projects

- [jenkins-ci-pipeline](https://github.com/tahoorshah/jenkins-ci-pipeline) — Jenkins + Git integration
- [docker-aws-ecr-pipeline](https://github.com/tahoorshah/docker-aws-ecr-pipeline) — Docker pipeline with AWS ECR

---

## 📝 Author

**Syed Tahoor Ali Shah**
- GitHub: [@tahoorshah](https://github.com/tahoorshah)
- Medium: [@tahoorshah](https://medium.com/@tahoorshah)
- LinkedIn: [syedtahooralishah](https://linkedin.com/in/syedtahooralishah)
