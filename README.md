# Scanner Apache Bench

This project is based on doing in a standard way using docker to use the Stress testing using Apache Bench.

# Table contents
1. [Information](#information)
2. [Requirements](#requirements)
3. [Commands](#commands)
4. [Autor](#autor)
5. [Example](#example)
6. [Contact](#contact)
7. [Documentation](#documentation)

## Information
- **Apache Bench**: It is based on Apache.

## Requirements
- **Docker**: It is required to have docker installed.
- **Docker Compose**: It is required to have docker compose installed.

# Commands

## Clone repository
```shell
git clone git@github.com:gbolivar/stress-bench.git
```

## Access the project
```shell
cd stress-bench
```

### Commands executed locally

Once the repository is cloned, the first thing is to generate the docker images:

```shell
docker-compose up -d --build
```
### To run the command in the container:

Scan an image in python with alpine
```shell
# Ontro project
docker-compose exec apache-bench ab -n 100 -c 10 -k -S https://ironsofts.com/
```
```shell
# Any part
docker exec -it apache-bench ab -n 1000 -c 10 -k -S https://httpd.apache.org/
```

Then go into the backend container:

```shell
docker exec -it apache-bench /bin/bash
```

To exit the container, use the exit command:

```shell
exit
```

Then you may want to delete the entire project container and leave it clean.:

```shell
docker-compose down
```
## Autor
Create for [Gregorio José Bolívar Bolívar](https://x.com/gbolivarb)

[![Twitter](https://img.shields.io/twitter/follow/gbolivarb?style=social)](https://x.com/gbolivarb)
[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&labelColor=0077B5)](https://www.linkedin.com/in/gregorio-bolivar/)
[![GitHub](https://img.shields.io/github/followers/gbolivar?style=social)](https://github.com/gbolivar)

### Contact
<p>
  Anything you need let me know so I can help you. 💬.
</p>
<p>
    <a href="https://x.com/gbolivarb" target="_blank">
        <img src="https://abs.twimg.com/responsive-web/client-web/icon-ios.77d25eba.png" 
    height="30">
    </a> &nbsp;&nbsp;
    <a href="https://github.com/gbolivar" target="_blank">
        <img src="https://cdn.iconscout.com/icon/free/png-256/github-153-675523.png" 
    height="30">
    </a> &nbsp;&nbsp;
    <a href="https://www.linkedin.com/in/gregorio-bolivar/" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/768px-LinkedIn_logo_initials.png" 
    height="30">
    </a>  &nbsp;&nbsp;
    <a href="https://ironsofts.com" target="_blank">
        <img src="https://ironsofts.com/assets/images/app/logo.png" 
    height="30">
    </a>
</p>

## Example
```shell
docker exec -it apache-bench ab -n 1000 -c 10 -k -S https://httpd.apache.org/
This is ApacheBench, Version 2.3 <$Revision: 1913912 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking httpd.apache.org (be patient)
Completed 100 requests
Completed 200 requests
Completed 300 requests
Completed 400 requests
Completed 500 requests
Completed 600 requests
Completed 700 requests
Completed 800 requests
Completed 900 requests
Completed 1000 requests
Finished 1000 requests


Server Software:        Apache
Server Hostname:        httpd.apache.org
Server Port:            443
SSL/TLS Protocol:       TLSv1.3,TLS_AES_128_GCM_SHA256,2048,128
Server Temp Key:        X25519 253 bits
TLS Server Name:        httpd.apache.org

Document Path:          /
Document Length:        7842 bytes

Concurrency Level:      10
Time taken for tests:   2.653 seconds
Complete requests:      1000
Failed requests:        0
Keep-Alive requests:    1000
Total transferred:      8353031 bytes
HTML transferred:       7842000 bytes
Requests per second:    376.90 [#/sec] (mean)
Time per request:       26.532 [ms] (mean)
Time per request:       2.653 [ms] (mean, across all concurrent requests)
Transfer rate:          3074.46 [Kbytes/sec] received

Connection Times (ms)
              min   avg   max
Connect:        0     0   50
Processing:    12    23  286
Waiting:       11    21  285
Total:         12    23  328

Percentage of the requests served within a certain time (ms)
  50%     21
  66%     23
  75%     25
  80%     26
  90%     29
  95%     34
  98%     41
  99%     75
 100%    328 (longest request)
```



## Documentation
- [Apache Bench doc](https://nowitsanurag.medium.com/stress-testing-using-apache-bench-ab-98a3f1312246)
- [Command ab](https://httpd.apache.org/docs/2.4/programs/ab.html)

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html)




