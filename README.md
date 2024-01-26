# fabricNetworkSetUp


clone this repository
```
git clone https://github.com/daser/fabricNetworkSetUp.git
```

change into the directory

```
cd fabricNetworkSetUp
```

```
cd /blockchain/aritifacts/channel/create-certificate-with-ca
```

create CA servers 
```
docker-compose up -d
```

Create crypto material

```
./create-certificate-with-ca.sh
```

```
cd ../
```

```
./create-artifacts.sh
```

```
cd /blockchain/artifacts
```

```
docker ps
```

```
docker-compose up -d
```

```
docker logs orderer.example.com -f
```

```
cd /blockchain/scripts
```

```
./createChannel.sh
```

```
./deployChaincode.sh
```

Last step is to set up Explorer

```
cd /blockchain/Explorer
```

```
docker-compose up -d
```

Check if you have the images running
```
docker ps | grep expl
```

assuming they are running you should check the log for one of them

```
docker logs explorer.mynetwork.com -f
```

run on the browser


http://localhost:8081/#/login
