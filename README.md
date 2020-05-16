# Influxdb Grafana for Guider

#### Version
```
Docker Image: 2.3.0
Ubuntu: 18.04
InfluxDB: 1.7.10
Grafana: 6.6.2
```

#### Run
* Start container
  * Method 1: Use DockerHub
  ```sh
  docker pull yoonje/influxdb-grafana-for-guider
  ```
  ```sh  
  docker run --ulimit nofile=66000:66000 \
    -d \
    --name guider-visualization \
    -p 3003:3003 \
    -p 8086:8086 \
  yoonje/guider-influxdb-grafana
  ```
  * Method 2: Build in local environment
  ```sh
  docker build -t guider-influxdb-grafana .
  ```
  ```sh  
  docker run --ulimit nofile=66000:66000 \
    -d \
    --name guider-visualization \
    -p 3003:3003 \
    -p 8086:8086 \
  guider-influxdb-grafana
  ```
  
* Stop container
```sh
docker stop guider-visualization
```
* Restart container
```sh
docker start guider-visualization
```

#### Port Forwarding
|Host|Container|Service|
|:---:|:---:|:---:|
|3003|3003|grafana|
|8086|8086|influxdb|

#### Grafana
Open <http://localhost:3003>
```
Username: root
Password: root
```
