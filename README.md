

1. Install WSL2 https://pureinfotech.com/install-windows-subsystem-linux-2-windows-10/ or https://learn.microsoft.com/en-us/windows/wsl/install
2. Install docker for window
3. Open Ubuntu And Docker
4. In Ubuntu terminal 
	4.1 sudo apt-get update && upgrade
	4.2 Pull the MongoDB Docker Image: docker pull mongodb/mongodb-community-server
	4.3 Run the Image as a Container: docker run -d -p 27017-27019:27017-27019 --name mongodb mongo:latest
	4.4 Check that the Container is Running: docker container ls
	4.5 Connect to the MongoDB Deployment with mongosh: docker exec -it mongo mongosh
	4.6 Validate Your Deployment: 
		db.runCommand(
		   {
			  hello: 1
		   }
		)
5. Connect mongodb from window
	In Ubuntu terminal:  docker inspect mongodb | grep IPAddress
