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
Create <strong>docker-composite.yml</strong> file where we will be writing all our docker service and how they interacts with each other. To run each of the service which we have defined in docker-compose.yml file is given below

```
docker-compose up <service-name>
```

### Creating Docker Shell
we can create docker shell which will be used in our docker-compose.yml file (python-shell service)

```
docker-compose run <service-name> bash
```

Then we can execute the commands which we would like to execute using interact shell in our case.

# To execute
Inside docker development shell(python-shell service) execute following codes.

1. To create migration to the tables(check <em>database/models.py</em> and changes in <em>testing/settings.py</em> database part) 
``` 
python manage.py makemigrations

python manage.py migrate
```
2. To run the server in our case django server In our case. Come out of the Docker container and execute it, this can be done by
```
docker-compose up python-server
```