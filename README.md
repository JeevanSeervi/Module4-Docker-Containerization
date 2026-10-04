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