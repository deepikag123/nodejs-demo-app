
# Node.js Demo App with CI/CD using GitHub Actions and Docker Hub

This project demonstrates a simple **Node.js application** containerized using **Docker** and deployed with an automated **CI/CD pipeline** via **GitHub Actions**.

---

## 🚀 Project Overview
- **Language:** Node.js (Express app)
- **Containerization:** Docker
- **CI/CD Tool:** GitHub Actions
- **Registry:** Docker Hub

The pipeline automatically builds and pushes the Docker image to **Docker Hub** whenever changes are pushed to the `main` branch.

---

## 🛠️ Setup & Workflow

### 1. Dockerfile
A `Dockerfile` is included to containerize the Node.js app.

### 2. GitHub Actions Workflow
Located in `.github/workflows/main.yml`:
- Triggers on push to `main`
- Builds Docker image
- Pushes image to Docker Hub repository:  
  `worldofdeepika/nodejs-demo-app:latest`

### 3. Docker Hub Repository
The final image is hosted at:  
👉 [Docker Hub Link](https://hub.docker.com/r/worldofdeepika/nodejs-demo-app)

---

## ▶️ Running the App (on any machine with Docker)
```bash
# Pull the latest image
docker pull worldofdeepika/nodejs-demo-app:latest

# Run the container
docker run -p 3000:3000 worldofdeepika/nodejs-demo-app:latest
