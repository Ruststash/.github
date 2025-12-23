# RustStash

A gaming platform with cryptocurrency integration, Steam trading, and AI-powered development tools.

## Architecture

```
                         ┌─────────────────────────────────────────────────────────────┐
                         │                    Frontend (Vue 3 + Vite)                  │
                         └───────────────────────────┬─────────────────────────────────┘
                                                     │
                         ┌───────────────────────────┴─────────────────────────────────┐
                         │                    API Server (Node.js + Socket.IO)         │
                         ├─────────────┬─────────────┬─────────────┬───────────────────┤
                         │   Workers   │  Steam Bots │   Crypto    │    AI Agents      │
                         └─────────────┴─────────────┴─────────────┴───────────────────┘
```

## Repositories

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| [api](https://github.com/ruststash/api) | Backend API & WebSocket server | Node.js, Express, Socket.IO, MySQL |
| [frontend](https://github.com/ruststash/frontend) | Web application | Vue 3, Vite, Vuetify, Pinia |
| [crypto](https://github.com/ruststash/crypto) | Cryptocurrency microservice | NestJS, TypeORM, PostgreSQL |
| [agents](https://github.com/ruststash/agents) | AI development agents | NestJS, Claude API |
| [infrastructure](https://github.com/ruststash/infrastructure) | DevOps & deployment | Docker, Kubernetes, Nginx |
| [backups](https://github.com/ruststash/backups) | Automated database backups | GitHub Actions, PostgreSQL |

## Environments

| Environment | Branch | URL |
|-------------|--------|-----|
| Production | `main` | ruststash.net |
| Staging | `staging` | staging.ruststash.net |
| Development | `dev` | dev.ruststash.net |

## Features

- **Real-time Gaming** - Jackpot, Coinflip, Crash, Roulette with live updates
- **Steam Integration** - Inventory management, automated trading, Steam authentication
- **Crypto Payments** - Multi-chain deposit/withdrawal (ETH, BTC, SOL, TRX, XRP, EOS)
- **AI Agents** - Development assistants for code navigation, security scanning, reviews

## Getting Started

See individual repository READMEs for setup instructions.

### Quick Local Setup

```bash
# Clone infrastructure
git clone https://github.com/ruststash/infrastructure.git
cd infrastructure

# Start all services
docker-compose --profile dev up
```

## Contributing

1. Fork the relevant repository
2. Create feature branch from `dev`
3. Submit pull request to `dev`
4. After review, changes merge through `staging` to `main`

## Tech Stack Overview

| Layer | Technologies |
|-------|--------------|
| Frontend | Vue 3, Vite, Vuetify 3, Pinia, Socket.IO Client |
| Backend | Node.js, Express, Socket.IO, MySQL, Redis |
| Microservices | NestJS, TypeORM, PostgreSQL, BullMQ |
| Infrastructure | Docker, Kubernetes, Nginx, Prometheus, Grafana |
| AI | Anthropic Claude API |
