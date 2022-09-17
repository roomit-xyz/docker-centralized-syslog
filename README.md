# DONATE

1. Ethereum : <pre>0xB0e6e6c379389bBB30fACD427e02d74d27ec0C78</pre>
2. Near Blockchain : <pre>xoreth.near</pre>
3. Mina Protocol : <pre>B62qiiBBXKN5CdgXv7wPkXxC1prdzQxwfaTMAi3isAeb9F7gCbzi5dU</pre>




# DOCKER-SYSLOG wajatmaka | IMPORTANT !!!

FHS Docker Syslog-ng :
```
  /docker
    |
    |
    |---|-----conf.d
    |   |-----Docker-Builds
    |   |          |--syslog
    |   |          |--tftp
    |   |-----docker-compose.yml

   /data
    |
    |-----log
    |      |
    |      |---networks
    |      |---os
    |---------backup
    |           |
    |           |---bin
    |           |---data
    |-----tftp     

```


## Information ##
Directory **/docker** is important, we can build any service in this directory.


### How To Build and Running Service ###
How to build and running docker with docker-compose? except docker compose we can run manual using **_docker run_**.
The following command build and run using docker-compose :


### Syslog-networks ####
** Build **
> `cd /docker`
> `docker-compose build syslog-networks`


** Running **
> `cd /docker`
> `docker-compose start syslog-networks`


** Build and Running **
>`cd /docker`
>` docker-compose up -d --build syslog-networks`


### How Check Service Running ###
Standard to check service using :
> `docker ps`


check all service using :
> `docker ps -a`


### How Start, Stop And Restart Service  ###
stop service in container
> `docker stop syslog-networks`


start service in container
> `docker start syslog-networks`


restart service in container
> `docker restart syslog-networks`


