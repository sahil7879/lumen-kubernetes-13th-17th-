13th :



```
--- created a server ubuntu : 

172.214.82.77

creds :
ramanvm
Ramankhanna@4321


ssh ramanvm@172.214.82.77

```

```
-- install docker as container runtime :

sudo -i


https://docs.docker.com/engine/install/ubuntu/



```


```

docker runtime operations :

 systemctl status docker
   20  clear
   21  docker ps
   22  docker images
   23  docker run -dt --name c1 centos:7
   24  docker ps
   25  clear
   26  cat /etc/os-release
   27  docker ps
   28  docker exec -it c1 ls
   29  docker exec -it c1 /bin/bash
   30  docker ps
   31  docker exec -it c1 ls
   32  docker exec -it c1 mkdir khanna
   33  docker exec -it c1 ls
   34  docker run -d --name c2 httpd
   35  docker ps
   36  docker exec -it c1 /bin/bash
   37  ps -ef
   38  clear
   39  docker ps
   40  docker images
   41  docker run -d --name c3 redis

cntrl+p+q

```


```

docker run -d --name c3 redis
   42  clear
   43  history
   44  clear
   45  docker ps
   46  docker images
   47  clear
   48  history
   49  clear
   50  docker ps
   51  clear
   52  docker ps
   53  docker images
   54  clear
   55  docker build
   56  docker build -h
   57  clear
   58  ls
   59  pwd
   60  docker images
   61  clear
   62  ls
   63  vi ramandockerfile
   64  docker images
   65  clear
   66  docker rm -f `docker ps -aq`
   67  docker rmi -f `docker ps -aq`
   68  docker rmi -f `docker images`
   69  clear
   70  docker ps
   71  docker images
   72  ls
   73  cat ramandockerfile
   74  docker build -t ramanimage:v1 -f ramandockerfile .
   75  docker images
   76  docker history ramanimage:v1
   77  clear
   78  docker images
   79  docker ps
   80  docker run -d --name ramancontainer ramancustomimage:v1
   81  docker run -d --name ramancontainer ramanimage:v1
   82  docker ps
   83  docker ps -a
   84  docker rm -f ramancontainer
   85  docker run -dt --name ramancontainer ramanimage:v1
   86  docker ps
   87  clear
   88  docker ps
   89  docker exec -it ramancontainer ls
   90  docker exec -it ramancontainer yum update -y
   91  docker exec -it ramancontainer which httpd
   92  docker exec -it ramancontainer rpm -qa | grep httpd
   93  docker exec -it ramancontainer rpm -qa | grep php
   94  docker exec -it ramancontainer cat /var/www/html/index.html

```


```

root@raman-docker:~# cat ramandockerfile
FROM centos:7
MAINTAINER  Raman Khanna raman.khanna@email.com
RUN mkdir /dataforaman
RUN yum update -y
RUN yum -y install httpd   php
RUN echo " DevOps and Cloud" > /var/www/html/index.html
EXPOSE 80
CMD ["/bin/bash"]

```


```



purpose : manage containers :

master : managements components  (pods_

worker : my ownapplications (pods)



kubeadm Kubernetes cluster :

3 nodes : master/controlplane , 2 worker nodes 



https://v1-29.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/

https://v1-29.docs.kubernetes.io/docs/reference/networking/ports-and-protocols/





calico , flannel , weave








  70  k get nodes
   71  k get nodes -o wide
   72  kubectl get ns
   73  clear
   74  kubectl get pods
   75  kubectl get ns
   76  kubectl get pods -n kube-system
   77  kubectl get pods -n kube-system -o wide
   78  clear
   79  kubectl get pods -n kube-system -o wide | grep master
   80  kubectl get pods -n kube-system -o wide | grep w1
   81  kubectl get pods -n kube-system -o wide | grep w2
   82  clear
   83  kubectl get pods -n kube-system -o wide
   84  clear
   85  k get nodes
   86  k get pods
   87  k create ns raman
   88  k get ns
   89  history

```


