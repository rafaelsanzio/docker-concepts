- _Creating and running a container from an image_
  $ docker run <image name>

<!-- Exemple: -->

$ docker run hello-world

- _Command to overwrite_
  $ docker run <image name> <command>

<!-- Exemple: -->

$ docker run busybox echo hi there

- _List all running containers_
  $ docker ps
- _List all containers that you have created_
  $ docker ps --all

$ docker run = docker create + docker start

<!-- Exemple create a container -->

$ docker create hello-world

<!-- Exemple start a container -->

$ docker create <image name>
$ docker start -a <container id>

- _Removing some files of stopped containers_
  $ docker system prune

- _Get logs from a container_
  $ docker logs <container id>

- _Stopping container_
  $ docker stop <container id> <!-- SIGTERM -->
  $ docker kill <container id> <!-- SIGKILL -->

- _Execute an additional command in a container_
  $ docker exec -it <container id> <command>

<!-- Example -->

    $ docker exec -it some_id redis_cli

-i -> reach STDIN in command
-t -> formating to see better at screen

- _Access to terminal (shell, zsh, sh) inside container_
  $ docker exec -it <container id> sh

- _docker volume_
  $ docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image_id>
