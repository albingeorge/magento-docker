This hosts 2 containers:

1. A magento container
2. A mysql container

This uses docker-compose to connect the above two containers.

###Installation instructions:
1. Clone this repo
2. Make the file bin/localdb-run.sh executable

 ```
 chmod +x ./bin/localdb-run.sh
 ```

3. Build the containers

 ```
 docker-compose build
 ```

4. Start the containers

 ```
 docker-compose up -d
 ```

5. Create an /etc/hosts entry for local.magento to the docker vm machine's IP
6. Now, goto local.magento on the browser


#####To get the docker VM's IP:

```
docker-machine ip default
```


This repository is copied from https://github.com/alexcheng1982/docker-magento

For storing mysql data on the host machine, I followed the instructions from:

https://github.com/neam/docker-stack/blob/1a741b0fb2ce59e9c0cadf4516dc61f147e3efc2/stacks/debian-php-nginx.dna-project-base/docker-compose.yml#L103-L112