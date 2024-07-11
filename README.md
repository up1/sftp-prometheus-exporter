# Working with SFTP server

## Create SFTP Server
```
$docker compose up -d sftp-basic
```

Connect to sftp server
```
$sftp -oPort=2222 foo@127.0.0.1 
```
* Password=password

## Monitoring SFTP server 
* [Prometheus Exporter for SFTP server](https://github.com/arunvelsriram/sftp-exporter)

### Create sftp exporter
```
$docker compose up -d sftp-basic-exporter
```

Access to url => http://localhost:8081/metrics


## Start Prometheus server
```
$docker compose up -d prometheus
```

Access to url => http://localhost:9090

## Start Grafana server
```
$docker compose up -d grafana
```

Access to url => http://localhost:3000
* Username=admin
* Password=password
