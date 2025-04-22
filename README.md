# CI/CD Pipeline with GitHub Actions & Docker (Local Deployment)

This project sets up a simple CI/CD pipeline using:

- GitHub Actions
- Docker & Docker Hub
- Minikube (or local VM)

---

## How It Works

1. Code is pushed to GitHub.
2. GitHub Actions:
   - Runs tests
   - Builds Docker image
   - Pushes image to Docker Hub
3. Image is pulled and deployed locally using Docker or Minikube.

---

## Run Locally

### Docker
```bash
docker build -t cicd-demo .
docker run -p 3000:3000 cicd-demo
Docker Compose

docker-compose up

CI/CD Workflow

Located at .github/workflows/docker-ci-cd.yml

Set GitHub Secrets:

DOCKER_HUB_USERNAME

DOCKER_HUB_ACCESS_TOKEN

Deploy on Minikube

minikube start

kubectl apply -f deployment.yaml
minikube service cicd-service
Links

🔗 https://hub.docker.com/r/ravindranadhtagore/cicd-demo


✅ GitHub Actions builds in Actions tab

Screenshots
Add screenshots of:

GitHub Actions pipeline

Docker Hub image

Local deployment (terminal & browser)

