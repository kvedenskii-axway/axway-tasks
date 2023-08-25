* [Get familiar with Linux](#get-familiar-with-linux)
* [Install Joomla in Ubuntu](#install-joomla-in-ubuntu-and-configure-redis-for-caching)
* [Install Redis and configure Joomla caching](#install-redis-and-configure-joomla-caching)
* [Configure SSL for Joomla site](#configure-ssl-for-joomla-site)
* [Joomla in docker container](#joomla-in-docker-container)

## Get familiar with Linux

1. Create Ubuntu virtual machine.  
**Note**:  For Linux newbies use [LTS desktop Ubuntu](https://ubuntu.com/download/desktop), not server version  
![Ubuntu Desktop LTS](assets/ubuntu-lts-desktop.png "Ubuntu Desktop LTS")
2. Get some very basic idea of Linux terminal.

**Suggested reading**:
* [Install Ubuntu in VirtualBox](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox)
* [How to open Terminal for commands in Ubuntu](https://itsfoss.com/open-terminal-ubuntu)
* [Linux - Tutorial for Beginners in 13 MINUTES!](https://www.youtube.com/watch?v=BMGixkvJ-6w)
* [40 Essential Linux Commands](https://www.hostinger.com/tutorials/linux-commands)

## Install Joomla in Ubuntu
1. Install Joomla prerequisites:
    * Apache webserver
    * PHP
    * MySQL
2. Install Joomla

**Suggested reading if you got stuck**:
* [Install Apache, PHP, MySQL and Joomla](https://www.linuxtuto.com/how-to-install-joomla-4-on-ubuntu-22-04/)  
**Note**: before *Step 6* in the tutorial missed disable default Apache configuration instruction. Execute this command before *Step 6*:
  ```sh
  sudo a2dissite *.conf
  ```

**Advice**:
* Use [VirtualBox snapshots](https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/snapshots.html) in order not to loose previously done work

## Install Redis and configure Joomla caching

1. Install Redis server and redis extension for PHP
2. Configure Joomla caching with Redis

**Suggested reading if you got stuck**:
* [How to install and Secure Redis on Ubuntu 22.04](https://www.rosehosting.com/blog/how-to-install-and-secure-redis-on-ubuntu-22-04/)  
**Note**: restart apache service after *Step 3*:
  ```sh
  sudo systemctl restart apache2
  ```

## Configure SSL for Joomla site

Configure the Joomla site to run over SSL (with self-signed certificate).

**Suggested reading**:

* [What is an SSL certificate](https://www.kaspersky.com/resource-center/definitions/what-is-a-ssl-certificate)

**Suggested reading if you got stuck**:
* [Creating a Self-Signed Certificate](https://www.baeldung.com/openssl-self-signed-cert)

## Joomla in docker container

TBD
