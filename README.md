
# Netdata-Monitored Node.js App

A lightweight Dockerized Node.js web server designed for real-time performance monitoring using **Netdata**. This project demonstrates how to deploy a simple application on AWS EC2 and monitor its system and container metrics using Netdata.

> 🔗 GitHub Repo: [Santhoshreddy1818/netdata_monitoring](https://github.com/Santhoshreddy1818/netdata_monitoring)

---

## 📌 Features

- 🚀 Simple Node.js HTTP server
- 🐳 Dockerized for easy deployment
- 📊 Netdata integration for real-time system and app metrics
- 💡 Ideal for DevOps learning, system resource visualization, and container monitoring

---

## 🛠️ Tech Stack

- Node.js (v18+)
- Docker
- Netdata (monitoring tool)
- AWS EC2 (Ubuntu)

---

## 📂 Project Structure

```
netdata_monitoring/
├── app.js            # Node.js HTTP server
├── Dockerfile        # Instructions to containerize the app
├── package.json      # App metadata and script definitions
└── README.md         # Documentation
```

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Santhoshreddy1818/netdata_monitoring.git
cd netdata_monitoring
```

### 2. Build and Run the App with Docker

```bash
docker build -t netdata-node-app .
docker run -d --name node-app -p 3000:3000 netdata-node-app
```

Access the app at:  
**`http://<your-ec2-public-ip>:3000`**

---

## 📈 Monitor with Netdata

### Step 1: Launch Netdata via Docker

```bash
docker run -d \
  --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
```

### Step 2: Access the Netdata Dashboard

Open in your browser:  
**`http://<your-ec2-public-ip>:19999`**

### Step 3: Explore Metrics

- **CPU, memory, and disk usage**
- **Docker container stats (e.g. `node-app`)**
- **Live alerts and health checks**
- **Network usage per container or interface**

---

## 📷 Deliverable (for assignment)

Take a screenshot of the Netdata dashboard showing:
- System metrics (CPU, memory, disk)
- Docker container (`node-app`) metrics

---

## 👤 Author

**Santhosh Reddy**  
DevOps Engineer | Cloud Enthusiast | [GitHub Profile](https://github.com/Santhoshreddy1818)

