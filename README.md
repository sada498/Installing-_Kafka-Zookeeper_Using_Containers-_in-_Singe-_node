# Install_Kafka_Zookeeper_Using_Containers_in_Singe_node
 How to Install a kafka and Zookeeper using Containers In single Ubuntu Node
 Installing a Kafka Custer in single node in Containers
### 1.Adding Docker to your package Repository
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```
![Add Your User to the Docker Group](/data/Images/Add Your User to the Docker Group.png)
 
### 2.Install docker and update the packages
```
sudo apt update
```
```
sudo apt install -y docker-ce=18.06.1~ce~3-0~ubuntu
```
 
### 3.Add Your User to the Docker Group
```
sudo usermod -a -G docker <your username>
```
 
### 4.Instal Docker Compose
```
sudo -i
```
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

  ```
```
chmod +x /usr/local/bin/docker-compose
```

### 5.Clone Repo from docker
 

### 6.Change directory 
```
 cd Installing_Kafka-Zookeeper_Using_Containers_in_Singe_node
```
### 7.Run docker 
```
docker-compose up -d –build
 ```
 

### 8.Install java
```
sudo apt install -y default-jdk
```

### 9.Download Kafka Binaries
 ```
wget https://mirror.cogentco.com/pub/apache/kafka/2.7.0/kafka_2.12-2.7.0.tgz 
   ```
```
tar -xvf kafka_2.12-2.7.0.tgz 
```
 




# Creating a first topic 
### Change directory to 
```
cd kafka_2.12-2.7.0
```

### create first topic
 
## Describe the topic
```
./bin/kafka-topics.sh --zookeeper localhost:2181 --topic test --describe
```

## Docker images and Container check
List of images in node
```
docker images 
```
 
## Check all 3 Kafka and 3 Zookeeper running in node

 ```
docker ps
```
 

