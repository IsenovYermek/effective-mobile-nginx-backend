# effective-mobile-nginx-backend

## Обзор
Простой стек: Python HTTP-сервер (backend) + Nginx (reverse proxy) в Docker.

- **Backend**: `/` → "Hello from Effective Mobile!", `/health` → "OK".
- **Nginx**: Проксирует localhost:80 → backend:8080.

## Требования
- Docker
- Docker Compose v2+

## Запуск
```bash
cd effective-mobile-nginx-backend
docker compose up -d --build
docker compose ps  # Проверить: Up (healthy)
curl http://localhost        # Hello from Effective Mobile!
