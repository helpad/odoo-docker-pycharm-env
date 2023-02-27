# odoo-docker-pycharm-env

- ## Description

This is my Odoo environment for development using Docker and Pycharm Professional, feel free to use
it.

## Requirements
- Docker
- Docker Compose
- Pycharm Professional
- Optional: Odoo Plugin for Pycharm

## Usage

### Clone this repository
Remove the .git folder to avoid conflicts with your own git repository
``` bash
git clone https://github.com/helpad/odoo-docker-pycharm-env
rm -rf ./odoo-docker-pycharm-env/.git
```

### Build the docker image
``` bash
cd odoo-docker/dockerfiles
docker build -t odoo:dev .
cd ../..
```

### Add the db and odoo folders
``` bash
mkdir odoo-data/odoo-db
mkdir odoo-data/odoo-data
```

### Configure the pycharm project
- add remote interpreter
![img.png](images/odoo-remote-interpreter.png)
- add remote debug configuration
![img.png](images/odoo-debugger.png)

### Start the debug server
![img.png](images/debugger.png)
![img.png](images/debugger-2.png)
![img.png](images/debugger-3.png)

### Start the containers
``` bash
cd odoo-docker/odoo-dev-env
docker-compose up -d
```

### Configure postgresql datasource

![img.png](images/datasource.png)

with a demo database

![img.png](images/demo-database.png)

introspecting the database

![img.png](images/introspecting-db.png)

![img.png](images/query-console.png)
