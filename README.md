
# Flask App with Docker & GitHub Actions CI/CD

This project is a demonstration of a simple Flask web application containerized using Docker and integrated with GitHub Actions to automate the CI/CD pipeline.

---

## 🚀 Project Overview

This repository contains:

- A basic Python Flask web server.
- Docker setup to containerize the application.
- GitHub Actions workflow to build and push the image to Docker Hub on every code push.
- Optionally, the image can be deployed to an AWS EC2 instance or any containerized environment.

---

## 🛠 Tech Stack

- **Backend**: Python 3 + Flask
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Cloud (optional)**: AWS EC2
- **Registry**: Docker Hub

---

## 📂 File Structure

```

├── app.py                 # Flask application
├── requirements.txt       # Python dependencies
├── Dockerfile             # Docker instructions
└── .github/
└── workflows/
└── main.yml       # GitHub Actions workflow

````

---

## 💻 Local Setup

```bash
# Clone the repo
git clone https://github.com/your-username/your-repo.git
cd your-repo

# Build Docker image
docker build -t flask-docker-demo .

# Run the container
docker run -d -p 5000:5000 flask-docker-demo
````

Visit `http://localhost:5000` to see the app running.

---

## 🔄 CI/CD Pipeline (GitHub Actions)

* Triggered on every push to the `main` branch.
* Logs into Docker Hub using GitHub Secrets.
* Builds the Docker image and pushes it to Docker Hub.

> Ensure the following GitHub secrets are set in your repo:
>
> * `DOCKERHUB_USERNAME`
> * `DOCKERHUB_TOKEN`

---

## 🧪 Optional Deployment (EC2)

You can run the pushed image on an EC2 instance:

```bash
docker pull your-dockerhub-username/flask-docker-demo:latest
docker run -d -p 5000:5000 your-dockerhub-username/flask-docker-demo:latest
```

Then visit `http://<EC2-PUBLIC-IP>:5000`

---

## 🔧 Future Enhancements

* Deploy to Kubernetes (EKS)
* Add testing stage to pipeline
* Integrate monitoring tools (Prometheus, Grafana)
* Error alerting & auto rollback mechanisms

---
It's me! **Benny!!!**
Feel free to connect on [LinkedIn](https://www.linkedin.com/in/benny17/) or check more projects on [GitHub](https://github.com/Benny-17)

---

