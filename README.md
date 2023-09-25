````yaml
################################################################################################
# Docker
################################################################################################
COMPOSE_PROJECT_NAME=visualboost

AUTH_MONGO_CONTAINER_NAME=mongoauth
MAIN_MONGO_CONTAINER_NAME=mongomain
BUILD_MONGO_CONTAINER_NAME=mongobuild

AUTH_APP_CONTAINER_NAME=visualboost_auth
MAIN_APP_CONTAINER_NAME=visualboost_main
BUILD_APP_CONTAINER_NAME=visualboost_build

################################################################################################
# Database
################################################################################################

COMPOSE_PROJECT_NAME=visualboost_auth

### Mongo-DB - User & DB ########################################################################
# User-Name of Mongo-DB with admin rights
MONGO_ADMIN=Admin

# Password of Mongo-DB Admin
MONGO_ADMIN_PW=PW_ADMIN

# Name of the database
MONGO_DB_NAME=db

# The User-Name with Read- & Write-Access (but no root) that will access that Mongo-DB.
MONGO_USER=User

# The password of the MONGO_USER.
MONGO_USER_PW=PW_USER

# Domains and ports of mongodb
MONGO_URL_AUTH=mongoauth
MONGO_PORT_AUTH=40001

MONGO_URL_MAIN=mongoauth
MONGO_PORT_MAIN=40011

MONGO_URL_BUILD=mongoauth
MONGO_PORT_BUILD=40021

# The volume where the db is located (outside of the Docker-Container).
MONGO_DATA_DIR_AUTH=./data/auth
MONGO_DATA_DIR_BUILD=./data/build
MONGO_DATA_DIR_MAIN=./data/main

### Applications ########################################################################
HTTP_PORT_AUTH=40000
HTTP_PORT_BUILD=40010
HTTP_PORT_MAIN=40020
HTTP_PORT_FRONTEND=44444

DOMAIN=localhost

### Secrets ########################################################################
JWT_SECRET=<YOUR_SECRET_KEY>

### Network ########################################################################
NETWORK_AUTH=visual_boost_auth_network
NETWORK_MAIN=visual_boost_main_network
NETWORK_BUILD=visual_boost_build_network
````
