# 🐳 AI Automation Infrastructure Roadmap

<p align="center">
  <a href="https://www.docker.com/">
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  </a>
  <a href="https://www.postgresql.org/">
    <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  </a>
  <a href="https://www.linux.org/">
    <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux"/>
  </a>
  <a href="https://n8n.io/">
    <img src="https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/>
  </a>
</p>

<h2>
  **A hands-on learning journey focused on building reliable infrastructure for AI automation, AI agents, and n8n workflows. Covering Docker, PostgreSQL, Linux, containerization, persistent storage, and deployment.**
</h2>

<h2>**Hands-on roadmap for AI Automation infrastructure.**</h2>

---

## 🎯 Roadmap

| Phase | Topic                         | Status         |
| ----- | ----------------------------- | -------------- |
| 01    | 🐳 Docker Fundamentals        | 🟡 In Progress |
| 02    | 🧩 Docker Compose             | ⬜ Planned      |
| 03    | 🗄️ PostgreSQL                | ⬜ Planned      |
| 04    | 🐧 Linux Fundamentals         | ⬜ Planned      |
| 05    | 🔌 n8n + PostgreSQL           | ⬜ Planned      |
| 06    | 🔐 Security & Troubleshooting | ⬜ Planned      |
| 07    | 🚀 Deployment                 | ⬜ Planned      |

---

## 🐳 01 — Docker Fundamentals

### Core Concepts

| Concept               | Role                      |
| --------------------- | ------------------------- |
| Image                 | Application template      |
| Container             | Running instance          |
| Volume                | Persistent data           |
| Port                  | Network access            |
| Network               | Container communication   |
| Environment Variables | Application configuration |

### Commands

**List images**

```powershell
docker images
```

**Create a container**

```powershell
docker run -d --name my-container nginx
```

**List containers**

```powershell
docker ps -a
```

**Create a volume**

```powershell
docker volume create my_volume
```

**Run n8n with persistent storage**

```powershell
docker run -d --name my-n8n -p 5680:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n:2.32.7
```

---

## 🧩 02 — Docker Compose

### Commands

```powershell
docker compose up -d
docker compose ps
docker compose logs -f
docker compose down
```

### Topics

* YAML configuration
* Services and dependencies
* Networks and volumes
* Environment variables

---

## 🗄️ 03 — PostgreSQL

### SQL Fundamentals

**Create a table**

```sql
CREATE TABLE customers (
    id SERIAL PRIMARY KEY,
    name TEXT NOT NULL,
    email TEXT UNIQUE
);
```

**Insert data**

```sql
INSERT INTO customers (name, email)
VALUES ('Abderrahmane', 'example@email.com');
```

**Read data**

```sql
SELECT * FROM customers;
```

**Update data**

```sql
UPDATE customers
SET name = 'New Name'
WHERE id = 1;
```

**Delete data**

```sql
DELETE FROM customers
WHERE id = 1;
```

### Topics

| Topic                  | Status |
| ---------------------- | ------ |
| Databases & Tables     | ⬜      |
| CRUD Operations        | ⬜      |
| Primary & Foreign Keys | ⬜      |
| JOIN Queries           | ⬜      |
| Indexes & Backups      | ⬜      |

---

## 🐧 04 — Linux Fundamentals

### Commands

**Navigation**

```bash
pwd
ls -la
cd /path/to/directory
```

**Files and directories**

```bash
mkdir project
touch notes.txt
cp notes.txt backup.txt
mv notes.txt renamed.txt
```

**Processes and resources**

```bash
ps aux
top
df -h
free -h
```

**Networking and logs**

```bash
ss -tulpn
journalctl -u docker
```

### Topics

* Files and directories
* Permissions and ownership
* Processes and services
* Networking and ports
* SSH and server administration

---

## 🔌 05 — n8n + PostgreSQL

```text
Webhook
   ↓
n8n Workflow
   ↓
Data Validation
   ↓
PostgreSQL
   ↓
Response
```

* Configure PostgreSQL credentials.
* Connect containers through a Docker network.
* Execute SQL queries from n8n.
* Store and retrieve workflow data.
* Handle errors and duplicate records.

---

## 🔐 06 — Security & Troubleshooting

```powershell
docker logs my-container
docker inspect my-container
docker network ls
docker volume ls
docker stats
```

* Protect credentials and API keys.
* Keep `.env` files out of Git.
* Separate application volumes.
* Back up important data.
* Inspect logs before troubleshooting.

---

## 🚀 07 — Final Project

| Component      | Purpose               |
| -------------- | --------------------- |
| Docker         | Containerization      |
| Docker Compose | Service orchestration |
| n8n            | Workflow automation   |
| PostgreSQL     | Data storage          |
| Linux          | Server management     |
| Volumes        | Persistent storage    |

---

## 📈 Progress

* [ ] Docker Images & Containers
* [ ] Volumes & Port Mapping
* [ ] Docker Compose
* [ ] PostgreSQL & SQL
* [ ] Linux Commands
* [ ] n8n Database Integration
* [ ] Security & Backups
* [ ] Linux Server Deployment

---

**🚀 Learn by building, testing, and documenting real projects.**
