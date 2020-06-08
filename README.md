# Docker InfluxDB Grafana

## Version
```
Docker Image: 2.3.0
Ubuntu: 18.04
InfluxDB: 1.7.10
Grafana: 6.6.2
```

## Run
* Start container
```sh
$ docker build -t influxdb-grafana .
```
```sh  
$ docker run --ulimit nofile=66000:66000 \
  -d \
  --name influxdb-grafana \
  -p 3003:3003 \
  -p 8086:8086 \
influxdb-grafana
```
  
* Stop container
```sh
$ docker stop influxdb-grafana
```
* Restart container
```sh
$ docker start influxdb-grafana
```

## Port Forwarding
|Host|Container|Service|
|:---:|:---:|:---:|
|3003|3003|grafana|
|8086|8086|influxdb|

## Grafana
Open <http://localhost:3003>
```
Username: root
Password: root
```
