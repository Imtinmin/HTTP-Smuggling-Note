> 通过nginx反代可以修改Client-IP

![2019-12-22.jpg](https://i.loli.net/2019/12/22/Wn9KByLZIT1gmzq.jpg)

修改`docker-compose.yml`的

```dockerfile
    ports:
      - "port:8080"
```

端口应和

`atss-etc/remap.conf`对应

```
regex_map http://(.*):port/ http://http-nginx/
```

