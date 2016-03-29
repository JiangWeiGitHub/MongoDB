### Install MongoDB
**Related Reference:**[ Click Here](https://docs.mongodb.org/manual/administration/install-on-linux/)<p>

###### Platform: debian 8.3 64bit<p>

*Install MongoDB Enterprise on Debian Jessie failed, >_<!*<p>
*So I have to install MongoDB Community Edition instead!*<p>

* Import the public key used by the package management system.<p>
`sudo apt-key adv --keyserver 'keyserver.ubuntu.com' --recv '7F0CEB10'`<p>

* Create a /etc/apt/sources.list.d/mongodb-enterprise.list file for MongoDB.<p>
`echo 'deb http://repo.mongodb.org/apt/debian wheezy/mongodb-org/3.2 main' | sudo tee '/etc/apt/sources.list.d/mongodb-org-3.2.list'`<p>
###### There's no jessie repository, so I have to use wheezy.<p>

* Reload local package database.<p>
`sudo apt-get update`<p>
  PS: If it appears "W: GPG error: http://repo.mongodb.org wheezy/mongodb-org/3.2 Release: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D68FA50FEA312927", you can use: __apt-key adv --keyserver keyserver.ubuntu.com --recv-keys D68FA50FEA312927__<p>

* Install the MongoDB packages.<p>
`sudo apt-get install -y mongodb-org`<p>
