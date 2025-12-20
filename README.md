# Flask + MySQL Two-Tier Application (Dockerized)

A **production-style two-tier application** built using **Flask** and **MySQL**, containerized with **Docker** and orchestrated using **Docker Compose**.

This project is designed specifically to demonstrate **Cloud & DevOps fundamentals** such as containerization, service dependency handling, environment-based configuration, and clean system design.

---

## 🎯 Project Goal (For Recruiters)


The goal of this project is to showcase my ability to:

- Build and containerize real applications
- Design clean and deployable system architectures
- Use Docker and Docker Compose correctly
- Manage configuration using environment variables
- Understand service startup order and healthchecks
---

## 🏗️ Architecture Overview

**Two-Tier Architecture**

1. **Application Tier**
   - Python Flask backend
   - Handles HTTP requests and database operations
   - Runs inside a Docker container

2. **Database Tier**
   - MySQL 5.7
   - Persistent storage using Docker volumes

Both services communicate over a **Docker bridge network** using service names instead of IPs.

---

## 🧰 Tech Stack

- **Backend**: Python (Flask)
- **Database**: MySQL 5.7
- **Containerization**: Docker
- **Orchestration**: Docker Compose
- **Configuration**: Environment Variables (`.env` files)
- **OS Compatibility**: Linux / Windows / macOS

---

## 📁 Repository Structure

```
├── Dockerfile
├── docker-compose.yml
├── app.py
├── requirements.txt
├── flask.env
├── mysql.env
├── message.sql
└── templates/
    └── index.html
```

**Why this structure?**
- No unused files
- Every file is actively used at runtime
- Clear separation of concerns

---

## 🧠 Key DevOps Improvements

### 1️⃣ Cleaned Repository Scope
- Removed Jenkinsfile, Makefile, Kubernetes manifests
- These were not part of the active deployment flow

---

### 2️⃣ Optimized Docker Image Design
- Single Dockerfile
- Dependencies installed in `/app/deps`
- Explicit `PYTHONPATH` usage

**Impact**
- Faster builds
- Isolated dependencies
- Easier debugging
---

### 3️⃣ Environment-Based Configuration
- Application and database configs moved to `.env` files
- No hardcoded credentials in code

**Impact**
- Secure configuration handling
- Easy environment switching (local / cloud)
- Industry best practice
---

### 4️⃣ Reliable Service Startup
- MySQL healthcheck implemented
- Flask starts only after database is healthy

**Impact**
- Stable container startup
- Production-aligned behavior

---

### 5️⃣ UI for Observability
The frontend is **not a product UI**.

Its purpose:
- Show real-time database writes
- Visualize backend availability
- Help during demos.

This makes system behavior visible without checking logs.

---

## 🔐 Environment Configuration

### `mysql.env`

``` 
MYSQL_ROOT_PASSWORD=your_root_password
MYSQL_USER=your_username
MYSQL_PASSWORD=your_password
MYSQL_DATABASE=your_database
```


### `flask.env`
```
MYSQL_HOST=mysql
MYSQL_USER=your_username
MYSQL_PASSWORD=your_password
MYSQL_DB=your_database
```
---

## 🚀 How to Run the Project

### Prerequisites
- Docker
- Docker Compose

### Start the Application
```bash
docker compose up
```
## 🌐 Access

- **Application**: http://localhost
---

## 🧪 What This Project Proves

This project demonstrates:

- Understanding of Docker containers  
- Practical Docker Compose usage  
- Service dependency management  
- Environment variable handling  
- Clean repository design
---

## 🔮 Future Enhancements (Planned)

- CI/CD pipeline using Jenkins  
- Cloud deployment (AWS / OCI)  
- Monitoring and logging  
- Secure secrets management  

These are intentionally excluded for now to keep the project focused and readable.

---

## 👤 Author

**SHIVAM BHARDWAJ**  
Aspiring Cloud / DevOps Engineer  
Networking • Linux • Git • GitHub • Docker • AWS 
