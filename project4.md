# Kingsley Documentation Of Project 4

In this Project, i am going to implement a simple Book Register web form using MEAN stack.

## Step 1: Install NodeJs

`sudo apt update`

`sudo apt upgrade -y`

`sudo systemctl status`

![ubuntu status](./images/status-ubuntu.jpg)

*Add certificates*

`sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates

curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -`

![certificates](./images/certificates-status.jpg)

*Install Nodejs*

`sudo apt install -y nodejs`

![nodejs](./images/nodejs-status.jpg)


## Step 2 - Install MongoDB

*Import the public key used by the package management system*

`sudo apt-get install gnupg curl`

*Issue the following command to import the MongoDB public GPG Key from 
https://pgp.mongodb.com/server-6.0.asc
:*

`curl -fsSL https://pgp.mongodb.com/server-6.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-6.0.gpg \
   --dearmor`

*Create a list file for MongoDB*

`echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-6.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list
`

*Reload local package database*

`sudo apt-get update`

![apt get update](./images/apt-get-update.jpg)

*Install the MongoDB packages*

`sudo apt-get install -y mongodb-org`

![mongodb packages](./images/mongodb-packages.jpg)

*Start and Enable The Mongod Service*

`sudo systemctl start mongod`

`sudo systemctl status mongod`

![mongod status](./images/mongod-status.jpg)

Update Version of NodeJS

*Installing Node.js with Apt Using a NodeSource PPA*

`curl -sL https://deb.nodesource.com/setup_18.x -o /tmp/nodesource_setup.sh`

*Check Nodejs content with test editor*

`nano /tmp/nodesource_setup.sh`

![updated nodejs content](./images/updated-nodejs-content.jpg)

*Run the script with sudo*

`sudo bash /tmp/nodesource_setup.sh`

The PPA will be added to your configuration and your local package cache will be updated automatically. You can now install the Node.js package in the same way you did in the previous section

`sudo apt install nodejs`

*Nodejs version update*

`node -v`

![updated nodejs status](./images/updated-nodejs-status.jpg)

*Install body-parser package*

`sudo npm install body-parser`

![body parser](./images/body-parser-install.jpg)

*Create a folder named ‘Books’*

`mkdir Books && cd Books`

*In the Books directory, Initialize npm project*

`npm init`

![npm init](./images/npm-init.jpg)

*Add a file to it named server.js*

`sudo vi server.js`

*Copy and paste the web server code below into the server.js file*

`var express = require('express');
var bodyParser = require('body-parser');
var app = express();
app.use(express.static(__dirname + '/public'));
app.use(bodyParser.json());
require('./apps/routes')(app);
app.set('port', 3300);
app.listen(app.get('port'), function() {
    console.log('Server up: http://localhost:' + app.get('port'));
});`















