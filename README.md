in docker-compose.yml

version: "3.7"
services:
  <write service name>:
    build: ./contents
    container_name: <write container_name>
    environment:
      - JUPYTER_ENABLE_LAB=yes
    ports:
      - "8888:8888"
    volumes:
      - .:/home/jovyan/work
    command: start.sh jupyter lab --NotebookApp.token=''