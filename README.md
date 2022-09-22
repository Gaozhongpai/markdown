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

## docker from Meng

郑梦(UII)(Meng ZHENG)@联影集团 9-21 pm03:32:31
```
NV_GPU=2,3 nvidia-docker run --shm-size=32G -p 6666:22 --cpuset-cpus="0-15" \
-v /mnt/UII_DataShare/data/Theta-Intelligence/PatientPositioning/Datasets/:/mnt/data \
-v /mnt/UII_DataShare/data/vision/:/mnt/data_vision -v /mnt/interns/:/mnt/code_intern/ \
-v /mnt/UIIUSA/mengz/code/:/mnt/code/ -it 10.10.0.192:5555/retinaface_meng bash

Host 162_SLP
    HostName 10.10.0.162
    User meng
    Port 6789
```
Run bash inside a docker save as `ssh_start.sh`
```
#!/bin/bash

apt-get update
apt-get install openssh-server
mkdir /var/run/sshd
chmod 0755 /var/run/sshd
/usr/sbin/sshd
useradd --create-home --shell /bin/bash --groups sudo meng
#passwd meng
#service ssh start
```


## ubuntu related

multiple versions

```
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2
```

