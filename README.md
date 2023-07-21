# kong-config-api-gateway
Config Kong API Gateway : services,routes,plugins,ports,env,...

Adjust Config Kong :ports,env,... in file kong-compose.yml
````text
   adjust kong-compose.yml
````

Adjust Kong API Gateway:services,routes,consumer,... in file kong.yml
````text
   adjust /compose/kong/config/kong.yml
````

Create docker a network
````sh
    docker network create kong-net
````

Run Kong API Gateway
```sh
 docker-compose -f kong-compose.yml up -d --build
```

Clean up containers
````sh
    docker kill kong-container
    docker container rm kong-container
    docker network rm kong-net
````