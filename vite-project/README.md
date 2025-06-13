# Docker Compose

What is Docker Compose?

Docker Compose is a tool for defining and running multi-container Docker applications. With Docker Compose, you define a multi-container application in a single file, then spin your application up in a single command which does everything that needs to be done to get it running.

Docker Compose is a powerful tool that allows you to define and run complex applications with ease. It simplifies the process of managing multiple containers and their dependencies, making it easier to deploy and scale your applications.

# Command line for Docker Compose

docker-compose up

docker-compose down

docker-compose watch

docker-compose build

docker-compose run web

docker-compose run web npm run dev

docker-compose run web npm run build

docker-compose run web npm run lint

# for mac simply use - sudo docker-compose up

# Docker Watch
- Sync , Rebuild and Restart


# Docker Compose File

version: "3.9"

services:
  web:
    build:
      context: .
    
    ports:
      - 5173:5173
    volumes:
      - .:/app
      - /app/node_modules         

