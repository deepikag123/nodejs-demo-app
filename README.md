# Node.js Demo App with CI/CD using GitHub Actions and Docker Hub

This project demonstrates a simple **Node.js application** containerized using **Docker** and deployed with an automated **CI/CD pipeline** via **GitHub Actions**.

---

## 🚀 Project Overview
- **Language:** Node.js (Express app)
- **Containerization:** Docker
- **CI/CD Tool:** GitHub Actions
- **Registry:** Docker Hub

Whenever code is pushed to the `main` branch:
1. GitHub Actions builds the Docker image.
2. The image is pushed to **Docker Hub** automatically.
3. The image can then be pulled and run on any Docker-enabled system.

---

## 🛠️ Setup & Workflow

### 1. Application Files
- `app.js` → simple Node.js server
- `package.json` → Node dependencies
- `Dockerfile` → steps to build the image
- `.github/workflows/main.yml` → GitHub Actions pipeline config

### 2. GitHub Actions Workflow
- Runs on every push to `main`
- Builds and tags the Docker image
- Logs in to Docker Hub
- Pushes image to:  
  **`worldofdeepika/nodejs-demo-app:latest`**

### 3. Docker Hub Repository
👉 [Docker Hub Repo](https://hub.docker.com/r/worldofdeepika/nodejs-demo-app)

---

## ▶️ Running the App

On any machine with Docker installed:

```bash
# Pull the latest image
docker pull worldofdeepika/nodejs-demo-app:latest

# Run the container
docker run -p 3000:3000 worldofdeepika/nodejs-demo-app:latest
