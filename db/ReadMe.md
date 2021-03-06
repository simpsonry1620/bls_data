# Setting up postgres db
https://hub.docker.com/_/postgres
Ensure the docker-compose.yml and database.env files match the configurations desired then simply run
```docker-compose up```

# Using pgAdmin in docker to manage db container
https://www.pgadmin.org/docs/pgadmin4/4.30/container_deployment.html
```
docker pull dpage/pgadmin4
docker run -p 80:80 \
    -e 'PGADMIN_DEFAULT_EMAIL=user@domain.com' \
    -e 'PGADMIN_DEFAULT_PASSWORD=SuperSecret' \
    -e 'PGADMIN_CONFIG_ENHANCED_COOKIE_PROTECTION=True' \
    -e 'PGADMIN_CONFIG_LOGIN_BANNER="Authorised users only!"' \
    -e 'PGADMIN_CONFIG_CONSOLE_LOG_LEVEL=10' \
    -d dpage/pgadmin4
 ```
