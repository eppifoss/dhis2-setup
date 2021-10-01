## IN5320 - DHIS2 Installation

This repo contains a dockerfile to build DHIS2 setup container. Alternatively, you can also use the dockerhub to pull the premade container bypassing the build step. 

#### Pull DHIS2 container image from docker hub
```shell
docker pull eppifoss/dhis2-in5320
```

#### Build the docker image

```shell
docker build -t <img_name> ./
```

#### Running the container

```shell
docker run --name <name_for_docker_instance>   -v <local_volume_absolute_path>:/usr/src/app -p 3000:3000 -p 9999:9999 -it <img_name> /bin/bash
```

#### Creating bash shell for running containers

```shell
docker exec -it <name_of_docker_instance> /bin/bash
```

### Initialize your app

```shell
d2 app scripts init myfirstapp
```

### Connecting to DHIS2 instance

The following command needs to be running on a seperate terminal along side ```yarn start```

```shell
npx dhis-portal --target=https://verify.dhis2.org/in5320/
```

