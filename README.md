# Installing Uptime Kuma on a VPS

## install docker
```bash
curl -fsSL https://get.docker.com | sudo sh
```

## create the folder
create the monitoring folder and add the docker-compose.yml, loki-config.yaml and Caddyfile below

## Create a password hash for Caddy
```bash
docker run --rm caddy:2-alpine caddy hash-password --plaintext "YourSecretShipperPasswordHere"
```
Paste the generated hash in the Caddyfile

## start docker
```bash
docker compose up -d
```

## init
Configure the uptime kuma monitoring and grafana to your liking. Grafana default credentials are admin:admin