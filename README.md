# Dockerized Flask Hello World 🌍🐳

A minimal Flask application containerized using Docker. This project is part of my learning journey into Docker, containerization, and deploying Python-based microservices.

---

## 🚀 Project Overview

This project runs a simple "Hello World" Flask app inside a Docker container. It includes basic use of `pandas` and `numpy` to simulate real-world dependencies.

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

## 📡 Docker Hub Image

🛰️ **Image Link:** [jubiii/welcome-app](https://hub.docker.com/r/jubiii/welcome-app)

Run it with:

```bash
docker pull jubiii/welcome-app
docker run -p 5000:5000 jubiii/welcome-app
```

App will be available at: [http://localhost:5000](http://localhost:5000)

---

## 💡 Future Ideas

- Add `/health` and `/status` routes  
- Include a Docker Compose setup  
- Add CI/CD pipeline using GitHub Actions  
- Unit tests for endpoints  

---

## 👨‍💻 Author

- **GitHub:** [@jubiii](https://github.com/jubiii)
- **Docker Hub:** [jubiii](https://hub.docker.com/u/jubiii)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE)
