 
FROM ubuntu:18.04

#更换apt源
RUN sed -i "s/security.ubuntu.com/mirrors.tuna.tsinghua.edu.cn/g" /etc/apt/sources.list && sed -i "s/archive.ubuntu.com/mirrors.tuna.tsinghua.edu.cn/g" /etc/apt/sources.list
#RUN sed -i "s/ppa\.launchpad\.net/lanuchpad.moruy.cn/g" /etc/apt/sources.list.d/*.list
#安装更新及安装必备软件
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive  &&  apt-get install -y apt-utils apache2 mysql-client php7.2 libapache2-mod-php vim curl
RUN apt-get -y upgrade && apt-get -y install php7.2-curl php7.2-mysqli php7.2-gd php7.2-mbstring php7.2-xml php7.2-curl

EXPOSE 80
