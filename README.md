# Dockerized Example Voting App 🚀

A multi-container Voting Application deployed using Docker Compose on AWS EC2.  
This project demonstrates containerization, service orchestration, and cloud deployment using DevOps best practices.

---

## 📌 Project Overview

This application allows users to vote between two options.  
Votes are stored in PostgreSQL, processed by a worker service, and displayed in real-time results.

The system is fully containerized and deployed on an Ubuntu-based AWS EC2 instance using Docker Compose.

---

## 🏗 Architecture

The application consists of the following services:

- **Vote Service** – Frontend voting interface
- **Result Service** – Displays live voting results
- **Worker Service** – Processes votes from Redis and stores in PostgreSQL
- **Redis** – In-memory data store / message broker
- **PostgreSQL** – Persistent database

---

## ⚙️ Technologies Used

- Docker
- Docker Compose
- AWS EC2 (Ubuntu)
- Redis
- PostgreSQL
- Linux CLI
- Git & GitHub
- Docker Hub

---

## 🔌 Application Ports

| Service        | Port  |
|---------------|-------|
| Vote App      | 8080  |
| Result App    | 8081  |
| Redis         | 6379  |
| PostgreSQL    | 5432  |

---

## 🚀 Deployment Steps (AWS EC2)

1. Launch Ubuntu EC2 instance
2. Install Docker
3. Install Docker Compose
4. Clone project repository
5. Run:

```bash
docker compose up -d
```

6. Configure EC2 Security Group:
   - Allow ports **8080 and 8081** (Custom TCP)
   - Allow SSH (22)

7. Access application via:

```
http://<EC2-Public-IP>:8080
http://<EC2-Public-IP>:8081
```

---

## 🛠 Troubleshooting Performed

- Fixed YAML syntax errors in `docker-compose.yml`
- Resolved Docker image pull errors
- Verified container logs using:
  ```bash
  docker logs <container_name>
  ```
- Checked running containers:
  ```bash
  docker ps
  ```
- Validated exposed ports and AWS Security Group rules
- Ensured Redis and PostgreSQL containers were healthy

---

## 📦 Docker Images

Application images were built and pushed to Docker Hub for deployment.

---

## 📊 Key DevOps Learnings

- Multi-container application deployment
- Docker networking between services
- Port mapping and security group configuration
- Container health checks
- Image management with Docker Hub
- Cloud deployment on AWS EC2

---

## 👨‍💻 Author

**Riyaz Khan**  
Aspiring DevOps Engineer | AWS | Docker | Cloud Deployment

---

⭐ If you found this project helpful, feel free to star the repository!
