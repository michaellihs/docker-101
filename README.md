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

