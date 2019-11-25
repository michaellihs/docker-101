Docker 101
==========

A hands-on 101 on Docker. Currently this tutorial is supposed to be for Mac users only.

Prerequisites
-------------

* [iTerm2 for Mac](https://iterm2.com/downloads.html)
* [git](https://git-scm.com/download/mac)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)

Step 1 - `vagrant up`
---------------------

> What is Vagrant? Vagrant provides an easy way to set up virtual machines on your computer. Therefore we do not have to install all the software required for this tutorial on your machine and can leave it in a clean state, once we are done.

* open a terminal window by pressing `COMMAND + SPACE` and start typing `iterm2` - once the iterm application shows up, press `RETURN`
* if you don't have a workspace directory on your computer, create one, via

   ```bash
   cd
   mkdir workspace
   cd workspace
   ```

* make a copy of this repository in your workspace via

   ```bash
   cd
   cd workspace
   git clone https://github.com/michaellihs/docker-101.git
   ```

* start the Vagrant Box that is included in this repository and get inside of it

   ```bash
   vagrant up
   ... this will take a while ...
   vagrant ssh
   ```
   
Step 2 - Test your Docker Setup
-------------------------------

> Following the famous tradition of running `hello world` programs to proof that something is working as expected, we will do a little Docker `hello world` first

* within your Vagrant Box (remember, you got in there via `vagrant ssh` in the directory where this project was cloned to, after running `vagrant up`), run

   ```bash
   docker run hello-world
   ```
   
  this should show something like
  
   ```bash
   Hello from Docker!
   This message shows that your installation appears to be working correctly.

   To generate this message, Docker took the following steps:
    1. The Docker client contacted the Docker daemon.
    2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
       (amd64)
    3. The Docker daemon created a new container from that image which runs the
       executable that produces the output you are currently reading.
    4. The Docker daemon streamed that output to the Docker client, which sent it
       to your terminal.

   To try something more ambitious, you can run an Ubuntu container with:
    $ docker run -it ubuntu bash

   Share images, automate workflows, and more with a free Docker ID:
    https://hub.docker.com/

   For more examples and ideas, visit:
    https://docs.docker.com/get-started/
   ```

* so what did just happen?
  1. by running the `docker run` command, Docker tried to start a new *container* from an image called *hello-world*
  1. since this image was not available locally, Docker downloaded it from a website called *Dockerhub* and immediately started it
  1. everything this image is doing, is showing the above output to kind of proof that your Docker setup works as expected

