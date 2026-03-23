# 🚀 Centralized CI/CD System with Shared Jenkins Pipelines

---

## 📌 Overview

This project demonstrates the implementation of a **centralized CI/CD system** using Jenkins, enabling multiple applications to use a **shared and standardized pipeline framework**.

Instead of maintaining separate Jenkins instances for each team, a **single centralized platform** is used to streamline the entire software delivery lifecycle — from code integration to deployment.

---

## 🎯 Purpose

This solution is designed to:

* Eliminate duplicate CI/CD infrastructure
* Ensure consistent pipeline execution across projects
* Improve security and governance
* Enable reusable and modular pipeline design

---

## 🧰 Technologies Used

* Jenkins (Automation Server)
* GitHub (Source Code Management)
* AWS EC2 (Jenkins Hosting)
* Docker (Containerization)
* Jenkins Shared Libraries

---

## 🏗️ System Architecture

Developers push code to GitHub repositories, which triggers Jenkins pipelines. These pipelines utilize a **shared library** to execute standardized stages and build containerized applications.

### 🔄 Workflow

```
Developer → GitHub → Jenkins (EC2) → Shared Library → Agent Node 
→ Build → Test → Scan → Deploy → Docker Image
```

---

## 📊 Architecture Diagram

📸 Location:

```
docs/architecture-diagram.png
```

---

## 📁 Repositories Overview

### 🔹 Jenkins Shared Library

**Repository:**
https://github.com/megha1002240/jenkins-shared-library

This repository contains reusable pipeline logic shared across multiple applications.

**Structure:**

```
jenkins-shared-library/
│
└── vars/
    └── cicdPipeline.groovy
```

📸 Screenshot:

<img width="1920" height="1008" src="https://github.com/user-attachments/assets/f514073f-ceb6-450f-9cea-dc07c7ca4aec" />

---

### 🔹 Node.js Application

**Repository:**
https://github.com/megha1002240/app1-nodejs

**Structure:**

```
app-nodejs/
│
├── app.js
├── package.json
├── Dockerfile
└── Jenkinsfile
```

📸 Screenshot:

<img width="1920" height="1008" src="https://github.com/user-attachments/assets/319213a1-0a8f-4c4c-812b-f803c3bfa877" />

---

### 🔹 Python Application

**Repository:**
https://github.com/megha1002240/app2-python

**Structure:**

```
app-python/
│
├── app.py
├── Dockerfile
└── Jenkinsfile
```

📸 Screenshot:

<img width="1920" height="1008" src="https://github.com/user-attachments/assets/af87d4ab-f5b8-4ac9-8566-b332ec4ab443" />

---

## ⚙️ Jenkins Infrastructure Setup

Jenkins is deployed on an AWS EC2 instance and configured to support centralized CI/CD operations.

### 🔧 Setup Steps

* Launch EC2 instance
* Install Java
* Install Jenkins
* Install required plugins
* Configure Jenkins agents
* Set up credentials (GitHub, Docker)
* Integrate shared library

📸 Jenkins Dashboard:

<img src="https://github.com/user-attachments/assets/d01578d0-2438-4594-80d3-ac6fb67ee370" />

---

## 🖥️ Jenkins Agent Configuration

A dedicated build agent is configured for executing pipelines.

### Configuration Details

* **Name:** docker-agent
* **Executors:** 1
* **Launch Method:** SSH
* **Label:** docker

📸 Screenshots:

<img width="1920" height="1008" src="https://github.com/user-attachments/assets/53840038-489f-4c31-b5c1-277326aa2024" />
<img width="1920" height="1008" src="https://github.com/user-attachments/assets/67d28609-e80d-45e8-9721-1ec4abef884b" />

---

## 📚 Shared Library Configuration

Configured in Jenkins under:

```
Manage Jenkins → Global Pipeline Libraries
```

### Library Name

```
shared-library-config
```

📸 Screenshot:

<img width="1920" height="1008" src="https://github.com/user-attachments/assets/7b369f99-7f4c-464f-abaf-085de6d39549" />

---

## 🔄 Jenkins Pipelines

Two pipeline jobs are configured:

* nodejs-app-pipeline
* python-app-pipeline

📸 Screenshots:

<img width="1920" height="1008" src="https://github.com/user-attachments/assets/7012acdf-15e2-4dae-8ad2-456490e6f881" />
<img width="1920" height="1008" src="https://github.com/user-attachments/assets/4a88c750-02a5-407e-8e4b-430ac3f37722" />

---

## 🚀 CI/CD Pipeline Stages

Each pipeline follows a standardized flow:

1. Checkout Code
2. Build Application
3. Run Tests
4. Security Scan
5. Deploy Application

📸 Pipeline Stage View:

<img width="1920" height="1008" src="https://github.com/user-attachments/assets/9d153198-4d86-46b4-991a-807d2f0b6f4d" />

---

## 🐳 Docker Build

Docker images are created during the build stage.

### Example Command

```bash
docker build -t meghapatil56285/nodejs-app:latest .
```

---

## 📦 Project Deliverables

* Centralized Jenkins CI/CD platform
* Shared pipeline library
* Multi-application pipeline setup
* Automated Docker image builds
* Role-based access control

---

## 📚 Key Learnings

This project demonstrates:

* CI/CD pipeline automation
* Jenkins administration
* Shared library implementation
* Docker-based deployments
* AWS infrastructure setup
* Multi-project pipeline design

---

## ✅ Conclusion

The centralized Jenkins platform successfully enables multiple applications to share a common pipeline structure. This improves **scalability, maintainability, and consistency** across development teams.

---

## 🔮 Future Enhancements

* Kubernetes integration for container orchestration
* Advanced security scanning (Trivy, SonarQube)
* Infrastructure as Code (Terraform)
* Automated rollback mechanisms
* Monitoring and alerting integration

---

## 👩‍💻 Author

**Megha Patil**
Cloud & DevOps Engineer

---
