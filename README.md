# Docker-DevOps-Workshop
Docker code though during the DevOps workshop. using Django admin working

# Creating abc docker image

```
docker build -t abc .
```
Above code will create all the dependance packages which are mentionded in <strong>requirements.txt</strong> file. Confirm if the image is created or not by using command

```
docker images
```

# Creating Docker Compose
Create docker-composite.yml file where we will be writing all our docker service and how they interacts with each other. To run each of the service which we have defined in docker-compose.yml file is given below

```
docker-compose up <service-name>
```

### Creating Docker Shell
we can create docker shell which will be used in our docker-compose.yml file (python-shell service)

```
docker-compose run <service-name> bash
```

Then we can execute the commands which we would like to execute using interact shell in our case.