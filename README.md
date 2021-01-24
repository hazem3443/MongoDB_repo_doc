# install MongoDB locally (linux)


1. Import the public key used by the package management system.
   
```
wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
```
  
-  Install gnupg and its required libraries using the following command:

```
sudo apt-get install gnupg
```

- Once installed, retry importing the key:

```
wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
```

1. Create a list file for MongoDB.

```
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
```
2. Reload local package database.        
```
sudo apt-get update
```


3. Install the MongoDB packages.
```
sudo apt-get install -y mongodb-org
```

for more info go to [link](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/)

# install MongoDB with docker 
1. docker pull 
```
docker pull mongo
```

# install mongoDB-compass 

1. Update your operating system.
   ```
   apt-get update
   ```
2. Download MongoDB compass
   ```
   wget https://downloads.mongodb.com/compass/mongodb-compass_1.15.1_amd64.deb
   ```
3. install the compass
   ```
   sudo dpkg -i mongodb-compass_1.15.1_amd64.deb
   ```



# install portainer for managing docker containers

1. Install and Configure Portainer
```
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
```