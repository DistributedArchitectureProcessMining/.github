# System
Information on the overall system.

## Project structure

We recommend making a folder structure similar to this.

```
├── <My_parent_folder>
    ├── Miner
    ├── Repository
    ├── ServiceRegistry
```

For simplicity, it the projects can be saved the this folders location as follows:

```
├── ProcessDryLab
    ├── Miner
    ├── Repository
    ├── ServiceRegistry
```

## Docker compose

If you have the above folder structure, the docker compose file from this project can be moved to <My_parent_folder> to do all the necessary start up steps. Top run the commands, open a terminal and navigate to <My_parent_folder> and run the commands below.

Build all images:
```
docker-compose build
```

Run all projects in seperate containers:
```
docker-compose up
```
This will also create a network and connect all containers to it, enabling communication between the projects. 

Stop all containers:
```
docker-compose down
```

Please be aware, that before you can run this compose file, you need to create and trust a development certificate for service registry. Follow the steps in the serviceRegistry README: https://github.com/ProcessDryLab-master-project/ServiceRegistry

