# Homeserver

My home server defined with infrastructure-as-code

I run these apps on my Raspberry Pi 4 8GB with the 64 bit Debian image cloned to an SATA SSD connected via an USB adapter. Ansible is used for configuration and deployment.

---

`.env` files needs to be created with values:
```
TIMEZONE=America/New_York
UID=1000
GID=1000
BASE_DOMAIN=example.com
```

Initial set up: `bootstrap-playbook.yml`

Docker containers deployment: `docker-playbook.yml`

Persistent data is stored in `/docker`

## TO-DO's
- Persistent data backup
- Proper secrets storage instead of omitted `.env` files that contains secrets
- Proper TLS with Traefik
- Generated docker-compose files through Ansible templates for more simplicity