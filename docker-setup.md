---
title: "Docker Setup"
layout: single
classes: wide
---

In order for your homeworks to be graded, they must run on the docker, which will have the same environment as our teaching servers. We will use the docker image from CSE113 (Winter 2022) for this class. This is an introduction to setting up docker. Please let us know if you have other references that you think could be useful!

**The docker has a very simple Ubuntu OS. If you use a linux/MacOS/WSL environment then it will likely work. However, please double check that code works on the docker imagine just to be sure. If it does not run, then it can't be graded.**

**Please make sure you understand the storage model of Docker as not all storage is persistant! It is always a good idea to back up your work in progress, e.g., using git. But please don't make your homework git repos public!**

_This write up has been contributed to by several students: Reese Levine, Yanwen Xu, Neal Chokshi, and Jessica Dagostini; please let me know if you have any other suggestions!_

------

## Install Docker

### Installing on Linux/Ubuntu

First, update the repository database

`sudo apt-get update`

Now we must add the official Docker repository key:

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`

And we must add the repository to the APT source

`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`

Update the repository database again, now with the Docker one added

`sudo apt-get update`

And install Docker

`sudo apt-get install docker-ce`

Once the installation is complete, to check if the installation was carried out correctly:

`sudo docker version`

### Installing on Mac

Download the Docker installer:

**For Mac with Apple chip** - [https://desktop.docker.com/mac/main/arm64/131620/Docker.dmg](https://desktop.docker.com/mac/main/arm64/131620/Docker.dmg?_gl=1*bju9bi*_ga*MjQ5NjY5NTU2LjE3MDQ4NjcyOTk.*_ga_XJWPQMJYHQ*MTcwNTA4MjQ1NC40LjEuMTcwNTA4MjUxNS42MC4wLjA.)

**For Mac with Intel chip** [https://desktop.docker.com/mac/main/amd64/131620/Docker.dmg](https://desktop.docker.com/mac/main/amd64/131620/Docker.dmg?_gl=1*1lackbt*_ga*MjQ5NjY5NTU2LjE3MDQ4NjcyOTk.*_ga_XJWPQMJYHQ*MTcwNTA4MjQ1NC40LjEuMTcwNTA4MjUxNS42MC4wLjA.)

Double-click `Docker.dmg` to open the installer, then drag the Docker icon to the Applications folder.

Double-click `Docker.app` in the Applications folder to start Docker.

The first screen select **Accept** to continue.

Select the **Use recommended settings (Requires password)** installation option.

Finally, press **Finished**.

### Installing on Windows
**IMPORTANT**

Before installing Docker, make sure that you have the Hyper-V virtualization enabled in your BIOS.

**For Windows 10 Pro, Enterprise, and Education**

Download the Docker installer: [https://desktop.docker.com/win/main/amd64/131620/Docker%20Desktop%20Installer.exe](https://desktop.docker.com/win/main/amd64/131620/Docker%20Desktop%20Installer.exe?_gl=1*1qns7iy*_ga*MjQ5NjY5NTU2LjE3MDQ4NjcyOTk.*_ga_XJWPQMJYHQ*MTcwNTA4MjQ1NC40LjEuMTcwNTA4MjUxNS42MC4wLjA).

Run the installer, following the steps indicated by it.

When prompted, ensure the **Use WSL 2 instead of Hyper-V** option on the Configuration page is selected or not depending on your choice of backend.

If your system only supports one of the two options, you will not be able to select which backend to use.

Once the installation is complete, open a terminal of your choice and run the command below to verify the installation.

`docker --version`

When Docker is active on the system, a ''whale'' will be shown in the status bar on the right, in the main menu.

**For Windows 10 Home**

Since Windows 10 Home does not support Hyper-V, we need to download Docker Toolbox: https://download.docker.com/win/stable/DockerToolbox.exe

Run the downloaded file as administrator.

Follow the installer's steps, installing the points recommended by him.

Once the installation is complete, look for Docker Quickstart Terminal

## Testing Installation + Docker Commands
After finishing installation, you are now able to run a container in your PC! To do that, follow the next steps

Open a terminal and type `docker run -it --rm hello-world`. You should see an output like this:


In the previous command we created and started a container instance from the image `hello-world`(which is a default test from docker community) with the `docker run` command, we attached it to our host terminal (with the `-it` option) and set to automatically delete when we exited (with the `--rm` option).

Every time you start a docker container, if you do not define the `--rm` option when launching it, the container will be kind of running until you use another command to remove it definetelly. To see if you have any container created and running (or not), you can type `docker ps -a` in your terminal. To clean all containers that are there, you can type `docker container prune`. It will delete all instances listed with the ps command.

`docker pull` also downloads the specified container, which in this case is `reeselevine/cse113:latest`, where `reeselevine/cse113` is the image name and `latest` is the tag. Docker allows multiple tags for the same image, but for this course we will most likely only be using the default latest tag for images.

`docker start` lets you start a container that has already been created

`-v` mounts a volume from the host (your computer) to the docker container. We will be mounting the current host machine directory to the directory `/assignments` inside the container.

`-it` gives us an interactive, terminal based session. Without this, the container would immediately exit.

Each `docker run` creates a new container, and it will stop when you exit. Do not create a new container each time you want to work on your project. Using `docker run` for the initial setup and then exiting and calling `docker start` whenever you want to resume development is the recommended workflow. Having a bunch of Docker containers can take a lot of space, fast. Some time it is useful to prune all stopped containers, and you can do it by running `docker container prune` to gain some space.

Follow instructions [here](https://docs.docker.com/get-docker/). The destop version is recommended. The following instructions outline how to use docker primarily through the CLI, but the desktop app provides the same functionality and may be easier to use.

## Download the Container
After Insalling Docker, run the following command:

`docker pull reeselevine/cse113:latest`

When running, the container includes everything necessary for the homework to work correctly, namely python3, C++ compilers, and make. It also includes two text editors, vim and emacs. If you’d like another text editor included in the image, please let us know.

## Development
We will be usnig Github Classroom for the controle, storage and evaluation of your homeworks at this class. If you are seeing this repository, this means that you already have access to the classroom. Each homework will follow the same procedure:
1. You will receive an invite to join a new assignment
2. Once accepted, Github Classroom will automatically create a fork from the template repository for that homework
3. Clone your repository to your local computer using `git clone <link-for-your-repo>`
4. This repository is only yours and all your edits and tries should be pushed to it
5. After you finish your editions, you should commit and push your answers to this repository
6. Using Github Actions we will automatically run tests and evaluate your solution, with real time feedback for you

You can either work on your code outside the container, using a text editor or IDE of your preference, or you can work on your code inside the container using a terminal based text editor like vim or emacs.

There is good support using VSCode with docker given it’s Dev Containers extension. This allows you to hook into the docker environment within VSCode, letting you access files and the terminal just as you would on your host system.

When you’re ready to start the container make sure you’re in the top level homework directory (for example, for homework 1 your current directory should be “hw1_<your-name>”, or wherever name you gave to). `pwd` should return something ending with /hw1_<your-name>. When you mount this directory within docker the permissions will change, so make sure you aren’t in a directory that you don’t want to lose access to. Once you are ready, run the following command depends on your system:

### On Linux/macOS
`docker run -v "$(pwd)":/assignments -it reeselevine/cse113:latest bash`

### On Windows
#### with Powershell (should work on both Powershell 7 and Windows Powershell):

`docker run -v ${pwd}:/assignments -it reeselevine/cse113:latest bash`

#### with cmd (Command Prompt):

`docker run -v %cd%:/assignments -it reeselevine/cse113:latest bash`

You should be running inside the container at this point. From that, you can type `cd /assignments` to access the files of your homework. Running `ls` should list your files. At any point, to exit the container just type `exit`.

Once you exit the container you can re-run the existing container either via the Docker Desktop UI by clicking the “run” icon within the list of available containers, or by the following commands in a terminal/powershell/cmd instance:

1. First list the available containers to get the assigned name from the NAMES column using `docker ps -a`
2. Start the container with `docker start <name> -i`. Add the `-i` option if you want an interactive shell. Once the container is started you can start using it if you passed -i, or connect to the container in VSCode.
3. At this point, you can edit your code and run it by following the instructions on the homework. As we were using the `-v` option, you can either edit the files using your local VSCode or any other editor in your regular way or edit directly throught the container using the terminal. Any changes you make to your files inside the container will persist when the container exits, and all changes you made in your files in your local machine will be reflected in the container for test.