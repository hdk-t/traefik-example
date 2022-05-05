# TRAEFIK EXAMPLE
Example of load balancing and proxy using traefik container
## SET UP
### Create network
    docker network create traefik_example_network  
### Starting traefik
    docker-compose -f ./gateway/docker-compose.yml up -d  
### Starting web servers
    docker-compose -f ./web/docker-compose.yml up -d
### Access traefik dashboard
[traefik dashboard](http://traefik.localhost)
### Access nginx
[nginx](http://localhost/nginx)
### Access apache
[apache](http://localhost/apache)
### Scale up nginx to 3
    docker-compose -f ./web/docker-compose.yml scale nginx=3
