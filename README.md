# Prerequisites

1. install docker
2. install docker-compose

# Use docker-compose to mine iron fish

Set your graffiti
```
docker run --rm -it --network host --volume $HOME/.ironfish:/root/.ironfish ghcr.io/iron-fish/ironfish:latest config:set blockGraffiti "air"
```

run services:
```
# always pull new version and run background
docker-compose pull && docker-compose up -d
```

Close services
```
docker-compose down
```

# Others

Check logs
```
docker-compose logs -f
# or
docker logs miner -f
docker logs ironfish -f
```
Check status
```
docker exec -it ironfish ./bin/run status -f
docker exec -it ironfish ./bin/run config:show
```
