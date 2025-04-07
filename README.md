# Dockerized Flask Hello World 🌍🐳

A minimal Flask application containerized using Docker. This project is part of my learning journey into Docker, containerization, and deploying Python-based microservices.

---

## 🚀 Project Overview

This project runs a simple "Hello World" Flask app inside a Docker container. It's a minimal example focused on learning Docker with Python web applications, using only Flask as a dependency.

---

## 📁 Project Structure

```
.
├── app.py               # Flask application
├── Dockerfile           # Docker image instructions
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
```

---

## 🐍 Files

- **`app.py`** – A simple Flask app that returns "Hello World" on the root endpoint.
- **`Dockerfile`** – Instructions to containerize the app using Python 3.7.
- **`requirements.txt`** – Lists Python dependencies: Flask, pandas, and numpy.

---

## 🐳 Docker Workflow

Below are the Docker commands used during the project:

```bash
# Build the image
docker build -t welcome-app .

# Run the container
docker run -p 5000:5000 welcome-app

# Stop container
docker ps
docker stop <container_id>

# Clean and rebuild for Docker Hub
docker image rm -f welcome-app
docker build -t jubiii/welcome-app .

# Push to Docker Hub
docker login
docker push jubiii/welcome-app:latest

# Pull and run (from anywhere)
docker pull jubiii/welcome-app:latest
docker run -p 5000:5000 jubiii/welcome-app
```

---

## 📡 Docker Hub Link

🛰️ **Link:** [jubiii/welcome-app](https://hub.docker.com/repository/docker/jubiii/welcome-app/general)

Run it with:

```bash
docker pull jubiii/welcome-app
docker run -p 5000:5000 jubiii/welcome-app
```

---

## ✅ Conclusion

This project served as a foundational step into the world of Docker and containerized Python applications. By creating a minimal Flask app, building a Docker image, and pushing it to Docker Hub, it showcases the complete lifecycle of containerizing and deploying a microservice. 

This setup lays the groundwork for scaling into more complex systems involving APIs, databases, and orchestration tools like Docker Compose and Kubernetes.

