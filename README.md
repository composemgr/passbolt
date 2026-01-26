## 👋 Welcome to passbolt 🚀

Open-source password manager for teams

## 📋 Description

Open-source password manager for teams

## 🚀 Services

- **app**: passbolt/passbolt:latest-ce

### Infrastructure Components

- **db**: Mariadb database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/passbolt/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/passbolt" ~/.local/srv/docker/passbolt
cd ~/.local/srv/docker/passbolt
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install passbolt
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
DB_CREATE_DATABASE_NAME=passbolt
DB_USER_NAME=passboltuser
DB_USER_PASS=changeme_db_password
EMAIL_SERVER_PORT=587
EMAIL_SERVER_HOST=172.17.0.1
EMAIL_SERVER_MAIL_FROM=no-reply@${BASE_DOMAIN_NAME:-${BASE_HOST_NAME
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:60236

## 📂 Volumes

- `./rootfs/data/passbolt/gpg` - Data storage
- `./rootfs/data/passbolt/jwt` - Data storage
- `./rootfs/data/db/mariadb/passbolt` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
