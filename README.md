
Platform: debian 8.3 64bit

##### Install MongoDB Enterprise on Debian Jessie failed, >_<!
##### So I have to install MongoDB Community Edition!
#### Import the public key used by the package management system.
sudo apt-key adv --keyserver 'keyserver.ubuntu.com' --recv '7F0CEB10'
#### Create a /etc/apt/sources.list.d/mongodb-enterprise.list file for MongoDB.
echo 'deb http://repo.mongodb.org/apt/debian wheezy/mongodb-org/3.2 main' | sudo tee '/etc/apt/sources.list.d/mongodb-org-3.2.list'
##### There's no jessie repository, so I have to use wheezy.
#### Reload local package database.
sudo apt-get update
#### Install the MongoDB packages.
sudo apt-get install -y mongodb-org
