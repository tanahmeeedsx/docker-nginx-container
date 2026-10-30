# Docker Nginx Container

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg" alt="Nginx logo" width="120">
</p>

<p align="center">
  A simple project demonstrating how to serve a custom static HTML website with Nginx inside a Docker container.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/Nginx-Web%20Server-009639?logo=nginx&logoColor=white" alt="Nginx">
  <img src="https://img.shields.io/badge/HTML-Static%20Website-E34F26?logo=html5&logoColor=white" alt="HTML">
</p>

---

## Project Overview

This beginner-friendly project packages a custom HTML page into a Docker image and serves it through the Nginx web server. It demonstrates the basic workflow of building an image, running a container, and accessing a website through a browser.

## Technologies Used

- **Docker** – Builds and runs the application container.
- **Nginx** – Serves the static website.
- **HTML** – Provides the website content.

## Architecture

```text
index.html + Dockerfile
        |
        v
  Docker Image
        |
        v
 Docker Container
        |
        v
 Nginx Web Server
        |
        v
 http://localhost:8081
```

## Project Structure

```text
docker-nginx-container/
├── Dockerfile
├── index.html
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/tanahmeeedsx/docker-nginx-container.git
cd docker-nginx-container
```

### 2. Build the Docker Image

```bash
docker build -t nginx-html .
```

### 3. Run the Container

```bash
docker run -d --name nginx-html-container -p 8081:80 nginx-html
```

### 4. Access the Website

Open the following address in your browser:

**http://localhost:8081**

The host port `8081` is mapped to Nginx's container port `80`.

## Useful Docker Commands

| Command | Description |
| --- | --- |
| `docker images` | List available images |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker logs nginx-html-container` | View container logs |
| `docker stop nginx-html-container` | Stop the container |
| `docker start nginx-html-container` | Start the container |
| `docker rm -f nginx-html-container` | Remove the container |

## Key Learnings

- Writing a basic Dockerfile using an official Nginx image.
- Copying custom HTML content into the Nginx web root.
- Building a Docker image and running a container.
- Publishing a container port to access a website locally.

## Author

**Tanjim Ahmed**

- GitHub: [@tanahmeeedsx](https://github.com/tanahmeeedsx)

---
