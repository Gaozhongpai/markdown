# Frequently used command

## ssh related

Generate private and public ssh keys:

``ssh-keygen``

On the server
`` <remoteuserhome>/.ssh/authorized_keys``

## docker related

display a list of containers

``docker ps -a``

Last container ``docker ps -l``  

enter a running container

``docker exec -it [container-id] bash``

commit container to image

``docker commit [CONTAINER_ID] [new_image_name]``

## ubuntu related

multiple versions

```
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2
```

