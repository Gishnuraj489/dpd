# 🚀 DPD Reverse Proxy with Docker Compose.

Hey there! 👋  
This is a simple project that shows how to run two backend services — one in Go and the other in Python Flask — all behind a single NGINX reverse proxy, using Docker Compose.

## 🧱 What's Inside?

Your project folder looks like this:


├── docker-compose.yml # Orchestrates all containers
├── nginx/
│ ├── nginx.conf # NGINX reverse proxy config
│ └── Dockerfile # Builds the NGINX image
├── service_1/ # Go backend service
│ ├── main.go
│ └── Dockerfile
├── service_2/ # Python Flask backend service
│ ├── app.py
│ ├── requirements.txt
│ └── Dockerfile
└── README.md

yaml
Copy code

---

## 🛠️ How to Run Everything

To get all services up and running, just run:

"docker-compose up --build"

Docker will:

Build both the Go and Python apps

Set up NGINX as a reverse proxy

Start everything with one simple command

You only need to access one port (8080) and NGINX will take care of routing to the right service.

🌐 Available Endpoints
Once everything is running, try these URLs in your browser or Postman:

Endpoint	Description

http://localhost:8080/service1/ping	Health check for Go service
http://localhost:8080/service1/hello	Hello message from Go
http://localhost:8080/service2/ping	Health check for Flask service
http://localhost:8080/service2/hello	Hello message from Flask

📌 Features
🌐 NGINX reverse proxy routes requests to the correct backend

🐳 Everything runs in Docker containers

📝 Access logs show request paths and timestamps

🛠️ No host networking — all containers use Docker's bridge network

👨‍💻 Built With
Go

Python Flask

NGINX

Docker

Docker Compose

📬 Get in Touch
If you have any questions or want to collaborate, feel free to reach out at
👉 github.com/Gishnuraj489

Happy Dockering! 🐳
