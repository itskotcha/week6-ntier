# 📋 Task Board - N-Tier Architecture (Week 6)

## 🏗️ Architecture

Browser → Nginx (HTTPS) → Node.js (API) → PostgreSQL (Data)

## 🚀 Quick Start

```bash
# Start all services
./scripts/start-all.sh

# Access
https://taskboard.local
```

## 📁 Project Structure
```
Plaintextweek6-ntier/
├── src/           # Backend source code
├── public/        # Frontend files
├── database/      # SQL scripts
├── nginx/         # Nginx config
└── scripts/       # Helper scripts
```
## 🛠️ Technologies
TierTechnologyWeb ServerNginxBackendNode.js + ExpressDatabasePostgreSQL

## 👨‍💻 Author
- **ชื่อ** : นางสาวกชพร วงศ์ใหญ่
- **รหัสประจำตัว** : 67543210067-4
- **ENGSE207 Week 6**

---

## 🛠️ แก้ปัญหาเบื้องต้น

### PostgreSQL
```
# ตรวจสอบ status
sudo systemctl status postgresql

# ดู logs
sudo tail -50 /var/log/postgresql/postgresql-*-main.log

# Reset password
sudo -u postgres psql -c "ALTER USER taskboard PASSWORD 'taskboard123';"
```

## Nginx
```
# Test config
sudo nginx -t

# ดู logs
sudo tail -f /var/log/nginx/taskboard_error.log

# Restart
sudo systemctl restart nginx
```
## Node.js
```
# ดู PM2 logs
pm2 logs taskboard-api

# Restart
pm2 restart taskboard-api

# ดู process
pm2 show taskboard-api
```
