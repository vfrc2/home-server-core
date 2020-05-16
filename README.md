# Server config

## Prerequisites

SERVER_HOST_NAME - root host name
SERVER_CERTS_PATH - path to server certs
SERVER_VHOSTD_PATH - path which contains nginx vhost configs 
SERVER_BACKUP_PATH - path to server backup folder
SERVER_DOCKER_NETWORK - name of docker network
SERVER_DOCKER_WIKI_VOLUME - name of wiki volume

Create network if not exists:
```
docker network create ${SERVER_DOCKER_NETWORK}
```

# System
- portainer
- jwilder/nginx-proxy  SERVER_VHOSTD, SECRETS: root.cert, wildcard.server.cert
- bitnami/dokuwiki     SERVER_WIKI_DATA? backup

# Stats
- grafana/grafana      VIRTUAL_HOST: graphana.server.pyt.lan backup
- influxdb             

# Download manager
- devonkupiec/flexget
- hurlenko/aria2-ariang

# Media
- jellyfin/jellyfin:10.5.2
- Plex Proxy?

# IOT

- mqtt
- zigbee2mqtt
- mosqutio
- node red
