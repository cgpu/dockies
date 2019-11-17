# dockies
Useful scripts, snippets and guidelines for common tasks related to docker

If a container is too big and you're working in an Centos based EC2 instance (does not work for ubuntu), this might work:


```
sudo service docker stop
sudo nano /etc/sysconfig/docker-storage
# change the storage
DOCKER_STORAGE_OPTIONS= --storage-opt dm.basesize=30G
sudo service docker start
```
