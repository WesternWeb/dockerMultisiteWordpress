
## Multisite Wordpress Docker container exposing virtual hosts

It can be achieved by using Nginx proxy server container along with the Wordpress.

Virtual host domain names need to be entered in `/etc/hosts` file, e.g. `127.0.0.1 devwebsite.local` on host machine and specified in `docker-compose.yml` for the Wordpress container configuration: `VIRTUAL_HOST` env. variable.

Check `Dockerfile` and `docker-compose.yml` for details.

I used another 2 containers, for database and GUI db tool (Adminer), but those are entirely optional.

