# docker-compose-watchtower
Docker Compose file for watchtower



```yaml
services:
  watchtower:
    container_name: watchtower
    image: containrrr/watchtower
    restart: unless-stopped
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
    environment:
      WATCHTOWER_CLEANUP: true
      WATCHTOWER_INCLUDE_STOPPED: true
      WATCHTOWER_POLL_INTERVAL: 86400
      WATCHTOWER_REVIVE_STOPPED: true
```
