# Setup two Container using Custom bridge network
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftedg-cisco%2Fpython-app.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftedg-cisco%2Fpython-app?ref=badge_shield)


## 1. Create Custom Bridge Network

```
  docker network create -d bridge javahome
  
```

## 2. Run redis container

We are using official image of redis(This image comes from docker hub)
by default redis container runs on 6379 port

```
  docker run -d --name=redis --network=javahome redis:latest
  
```

## 3. Run Python Container

Python is the application developed by me, so this image comes from my docker hub account(it is public)

```
  docker run -d -p 8080:5000 --name=pythonap  --network=javahome kammana/python-app:1
```

## 4. Access The APp

Open browser and put the following url
http://<ip-address>:8080


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftedg-cisco%2Fpython-app.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftedg-cisco%2Fpython-app?ref=badge_large)