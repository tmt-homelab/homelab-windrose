# Windrose Deployment

GitOps deployment repository for Windrose (multi-user AI chat application).

## Stack

- **windrose**: Next.js 14 app (fork of Vane)
- **postgres**: PostgreSQL 16 database
- **redis**: Redis 7 session store
- **searxng**: SearXNG private search engine

## Deployment

All changes go through GitHub Actions:

1. Create branch: `git checkout -b feature/xyz`
2. Edit `stacks/windrose/docker-compose.yml`
3. Commit and push
4. Create PR
5. After merge, GitHub Actions deploys to dockp01

## Secrets

Managed via 1Password Connect:
- `homelab-windrose-db` - Database credentials
- `homelab-windrose-session` - Session secrets
- `homelab-windrose-searxng` - SearXNG secrets

## Access

- **URL**: https://windrose.themillertribe-int.org
- **Host**: tmtdockp01 (192.168.20.15)
- **Port**: 3000
