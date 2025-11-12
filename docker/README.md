# Docker Compose Stacks

Production-ready Docker Compose configurations for various services.

## Available Stacks

### nginx + PostgreSQL
**File**: `nginx-postgres-stack.yml`

Simple web server with PostgreSQL database backend.
```bash
docker compose -f nginx-postgres-stack.yml up -d
```

Access: http://192.168.1.194:8081

### WordPress + MySQL
**File**: `wordpress-stack.yml`

Full WordPress CMS with MySQL database.
```bash
docker compose -f wordpress-stack.yml up -d
```

Access: http://192.168.1.194:8082

## Management Commands
```bash
# Start a stack
docker compose -f <stack-file> up -d

# Stop a stack
docker compose -f <stack-file> down

# View logs
docker compose -f <stack-file> logs -f

# Check status
docker compose -f <stack-file> ps

# Restart services
docker compose -f <stack-file> restart
```

## Cleanup
```bash
# Stop and remove containers + volumes
docker compose -f <stack-file> down -v

# Remove all unused containers, networks, images
docker system prune -a
```
