Overview
---------

Project will create (in docker)

* A single MarkLogic node

Admin account is
* Username: admin
* Password: admin

Prerequisites
-------------

1. docker toolkit installed
2. Java 8 installed
3. Following ports available -
* 8000-8050


Installation steps (once off)
-----------------------------

1. Download MarkLogic-9.0-5.x86_64.rpm (or any other MarkLogic v9 rpm) and copy it to src/main/docker/marklogic
2. Execute (this will download all required docker dependencies to build marklogic image) 
  * for a ml10 node
```
    docker-compose -f docker-compose.v10.yml build   
```
  * for a ml9 node
```
    docker-compose -f docker-compose.v9.yml build   
```
3. Execute (this will download all required gradle dependencies)
```
    ./gradlew build 
```

Server Setup for MarkLogic V9
-------------
1. ./gradlew mlDockerSetupNode -PenvironmentName=v9

Server Start for MarkLogic V9
-------------
1. ./gradlew mlDockerStart -PenvironmentName=v9

Server Stop for MarkLogic V9
-------------
1. ./gradlew mlDockerStop -PenvironmentName=v9

Server TearDown for MarkLogic V9
-------------
1. ./gradlew mlDockerTeardown -PenvironmentName=v9


Server Setup for MarkLogic V10
-------------
1. ./gradlew mlDockerSetupNode -PenvironmentName=v10

Server Start for MarkLogic V10
-------------
1. ./gradlew mlDockerStart -PenviornmentName=v10

Server Stop for MarkLogic V10
-------------
1. ./gradlew mlDockerStop -PenviornmentName=v10

Server TearDown for MarkLogic V10
-------------
1. ./gradlew mlDockerTeardown -PenviornmentName=v10

