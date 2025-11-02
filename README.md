# KubernetesMicroservicesApp
🚀 Project Overview

This project demonstrates a microservices-based web application deployed on Kubernetes using Docker containers.
It includes a React frontend, Flask backend, and Redis for caching.

🧩 Tech Stack

Frontend: React

Backend: Flask (Python)

Cache: Redis

Containerization: Docker

Orchestration: Kubernetes (Minikube)

⚙️ Steps to Run the Project

Build Docker Images

docker build -t flask-backend:latest ./backend
docker build -t react-frontend:latest ./frontend

Start Minikube

minikube start

Load Images into Minikube

minikube image load flask-backend:latest
minikube image load react-frontend:latest

Deploy All Services

kubectl apply -f redis-deployment.yaml
kubectl apply -f backend-deployment.yaml
kubectl apply -f frontend-deployment.yaml

Access the App

minikube service frontend-service
✅ Features

Simple communication between frontend and backend.

Backend visit count stored in Redis.

Containerized and deployed on a local Kubernetes cluster.

📦 Tools Used

Docker, Kubernetes, Minikube, Flask, React, Redis

💡 Future Improvements

Add CI/CD pipeline for automated builds and deployments.

Integrate database for persistent data storage.

Author: sid-2812

Learning Goal: Understanding end-to-end microservices deployment on Kubernetes.
