# Install Neo4j with Docker Ubuntu Server


### Install using the repository
Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker repository. Afterward, you can install and update Docker from the repository.

### Set up the repository
1.  Update the apt package index and install packages to allow apt to use a repository over HTTPS:

        $ sudo apt-get update
    
        $ sudo apt-get install \
          ca-certificates \
          curl \
          gnupg \
          lsb-release
2. Add Docker’s official GPG key:

        $ sudo mkdir -p /etc/apt/keyrings

        $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
3. Use the following command to set up the repository:

        $ echo \
          "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
          $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
          
### Install Docker Engine
1. Update the apt package index:

        $ sudo apt-get update
2. Install Docker Engine, containerd, and Docker Compose.

    To install the latest version, run: 

        $ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
3. Verify that the Docker Engine installation is successful by running the hello-world image:

        $ sudo docker run hello-word
## Install the Compose plugin
### Install using the repository
1. Update the package index, and install the latest version of Docker Compose:

        $ sudo apt-get update
        
        $ sudo apt-get install docker-compose-plugin
        
2. Verify that Docker Compose is installed correctly by checking the version.

        $ docker compose version
        Output: Docker Compose Version v2.12.2(for now)
 ## neo4j docker playground from https://github.com/ikwattro
1. clone
 
        $ git clone https://github.com/ikwattro/neo4j-docker-playground.git
2. Stop neo4j if it's still running, open directory neo4j-docker-playground and go to any directory, run:        
        
        $ sudo docker compose up -d
        $ sudo docker ps
        $ cat docker-compose.yml
3. Open browser "(your ip):7474"
 
        
