# raspi-gyro

The proposal for this project is implements a simple test for testing gyroscope in mobile phones.
We are going to use Node.JS in server application and WebSockets in client application by HTTP.
Server application will be run in "Raspberry Pi" in this tutorial and web application using ipad or iphone devices.

# Prerequisites

Preparing and configuring our Raspberry Pi

We need to have installed node in version 0.12 in the linux device

	> wget http://node-arm.herokuapp.com/node_latest_armhf.deb
	> sudo dpkg -i node_latest_armhf.deb

After install we will check installation

	> node -v
	(The expected result should be v0.12.x or upper)

Next package necesary is npm

	> sudo apt-get install npm

When npm was installed and exists some authentication problem using https, it will be necesary set registry without https

	> sudo npm config set registry http://registry.npmjs.org/

# Installing components and applications

First clone the git repository in someone directory (example: /home/pi/test)

	> git clone https://github.com/jomifm/raspi-gyro
	
Download modules for node from npm registry

	> cd raspi-gyro
	> npm install socket.io ip node-static
	
# Testing

Start server application in "Raspberry Pi"

	> cd /home/pi/raspi-gyro
	> node server.js
	
Start web browser in mobile device. Set address and port to the Raspberry Pi address on your network

	http://192.168.1.11:8080



