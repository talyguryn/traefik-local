# Traefik

Example of running on localhost.

![](https://telegra.ph/file/aa37dbbf11e2efebb7c2a.jpg)

![](https://telegra.ph/file/f9273e7c6079b50c163e3.jpg)

## How to run

Create network `traefik`

```
docker network create traefik
```

Update `/etc/hosts` file.

```
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting. Do not change this entry.
##
127.0.0.1       localhost
255.255.255.255 broadcasthost
::1             localhost

127.0.0.1       traefik.local
127.0.0.1       grafana.local
127.0.0.1       prometheus.local
127.0.0.1       whoami.local
127.0.0.1       nginx.local
127.0.0.1       wordpress.local
```

Run traefik container

```
cd traefik
docker-compose up -d
```

Run other containers.
