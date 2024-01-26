# fabricNetworkSetUp

```
cd /blockchain/aritifacts/channel/create-certificate-with-ca
```

```
docker-compose up -d
```

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
