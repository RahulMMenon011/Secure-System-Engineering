### Docker

For the following task refer the link 1

Create and use a Docker container interactively
Create a Dockerfile, which allows you to declaratively define your containers
Run detached containers and understand port forwarding
Use docker-compose to run a multi-container web application

For the following task 1, 2, 3 refer link 3

Task 1: Run some simple Docker containers

Task 2: Package and run a custom app using Docker

Task 3: Modify a Running Website

https://decal.ocf.berkeley.edu/archives/2018-fall/labs/a11

https://www.youtube.com/watch?v=F7We8xx1_Lw

https://training.play-with-docker.com/beginner-linux/ https://github.com/dockersamples -- this has apps for docker

### Set Up the Environment:

Install Docker Desktop:

1. Visit the Docker Desktop for Windows download page.
2. Download the Docker Desktop installer.
3. Double-click Docker Desktop Installer.exe to run the installer.
4. Follow the installation instructions.

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/a4441720-edbd-45ae-84d8-e8ab90586055)

### Verify Installation:

Open a command prompt (Windows PowerShell or Command Prompt).
Run the command: docker --version It should show client and server both installation where client is our host os command Prompt and server is Docker Engine.

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/2f96dec1-4240-4095-88ae-e36878809d4b)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/2152afb2-8a06-4983-91dd-0fb3f164c601)

Run the hello-world Image docker run hello-world

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/433137b4-56d8-43e0-bb03-61031b8effe5)

### Create and use a Docker container interactively

`docker run -it ubuntu bash`

In this command -i refers to an interactive, -t refers to the tag that needs to be pulled. ubuntu is the tag name that gets pulled, bash is the command that would be run interactively.

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/5c6cc99a-508a-4d3f-8eb1-b1add7b529dc)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/4b9c894f-26a5-4a3a-a034-71fcb2a519d3)

`docker images`

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/efbfb180-b783-42ac-931f-0d14391af06e)

### Create a Dockerfile, which allows you to declaratively define your containers

Create a file named Dockerfile in the current directory with the following contents.

FROM ubuntu:bionic

FROM ubuntu:bionic

RUN apt-get update && apt-get install -y python3.6 --no-install-recommends

CMD ["/usr/bin/python3.6", "-i"]

Build an image using the instructions written in the Dockerfile.

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/763b167c-a0f2-413a-a3e3-29dda38c88be)

Verify the created Docker Image.

`docker images`

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/37a9bc7f-da1b-4e8d-99f0-989ae5742133)

Interactively run the Docker Image and execute Python commands.

`docker run -it mypython`

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/63b8e8ed-6c28-46a9-b652-799bb109699b)

### Run detached containers and understand port forwarding

`docker run -d -p=5050:80 httpd`

The -d in the above command instructs the Docker Engine to run the container in detached mode. This will make the container to keep running until we explicitly stop it.

The httpd is the name of an image already built and available in the Docker Hub. The -p flag takes in a colon separated pair of HOST_PORT:CONTAINER_PORT.

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/69e617f4-ed88-4523-99c9-08e667a21f95)

If we check in browser it works

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/812d6458-89fb-4b9b-a0a2-805b098992b0)

### Use docker-compose to run a multi-container web application

docker compose is installed by typing the below commands in the Terminal. As windows is there as hostOS, So docker compose is available

`docker-compose version`

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/28185c22-2fdd-4e78-af66-0d313bab1b22)

A Dockerfile is written in the project directory which would contain the instructions required for the deployment of the NodeJS project.

The NodeJS project is downloaded from the provided location by typing the below commands. git clone https://github.com/0xcf/decal-sp18-a10 cd decal-sp18-a10

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/6f198ef5-e991-4fbb-aa11-a9e2ddb274e5)

We navigate back to the parent directory using the below command.

A docker-compose.yml file is written which would glue the above NodeJS container with a database container (Example: MongoDB)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/3d2d3529-ad31-4021-94d6-f0e5ec4ab78f)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/3b8361ab-be22-4465-9e70-a068d14d739b)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/30688aaa-bf6f-4d2d-8725-c826a879c22a)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/1b325a8d-422c-40b5-80c6-0d5b6a4d702e)

We open browser at http://localhost:80.

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/ca8320c1-3972-43eb-a969-59d6fbadae76)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/8a06a0c1-b6fa-4f24-b0f7-7756cd4ab400)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/0e242b02-0500-40a9-a8a9-13603d0a46bc)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/063b26b9-974a-4dc5-8874-4e83a4d6a903)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/c30efd78-38e7-4789-84c2-470000f608fd)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/ff3e6ec9-9533-497b-a51c-09ed49f8254b)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/ad281c82-de62-41db-8c56-69cf80f75bf3)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/502bd4a1-f284-4606-92ae-329c4f9dede3)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/1d5ca301-1c63-4453-8a55-0e3ea0e0766c)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/849e16d6-1f5c-4b0e-aa18-e2b62312cb63)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/22990328-be98-43c7-ab4c-15a2205d097c)

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/7a81bd47-faa5-4957-852f-42415ab9472d)



