# Digdag
Digdag with docker

## Requirements
- docker
- docker-compose

## Enabled extra operators
- rb>
- py>

## Getting started
```bash
 # server mode
docker-compose up

# log in to digdag container
docker-compose exec digdag bash

# create and run workflow with python template
digdag init -t python ${PROJECT_NAME}
cd ${PROJECT_NAME} && digdag run ${PROJECT_NAME}.dig

# stop
docker-compose down
```

## GUI
http://localhost:65432/
