# Load Balancer

This will run an NGINX docker container which will connect `localhost:80` to website and `localhost:80/api` to API.

To build:
```
$ docker build -t db/lb .
```

To run:
```
$ docker run -p 80:80 --name db-db --rm --link db-backend:db-backend --link node-db:db-frontend db/lb
```
Please replace the former `db-backend` and `node-db` with the respective names of the docker running.