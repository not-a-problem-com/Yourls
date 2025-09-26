# Yourls
Docker image and Compose used in 'When links necessitate amputation'

### Dockerfile
Custom image file for Yourls that adds PHP extensions and pre-installs some plugins to the image. If you do not build the dockerfile using `docker compose build` prior to running the compose it should build automatically.

#### Issues

1. It will not override existing configuration or update plugins if the volume contains the install location.

### Compose
Includes Cloudflared tunnel for external access and mysql DB for Yourls. 

Cloudflared will only start if `COMPOSE_PROFILES=cloudflared` is passed as an environmental variable when it starts.

#### ENV
Please see .env.example for available env variables. More variables exist then are present in the example but these are mostly needed for running.