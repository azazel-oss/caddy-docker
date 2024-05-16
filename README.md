# Here is the list of all the commands required to run up this application

- `docker network create caddytest`
- `docker run --network caddytest --name caddy1 -p 8001:80 -v $PWD/index1.html:/usr/share/caddy/index.html caddy`
- `docker run --network caddytest --name caddy2 -p 8002:80 -v $PWD/index2.html:/usr/share/caddy/index.html caddy`
- `docker run -it --network caddytest docker/getting-started /bin/sh`
- `docker run --network caddytest -p 8080:80 -v $PWD/Caddyfile:/etc/caddy/Caddyfile caddy`

#### Now run your application on localhost:8080/

You can see that everytime you make a request you are visiting a webpage served by a different server
