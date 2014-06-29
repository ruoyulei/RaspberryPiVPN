RaspberryPiVPN
==============

A brief and practical way to build a VPN server on you Raspberry Pi


It is super useful to log into a VPN server for countless purposes. As a matter of fact, you can build your own simply by using a raspberry pi.

Hardwares that you will need: 

1. A raspberry pi 
2. A SD card (at least 4 GB)
3. Cable to support the power of raspberry pi
4. Ethernet cable that connects your pi to the internet

Softwares that being used in the project:

1. Logmein-Hamachi
2. Privoxy


I assume that you have some basic knowledge of raspberry pi and got the OS on the raspberry pi installed (I use raspbian)

First, type

$ sudo apt-get update

Recommendedly, you might want to 

$ sudo apt-get upgrade

The upgrade takes a while. After it finished, install lsb on you pi

$ sudo apt-get install lsb-core

$ sudo apt-get install lsb

The installation of lsb is required by hamachi, which is the major app that we use to setup a virtual network. Although you can always download the latest version of logme-hamachi arm version from its website. It is highly recommended that you use 2.1.0.101-armel version which is provided here because this version is the most stable and reliable one so far as we known.

$ tar -zxvf logmein-hamachi-2.1.0.101-armel.tgz

Now you have a folder named logmein-hamachi-2.1.0.101-armel

$ cd logmein-hamachi-2.1.0.101-armel

Switch to super user

$ sudo bash

Install hamachi 

$ source ./install.sh

After the installation is over, check if hamachi works by typing

$ /etc/init.d/logmein-hamachi start

It will show version and other information. 


