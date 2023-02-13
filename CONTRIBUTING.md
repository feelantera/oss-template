# Contributor Guideline

## 🏁 Quick Start

### Prerequisites

At least you will need `PostgreSQL >=14` and optionally `Docker >= 20.10` for building the container.

### Generate Secret Key

Before you continue, you need to create `.env` file (you can duplicate `.env.example`) and
fill the `application secret key` with some random string. To generate a secret key, use
the following command:

```sh
openssl rand -base64 500 | tr -dc 'a-zA-Z0-9' | fold -w 32 | head -n 1
```

### Up and Running

_TODO_

## 📦 Docker Container

```sh
# Build the container
docker build -t :latest -t IMAGE_NAME:v0.1.0 .

# Running the container
docker run --rm -it --name CONTAINER_NAME -p 3000:3000 --env-file .env IMAGE_NAME:latest

# Entering container shell
docker run --rm -it --entrypoint sh IMAGE_NAME:latest
```
