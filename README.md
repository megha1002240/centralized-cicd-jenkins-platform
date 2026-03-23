# 🚀 Centralized CI/CD System with Shared Jenkins Pipelines

---

## 📌 Overview

This project showcases the implementation of a **centralized CI/CD system** using Jenkins that enables multiple applications to follow a unified and reusable pipeline approach.

Rather than having separate Jenkins setups for each team, a **single shared platform** is used to streamline the entire software delivery lifecycle — from code integration to deployment.

---

## 🎯 Purpose

The aim of this solution is to:

* Eliminate redundant CI/CD setups
* Maintain consistent pipeline execution across projects
* Improve security and governance
* Promote reusable and modular pipeline design

---

## 🧰 Tools & Technologies

* Jenkins (Automation Server)
* GitHub (Source Code Management)
* AWS EC2 (Hosting Jenkins)
* Docker (Containerization)
* Jenkins Shared Libraries

---

## 🏗️ System Design

Developers commit code to their repositories, which triggers Jenkins pipelines. These pipelines utilize a **shared library** to execute predefined stages and build containerized applications.

### 🔄 Workflow:

```
Developer → GitHub → Jenkins (EC2) → Shared Library → Agent Node 
→ Build → Test → Security Check → Deploy → Docker Image
```

---

## 📊 Architecture Diagram

📸 Add your diagram here:

```
docs/architecture-diagram.png
```

---

## 📁 Repositories Overview

### 🔹 Shared Pipeline Library
# Repo link: 
https://github.com/megha1002240/jenkins-shared-library

This repository contains reusable pipeline logic used across all applications.

**Structure:**

```
jenkins-shared-lib/
│
└── vars/
    └── cicdPipeline.groovy

<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/f514073f-ceb6-450f-9cea-dc07c7ca4aec" />

---

### 🔹 Sample Application 1 (Node.js)
# Repo link: 
https://github.com/megha1002240/app1-nodejs
**Structure:**

```
nodejs-app/
│
├── app.js
├── package.json
├── Dockerfile
└── Jenkinsfile
```

📸 Screenshot:


<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/319213a1-0a8f-4c4c-812b-f803c3bfa877" />



---

### 🔹 Sample Application 2 (Python)
# Repo link:
https://github.com/megha1002240/app2-python
**Structure:**

```
python-app/
│
├── app.py
├── Dockerfile
└── Jenkinsfile
```

📸 Screenshot:


<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/af87d4ab-f5b8-4ac9-8566-b332ec4ab443" />



---

## ⚙️ Jenkins Setup

The Jenkins server is hosted on an EC2 instance and configured for centralized pipeline execution.

### 🔧 Steps Performed:

* Created EC2 instance
* Installed Java runtime
* Installed and configured Jenkins
* Added necessary plugins
* Configured build agents
* Set up credentials
* Integrated shared library

📸 Dashboard Screenshot:


![WhatsApp Image 2026-03-23 at 2 28 11 PM](https://github.com/user-attachments/assets/d01578d0-2438-4594-80d3-ac6fb67ee370)



---

## 🖥️ Build Agent Setup

A dedicated agent is configured to handle pipeline execution.

### Configuration Details:

* Name: docker-agent
* Executors: 1
* Connection: SSH
* Label: docker

📸 Screenshot:


<img width="1920" height="1008" alt="Screenshot 2026-03-19 152211" src="https://github.com/user-attachments/assets/53840038-489f-4c31-b5c1-277326aa2024" />
<img width="1920" height="1008" alt="Screenshot 2026-03-19 152148" src="https://github.com/user-attachments/assets/67d28609-e80d-45e8-9721-1ec4abef884b" />




---

## 📚 Shared Library Integration

Configured in Jenkins under:

```
Manage Jenkins → Global Pipeline Libraries
```

**Library Identifier:**

```
shared-library-config
```

📸 Screenshot:


<img width="1920" height="1008" alt="Screenshot 2026-03-19 152239" src="https://github.com/user-attachments/assets/7b369f99-7f4c-464f-abaf-085de6d39549" />



---

## 🔄 Pipeline Jobs

Two applications are integrated into Jenkins:

* nodejs-app-pipeline
* python-app-pipeline

📸 Scrrenshot:

<img width="1920" height="1008" alt="Screenshot 2026-03-19 145336" src="https://github.com/user-attachments/assets/7012acdf-15e2-4dae-8ad2-456490e6f881" />
<img width="1920" height="1008" alt="Screenshot 2026-03-19 145115" src="https://github.com/user-attachments/assets/4a88c750-02a5-407e-8e4b-430ac3f37722" />




---

## 🚀 Pipeline Execution Stages

Each pipeline follows a consistent structure:

1. Code Checkout
2. Build Process
3. Testing Phase
4. Security Scanning
5. Deployment

📸 Stage View:


<img width="1920" height="1008" alt="Screenshot 2026-03-19 145336" src="https://github.com/user-attachments/assets/9d153198-4d86-46b4-991a-807d2f0b6f4d" />



---

## 🐳 Docker Build Process

During the build stage, Docker images are created for deployment.

### Example Command:

```bash
docker build -t your-dockerhub-meghapatil56285/nodejs-app:latest .
```



---

## 📦 Deliverables

This project includes:

* Centralized Jenkins platform
* Reusable shared pipeline library
* Multiple application pipelines
* Automated Docker image builds
* Role-based access configuration

---

## 📚 Learning Highlights

Through this project, the following skills are demonstrated:

* Designing scalable CI/CD systems
* Jenkins administration and configuration
* Creating reusable pipeline libraries
* Docker-based application deployment
* Cloud-based infrastructure setup
* Managing multi-project CI/CD workflows

---

## ✅ Summary

This implementation proves how a centralized Jenkins setup can efficiently manage multiple applications using shared logic. It ensures uniformity, reduces operational overhead, and simplifies CI/CD management.

---

## 🔮 Possible Enhancements

* Integration with Kubernetes for orchestration
* Advanced vulnerability scanning tools
* Infrastructure automation using Terraform
* Automated rollback and failure handling
* Monitoring and alerting integration

---

## 👩‍💻 Author

**Megha Patil**
Cloud & DevOps Enthusiast

---
