# 🚀 AWS DevOps CI/CD Pipeline — Containerized App Deployment on ECS Fargate

> **Auto-deploy on every Git commit** — Code pushed to GitHub triggers a full CI/CD pipeline that builds, pushes, and deploys Docker containers to ECS Fargate with zero manual steps.

---

## 🏗️ Architecture

![Architecture Diagram](./Architecture-diagram.png)

---

## 🔄 How It Works (Flow)

```
Developer pushes code to GitHub
        ↓
AWS CodePipeline triggers (webhook)
        ↓
AWS CodeBuild → builds Docker image
        ↓
Image pushed to ECR (Elastic Container Registry)
        ↓
AWS CodeDeploy → deploys to ECS Fargate (auto-scaled tasks)
        ↓
Traffic served via Load Balancer → Clients / Users
```

---

## 🛠️ Tech Stack

| Category | Services Used |
|---|---|
| **Source Control** | GitHub |
| **CI/CD** | AWS CodePipeline → CodeBuild → CodeDeploy |
| **Containerization** | Docker, Amazon ECR |
| **Orchestration** | Amazon ECS + Fargate (serverless containers) |
| **Networking** | VPC, Availability Zone |
| **Monitoring** | CloudWatch Logs, CloudWatch Alarm |

---

## ✅ Key Features

- **Auto-deploy on commit** — GitHub webhook triggers full pipeline instantly
- **Serverless containers** — ECS Fargate; no EC2 servers to manage
- **Fully monitored** — CloudWatch Logs + Alarms for pipeline and app health
- **Scalable** — Multiple Fargate tasks run in parallel across availability zones

---

## 📁 Project Structure

```
├── Dockerfile              # Container build definition
├── buildspec.yml           # CodeBuild instructions
├── appspec.yml             # CodeDeploy ECS deployment config
├── taskdef.json            # ECS Task Definition
└── app/                    # Application source code
```

---

## 🚀 How to Deploy

1. Push code to the `main` branch on GitHub
2. CodePipeline triggers automatically via webhook
3. CodeBuild builds and pushes the Docker image to ECR
4. CodeDeploy updates the ECS service with the new image
5. Live in minutes — no manual steps required

---

## 📸 Screenshots

| Step | Screenshot |
|---|---|
| CodePipeline Triggered | ![Architecture Diagram](./Architecture-diagram.png) |
| CodeBuild Logs | *(upload screenshot)* |
| ECR Image Pushed | *(upload screenshot)* |
| ECS Fargate Tasks Running | *(upload screenshot)* |
| CloudWatch Monitoring | *(upload screenshot)* |

---

## 👨‍💻 Author

**Chirag** — DevOps Engineer  
[GitHub](https://github.com/) • [LinkedIn](https://linkedin.com/)
