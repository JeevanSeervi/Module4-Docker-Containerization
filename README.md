# Module 4 - Docker & Containerization

## Project Overview

This project demonstrates how to containerize a simple Flask web application using Docker and Docker Compose.

## Technologies Used

- Python
- Flask
- Docker
- Docker Compose

## Project Structure

```text
Module4-Docker-Containerization/
├── app.py
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
└── README.md

Docker Workflow
Source Code → Dockerfile → Docker Image → Docker Container → Docker Compose → Running Application
Docker Commands Used
Build Docker Image
docker build -t module4-flask-app .

Run Docker Container
docker run -d --name module4-container -p 5000:5000 module4-flask-app

Check Running Containers
docker ps

View Container Logs
docker logs module4-container

Run with Docker Compose
docker compose up -d

Check Compose Services
docker compose ps

Stop Compose Application
docker compose down

Application
The Flask application runs on:
http://localhost:5000

---

# Module 5 - DevOps, CI/CD & Monitoring

## Project Overview

This module extends the Dockerized Flask application by implementing a basic DevOps workflow using GitHub Actions, automated testing, Docker image building, continuous deployment, AWS EC2 deployment, and monitoring.

## DevOps Workflow

GitHub → GitHub Actions → Automated Testing → Docker Build → EC2 Deployment → Docker Container → Monitoring

## Technologies Used

- Python
- Flask
- Pytest
- Git
- GitHub
- GitHub Actions
- Docker
- AWS EC2
- Linux
- Docker Logs
- Docker Stats

## CI/CD Pipeline

The GitHub Actions workflow performs the following steps:

1. Checkout the source code from GitHub.
2. Set up Python 3.11.
3. Install project dependencies.
4. Run automated tests using Pytest.
5. Build the Docker image.
6. Connect securely to the AWS EC2 server using SSH.
7. Pull the latest code from GitHub.
8. Build the latest Docker image on EC2.
9. Stop and remove the previous container.
10. Start the updated Docker container.

## Automated Testing

A basic Flask application test was created using Pytest.

Test file:

```text
test_app.py