# Create directory
mkdir compose
cd compose/

# docker compose command
````
docker compose
````
# Clone source code of Emart App
````
git clone https://github.com/devopshydclub/emartapp.git
cd emartapp/
````

# Bring up all the containers
````
docker compose up -d
docker compose ps
ip addr show | grep inet
docker compose down
docker stop $(docker ps -a --format '{{.Names}}')
docker rm  $(docker ps -a --format '{{.ID}}' )
docker rmi $(docker images --format '{{.ID}}')
````
Go to browser and enter VMIP:80

# Clean up
````
docker compose down
docker system prune -a
exit
````