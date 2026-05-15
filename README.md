# 🚀 Talent Forge DevOps Project
### Dockerized Application with CI/CD Pipeline

**By NJI MENYONGA ARIANE RUTH**  
📅 Date: May 15, 2026

---

## 📌 Project Overview

Talent Forge DevOps is a containerized web application demonstrating a complete, end-to-end DevOps workflow. Every code push triggers a fully automated chain — Docker build, image publish, and live deployment — with zero manual steps.

| Resource | URL |
|----------|-----|
| 🐙 GitHub Repository | https://github.com/NjiAriane/talent-forge-devops |
| 🐳 Docker Hub Image | https://hub.docker.com/r/ariana1/myapp |
| 🌐 Live Application | https://talent-forge-devops.onrender.com |

### Key Learning Outcomes
- Practical CI/CD implementation from code push to live deployment
- Git branching, pull requests, and multi-branch merging
- Docker containerization and image publishing to Docker Hub
- Automated deployment and 24/7 uptime monitoring

---

## 🏗️ System Architecture

The system is composed of five integrated services working together in a continuous pipeline.
💻  Developer
Edits code locally
↓
🐙  GitHub Repository
git push to main branch
↓
⚡  GitHub Actions CI
Workflow triggered — builds Docker image
↓
📦  Docker Hub
Built image pushed to ariana1/myapp
↓
🚀  Render
Pulls latest image & redeploys automatically
↓
🌐  Live Web App
talent-forge-devops.onrender.com
↓
🔔  UptimeRobot
Monitors availability — alerts on downtime

| Layer | Tool | Responsibility |
|-------|------|----------------|
| Source Control | GitHub | Version control, branch management, PR workflow |
| CI Pipeline | GitHub Actions | Automated build & Docker image push on push to main |
| Container Registry | Docker Hub | Stores and distributes the versioned Docker image |
| CD / Hosting | Render | Pulls the latest Docker image and serves the live app |
| Monitoring | UptimeRobot | Monitors availability and sends downtime alerts |

---

## 🛠️ Technology Stack

| Technology | Tier | Purpose |
|------------|------|---------|
| Docker | Latest stable | Application containerization and environment isolation |
| GitHub | Cloud / Free | Source code repository and collaboration platform |
| GitHub Actions | Cloud CI runner | Automated CI pipeline (build + push) |
| Docker Hub | Public registry | Container image storage and distribution |
| Render | Cloud PaaS | Continuous deployment and web hosting |
| UptimeRobot | Free monitoring | Availability monitoring and alert notifications |

---

## 📁 Repository Structure
talent-forge-devops/
├── .github/workflows/
│   └── deploy.yml             # GitHub Actions CI/CD workflow
├── Dockerfile                 # Container image definition
├── Dockerfile.save            # Backup Dockerfile
├── index.html                 # Main page of the web application
├── about.html                 # About page of the web application
└── README.md                  # Project overview

The app is a static two-page website (`index.html` and `about.html`) served from a Docker container. The `Dockerfile` packages these files into an image. The `deploy.yml` workflow triggers automatically on every push to main.

---

## ⚙️ CI/CD Pipeline

| Step | Action | Description |
|------|--------|-------------|
| 1 | Checkout code | GitHub Actions checks out the latest code from main |
| 2 | Authenticate Docker Hub | Uses GitHub Secrets to log in to Docker Hub securely |
| 3 | Build Docker image | Builds a new image from the Dockerfile |
| 4 | Push to Docker Hub | Pushes the built image to ariana1/myapp |
| 5 | Render auto-deploy | Render detects the new image and redeploys the live app |

---

## 🐳 Docker & Deployment

### Docker
- **Registry:** Docker Hub
- **Image:** `ariana1/myapp` → https://hub.docker.com/r/ariana1/myapp

```bash
docker pull ariana1/myapp               # Pull latest image
docker run -p 8080:80 ariana1/myapp     # Run container locally
# App available at: http://localhost:8080
```

### Deployment (Render)
- **Live URL:** https://talent-forge-devops.onrender.com
- **Type:** Docker container Web Service — auto-deploys on new image push

| Monitor Parameter | Configuration |
|-------------------|---------------|
| Monitor Type | HTTP(S) |
| Monitored URL | https://talent-forge-devops.onrender.com |
| Alert Method | Email notification on downtime |
# Talent Forge DevOps Project
### Dockerized Application with CI/CD Pipeline

**By NJI MENYONGA ARIANE RUTH**  
Date: May 15, 2026

---

## Project Overview

Talent Forge DevOps is a containerized web application demonstrating a complete, end-to-end DevOps workflow. Every code push triggers a fully automated chain — Docker build, image publish, and live deployment — with zero manual steps.

| Resource | URL |
|----------|-----|
| GitHub Repository | https://github.com/NjiAriane/talent-forge-devops |
| Docker Hub Image | https://hub.docker.com/r/ariana1/myapp |
| Live Application | https://talent-forge-devops.onrender.com |

### Key Learning Outcomes
- Practical CI/CD implementation from code push to live deployment
- Git branching, pull requests, and multi-branch merging
- Docker containerization and image publishing to Docker Hub
- Automated deployment and 24/7 uptime monitoring

---

## System Architecture

The system is composed of five integrated services working together in a continuous pipeline.
Developer
Edits code locally
↓
GitHub Repository
git push to main branch
↓
GitHub Actions CI
Workflow triggered — builds Docker image
↓
Docker Hub
Built image pushed to ariana1/myapp
↓
Render
Pulls latest image & redeploys automatically
↓
Live Web App
talent-forge-devops.onrender.com
↓
UptimeRobot
Monitors availability — alerts on downtime

| Layer | Tool | Responsibility |
|-------|------|----------------|
| Source Control | GitHub | Version control, branch management, PR workflow |
| CI Pipeline | GitHub Actions | Automated build & Docker image push on push to main |
| Container Registry | Docker Hub | Stores and distributes the versioned Docker image |
| CD / Hosting | Render | Pulls the latest Docker image and serves the live app |
| Monitoring | UptimeRobot | Monitors availability and sends downtime alerts |

---

## Technology Stack

| Technology | Tier | Purpose |
|------------|------|---------|
| Docker | Latest stable | Application containerization and environment isolation |
| GitHub | Cloud / Free | Source code repository and collaboration platform |
| GitHub Actions | Cloud CI runner | Automated CI pipeline (build + push) |
| Docker Hub | Public registry | Container image storage and distribution |
| Render | Cloud PaaS | Continuous deployment and web hosting |
| UptimeRobot | Free monitoring | Availability monitoring and alert notifications |

---

## Repository Structure
talent-forge-devops/
├── .github/workflows/
│   └── deploy.yml             # GitHub Actions CI/CD workflow
├── Dockerfile                 # Container image definition
├── Dockerfile.save            # Backup Dockerfile
├── index.html                 # Main page of the web application
├── about.html                 # About page of the web application
└── README.md                  # Project overview

The app is a static two-page website (`index.html` and `about.html`) served from a Docker container. The `Dockerfile` packages these files into an image. The `deploy.yml` workflow triggers automatically on every push to main.

---

## CI/CD Pipeline

| Step | Action | Description |
|------|--------|-------------|
| 1 | Checkout code | GitHub Actions checks out the latest code from main |
| 2 | Authenticate Docker Hub | Uses GitHub Secrets to log in to Docker Hub securely |
| 3 | Build Docker image | Builds a new image from the Dockerfile |
| 4 | Push to Docker Hub | Pushes the built image to ariana1/myapp |
| 5 | Render auto-deploy | Render detects the new image and redeploys the live app |

---

## Docker & Deployment

### Docker
- **Registry:** Docker Hub
- **Image:** `ariana1/myapp` — https://hub.docker.com/r/ariana1/myapp

```bash
docker pull ariana1/myapp               # Pull latest image
docker run -p 8080:80 ariana1/myapp     # Run container locally
# App available at: http://localhost:8080
```

### Deployment (Render)
- **Live URL:** https://talent-forge-devops.onrender.com
- **Type:** Docker container Web Service — auto-deploys on new image push

| Monitor Parameter | Configuration |
|-------------------|---------------|
| Monitor Type | HTTP(S) |
| Monitored URL | https://talent-forge-devops.onrender.com |
| Alert Method | Email notification on downtime |

---

## Git Branching & Environment Variables

### Branch Strategy

| Branch | Triggers CI/CD | Purpose |
|--------|---------------|---------|
| `main` | Yes | Production-ready. Pipeline fires on every push. |
| `feature/*` | No | Development branches. Merged to main via Pull Request. |

**Workflow:**
1. Create a feature branch from main
2. Develop, commit, and push changes
3. Open a Pull Request and merge to main
4. CI/CD pipeline triggers automatically

### Secrets & Environment Variables

| Variable | Scope | Description |
|----------|-------|-------------|
| `DOCKER_USERNAME` | GitHub Secrets | Docker Hub username for CI authentication |
| `DOCKER_PASSWORD` | GitHub Secrets | Docker Hub access token for secure login |
| App-level vars | Render Dashboard | Runtime environment variables for the application |

---

## Troubleshooting

| Issue | Likely Cause | Resolution |
|-------|-------------|------------|
| Actions workflow fails | Invalid Docker credentials | Check `DOCKER_USERNAME` and `DOCKER_PASSWORD` in GitHub Secrets |
| Image not updating on Render | Auto-deploy not configured | Verify Render service is set to auto-deploy from Docker Hub |
| App down at live URL | Container crash / Render issue | Check Render logs; verify Docker image runs locally first |
| `docker pull` fails locally | Image not found or private | Ensure image is public on Docker Hub or run `docker login` |

---

## Glossary

| Term | Definition |
|------|------------|
| CI | Continuous Integration — automated build & validation on every code push |
| CD | Continuous Deployment — automated release to production without manual steps |
| Docker | Platform for packaging applications into portable, isolated containers |
| Docker Hub | Cloud registry for storing and distributing Docker images |
| GitHub Actions | GitHub's built-in CI/CD tool triggered by repository events |
| Render | Cloud PaaS that hosts and auto-deploys web apps from Docker images |
| UptimeRobot | Free monitoring service that alerts on website downtime |
| Pipeline | Automated sequence of steps: build, push, deploy |
| Pull Request | GitHub mechanism to review and merge code from a feature branch to main |
| Dockerfile | Instructions for building a Docker image |
| GitHub Secrets | Encrypted variables used in workflows without exposing credentials in code |

---

## What I Learnt

- Came in with CI/CD theory. This project gave me the practical side: branching, pull requests, and merging cleanly into main
- Every push to main triggers GitHub Actions to build a Docker image and push it to Docker Hub automatically. That is CI
- Render picks up the new image and serves it live without any manual step. That is CD
- Used Render for the first time and learned the entire pipeline can run completely free
- If something breaks, UptimeRobot alerts immediately. Monitoring is part of the workflow, not an afterthought
- DevOps is not just about understanding tools. It is about knowing how all the pieces connect and move together in a real workflow
