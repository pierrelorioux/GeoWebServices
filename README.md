RedCross GeoWebServices
============

Using Node.js 0.10.15

Instructions for setting up Node.js 0.10.15 on Ubuntu 12.04 (EC2)
=========================================================================	

### Install 'make', g++, python, curl, git ,etc
	sudo apt-get upgrade
	sudo apt-get install g++ curl libssl-dev apache2-utils git-core
	sudo apt-get install make
	sudo apt-get install python-software-properties

### Install Node
	sudo add-apt-repository ppa:chris-lea/node.js
	sudo apt-get update 
	sudo apt-get install nodejs

### download and install node package manager (npm)
	cd /tmp 
	git clone http://github.com/isaacs/npm.git 
	cd npm 
	sudo make install

### Use npm to install Express
	sudo npm install express

### Create services directory, clone repo (Ryan's spatial server for now, will be this repo soon)
	cd ~
	mkdir webservices
	cd webservices
	git clone https://github.com/spatialdev/PGRestAPI.git

### Install the GeoWebServices node app, global install of nodemon, open port 3000
	cd PGRestAPI
	sudo npm install
	sudo npm install -g nodemon
	sudo ufw allow 3000







