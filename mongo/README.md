# MongoDB service 
## Start the service for the first time
NOTE: If you already create the network while starting an another service, you can skip the first step
1. Create the custom-network network
```
make network
```
2. Build the image 
```
make build
```
3. Run docker compose
```
make up
```

## Restart the service
```
make restart	
```
## Stop the service without deleting containers
```
make stop
```
## Stop the service and delete containers
```
make down

```
## Configure MongoDB for Florus
1. Start the MongoDB service

2. Run the following script to create the DB. The example code is for authentication service only. 
```
docker exec -it florus-mongo mongosh -u root -p root --authenticationDatabase admin /scripts/create_authen.js
```
