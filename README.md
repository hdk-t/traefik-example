# TRAEFIK EXAMPLE
![Architecture diagram](https://user-images.githubusercontent.com/71418821/167065540-820399d9-e70d-4317-bd8b-51ba320153b4.png)

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
