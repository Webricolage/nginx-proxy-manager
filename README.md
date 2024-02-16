# Nginx Proxy Manager (NPM)

My own spin on the [Nginx Proxy Manager (NPM)](https://nginxproxymanager.com/) project.

## Changes vis-a-vis the official Docker Compose file

The container is connected to a Docker network to connect various project containers to this reverse proxy container.

PUID and PGID have been set to 0 in the environment variables as requested by one the of the projects reverse-proxied.

## Automatically restart after a system reboot

To restart the Docker container after a system reboot on a systemd system execute the following:

```sh
curl -fsSL https://techoverflow.net/scripts/create-docker-compose-service.sh | sudo bash /dev/stdin
```

More info: https://techoverflow.net/2020/10/24/create-a-systemd-service-for-your-docker-compose-project-in-10-seconds/
