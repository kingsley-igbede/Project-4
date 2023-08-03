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







