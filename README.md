Server files required to run themesong client and api repos

docker-compose.yml contains the following:
- Dynamic DNS docker container which will dynamically update the A record in cloudflare to the IP address of the machine if it changes
- Caddy container which will forward traffic in the following way:
    - themesong.io/ traffic to the themesong-client service running on 8080 from the themesong-client repo
    - api.themesong.io/ traffic to themesong-api service running on 8000 from the themesong repo
