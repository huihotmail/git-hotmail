docker

镜像images：就是将软件和软件所需要的运行环境打包到一个镜像文件里面

通过镜像文件可以创建对应的容器，容器有了，软件就会自动有了

Daemon:守护进程

![Screen Shot 2022-04-18 at 5.26.02 PM](docker/Screen%20Shot%202022-04-18%20at%205.26.02%20PM.png)

![Screen Shot 2022-04-18 at 5.30.18 PM](docker/Screen%20Shot%202022-04-18%20at%205.30.18%20PM.png)

![Screen Shot 2022-04-18 at 5.30.37 PM](docker/Screen%20Shot%202022-04-18%20at%205.30.37%20PM.png)

![Screen Shot 2022-04-18 at 5.31.29 PM](docker/Screen%20Shot%202022-04-18%20at%205.31.29%20PM.png)

![Screen Shot 2022-04-18 at 7.32.25 PM](docker/Screen%20Shot%202022-04-18%20at%207.32.25%20PM.png)

![Screen Shot 2022-04-18 at 7.33.15 PM](docker/Screen%20Shot%202022-04-18%20at%207.33.15%20PM.png)

![Screen Shot 2022-04-18 at 7.34.45 PM](docker/Screen%20Shot%202022-04-18%20at%207.34.45%20PM.png)

![Screen Shot 2022-04-18 at 7.35.47 PM](docker/Screen%20Shot%202022-04-18%20at%207.35.47%20PM.png)

# 启动docker

![Screen Shot 2022-04-18 at 7.39.31 PM](docker/Screen%20Shot%202022-04-18%20at%207.39.31%20PM.png)

# 停止docker

![Screen Shot 2022-04-18 at 7.40.12 PM](docker/Screen%20Shot%202022-04-18%20at%207.40.12%20PM.png)

# 重启docker

![Screen Shot 2022-04-18 at 7.40.37 PM](docker/Screen%20Shot%202022-04-18%20at%207.40.37%20PM.png)

# 开机启动/Linux服务器一启动

# Deamon 守护：后台运行

开机启动/Linux服务器一启动，就自动打开docker

![Screen Shot 2022-04-18 at 7.41.33 PM](docker/Screen%20Shot%202022-04-18%20at%207.41.33%20PM.png)

# images镜像

![Screen Shot 2022-04-18 at 8.37.44 PM](docker/Screen%20Shot%202022-04-18%20at%208.37.44%20PM.png)

![Screen Shot 2022-04-18 at 8.38.31 PM](docker/Screen%20Shot%202022-04-18%20at%208.38.31%20PM.png)

# 查看镜像

![Screen Shot 2022-04-18 at 8.41.34 PM](docker/Screen%20Shot%202022-04-18%20at%208.41.34%20PM.png)

镜像images：就是将软件和软件所需要的运行环境打包到一个镜像文件里面

通过镜像文件可以创建对应的容器，容器有了，软件就会自动有了

image ID删除的时候用的到

# 查找镜像

查找redis的镜像

![Screen Shot 2022-04-18 at 8.47.04 PM](docker/Screen%20Shot%202022-04-18%20at%208.47.04%20PM.png)

# 下载镜像/拉取

![Screen Shot 2022-04-18 at 8.48.14 PM](docker/Screen%20Shot%202022-04-18%20at%208.48.14%20PM.png)

![Screen Shot 2022-04-18 at 8.49.41 PM](docker/Screen%20Shot%202022-04-18%20at%208.49.41%20PM.png)

# 查找下载哪个版本的镜像

![Screen Shot 2022-04-18 at 8.50.22 PM](docker/Screen%20Shot%202022-04-18%20at%208.50.22%20PM.png)

![Screen Shot 2022-04-18 at 8.51.17 PM](docker/Screen%20Shot%202022-04-18%20at%208.51.17%20PM.png)

![Screen Shot 2022-04-18 at 8.52.01 PM](docker/Screen%20Shot%202022-04-18%20at%208.52.01%20PM.png)

# 删除镜像

![Screen Shot 2022-04-18 at 8.53.47 PM](docker/Screen%20Shot%202022-04-18%20at%208.53.47%20PM.png)

![Screen Shot 2022-04-18 at 8.55.36 PM](docker/Screen%20Shot%202022-04-18%20at%208.55.36%20PM.png)

![Screen Shot 2022-04-18 at 8.56.41 PM](docker/Screen%20Shot%202022-04-18%20at%208.56.41%20PM.png)

# 容器的相关命令

镜像文件创建出了容器

![Screen Shot 2022-04-18 at 8.59.47 PM](docker/Screen%20Shot%202022-04-18%20at%208.59.47%20PM.png)

## 创建容器方法1

```
-i 表示没有客户端连接，也能保持容器一直运行的状态；
   如果没有-i 就表示没有客户端连接，容器自动关闭

-it 和 -i -t 是一样的

-t表示给容器一些伪的终端，给容器输入一些命令

-t terminal 进入容器内部，分配一些终端

--name表示给容器起名
可以写成     --name=c1
也可以写成   --name c1

/bin/bash 进入容器的初始化指令 (不写也执行这个)
```

![Screen Shot 2022-04-18 at 11.26.04 PM](docker/Screen%20Shot%202022-04-18%20at%2011.26.04%20PM.png)

```
exit 退出容器
退出之后，又回到了Linux系统，所以称Linux系统为--宿主机


进入docker容器：   docker exec -it 775ajkklkjl /bin/bash
```

![Screen Shot 2022-04-18 at 11.28.48 PM](docker/Screen%20Shot%202022-04-18%20at%2011.28.48%20PM.png)

我可不可以不装虚拟机，直接docker里来个centos的容器，在centos容器里再装一个docker。那就不用在windows装centos的虚拟机了

```
通过 docker run -it 创建的容器，一旦退出(exit)，容器就自动关闭
docker ps 查看正在运行的容器(此时里面为空)
```

![Screen Shot 2022-04-18 at 11.32.02 PM](docker/Screen%20Shot%202022-04-18%20at%2011.32.02%20PM.png)

![Screen Shot 2022-04-18 at 11.34.02 PM](docker/Screen%20Shot%202022-04-18%20at%2011.34.02%20PM.png)

##  创建容器方法2

```
-d 表示后台运行创建容器：容器创建完之后，不会立即进入容器，必须要通过命令才可能进入容器
操作之后，再走exit，容器不会自动关闭

docker ps -a 命令里面的status下的up表示在c2正在运行

docker exec -it c2 /bin/bash 表示进入容器内部
 t 表示伪终端

ll  表示查看容器内部
```

![Screen Shot 2022-04-18 at 11.42.04 PM](docker/Screen%20Shot%202022-04-18%20at%2011.42.04%20PM.png)

![Screen Shot 2022-04-18 at 11.45.08 PM](docker/Screen%20Shot%202022-04-18%20at%2011.45.08%20PM.png)

![Screen Shot 2022-04-18 at 11.46.54 PM](docker/Screen%20Shot%202022-04-18%20at%2011.46.54%20PM.png)

![Screen Shot 2022-04-19 at 8.06.51 AM](docker/Screen%20Shot%202022-04-19%20at%208.06.51%20AM.png)

![Screen Shot 2022-04-19 at 8.10.02 AM](docker/Screen%20Shot%202022-04-19%20at%208.10.02%20AM.png)

![Screen Shot 2022-04-19 at 8.11.26 AM](docker/Screen%20Shot%202022-04-19%20at%208.11.26%20AM.png)

![Screen Shot 2022-04-19 at 8.12.29 AM](docker/Screen%20Shot%202022-04-19%20at%208.12.29%20AM.png)

# 数据卷

数据卷：理解为一个文件/目录

![Screen Shot 2022-04-19 at 8.30.56 AM](docker/Screen%20Shot%202022-04-19%20at%208.30.56%20AM.png)

![Screen Shot 2022-04-19 at 8.32.31 AM](docker/Screen%20Shot%202022-04-19%20at%208.32.31%20AM.png)

![Screen Shot 2022-04-19 at 8.35.13 AM](docker/Screen%20Shot%202022-04-19%20at%208.35.13%20AM.png)

# 配置数据卷

![Screen Shot 2022-04-19 at 8.54.53 AM](docker/Screen%20Shot%202022-04-19%20at%208.54.53%20AM.png)

![Screen Shot 2022-04-19 at 8.56.22 AM](docker/Screen%20Shot%202022-04-19%20at%208.56.22%20AM.png)

![Screen Shot 2022-04-19 at 8.59.44 AM](docker/Screen%20Shot%202022-04-19%20at%208.59.44%20AM.png)

![Screen Shot 2022-04-19 at 9.01.49 AM](docker/Screen%20Shot%202022-04-19%20at%209.01.49%20AM.png)

![Screen Shot 2022-04-19 at 9.03.57 AM](docker/Screen%20Shot%202022-04-19%20at%209.03.57%20AM.png)

![Screen Shot 2022-04-19 at 9.05.36 AM](docker/Screen%20Shot%202022-04-19%20at%209.05.36%20AM.png)

![Screen Shot 2022-04-19 at 9.06.21 AM](docker/Screen%20Shot%202022-04-19%20at%209.06.21%20AM.png)

![Screen Shot 2022-04-19 at 9.07.58 AM](docker/Screen%20Shot%202022-04-19%20at%209.07.58%20AM.png)

![Screen Shot 2022-04-19 at 9.09.01 AM](docker/Screen%20Shot%202022-04-19%20at%209.09.01%20AM.png)

![Screen Shot 2022-04-19 at 9.10.11 AM](docker/Screen%20Shot%202022-04-19%20at%209.10.11%20AM.png)

![Screen Shot 2022-04-19 at 9.11.25 AM](docker/Screen%20Shot%202022-04-19%20at%209.11.25%20AM.png)

![Screen Shot 2022-04-19 at 9.13.38 AM](docker/Screen%20Shot%202022-04-19%20at%209.13.38%20AM.png)

![Screen Shot 2022-04-19 at 9.17.31 AM](docker/Screen%20Shot%202022-04-19%20at%209.17.31%20AM.png)

# 容器之间数据交换

![Screen Shot 2022-04-19 at 9.18.53 AM](docker/Screen%20Shot%202022-04-19%20at%209.18.53%20AM.png)

![Screen Shot 2022-04-19 at 9.21.22 AM](docker/Screen%20Shot%202022-04-19%20at%209.21.22%20AM.png)

![Screen Shot 2022-04-19 at 9.23.10 AM](docker/Screen%20Shot%202022-04-19%20at%209.23.10%20AM.png)

![Screen Shot 2022-04-19 at 9.25.00 AM](docker/Screen%20Shot%202022-04-19%20at%209.25.00%20AM.png)

# 进阶/方便的容器之间的数据交换

**C3挂了，c1和c2还能通信**：因为宿主机中的数据卷还存在，数据卷容器相当于多做一次处理，实际上还是关联到宿主机

因为是 c1、c2、c3 都和宿主机设置了数据卷，c3 只是其中一个节点

![Screen Shot 2022-04-19 at 9.33.19 AM](docker/Screen%20Shot%202022-04-19%20at%209.33.19%20AM.png)

## 配置数据卷容器

- 如果不设置左边的(:左边的，就是/volume左边的)，docker会自动分配那部分

![Screen Shot 2022-04-19 at 9.39.56 AM](docker/Screen%20Shot%202022-04-19%20at%209.39.56%20AM.png)

![Screen Shot 2022-04-19 at 9.41.21 AM](docker/Screen%20Shot%202022-04-19%20at%209.41.21%20AM.png)

![Screen Shot 2022-04-19 at 9.42.30 AM](docker/Screen%20Shot%202022-04-19%20at%209.42.30%20AM.png)

![Screen Shot 2022-04-19 at 9.43.40 AM](docker/Screen%20Shot%202022-04-19%20at%209.43.40%20AM.png)

![Screen Shot 2022-04-19 at 9.44.21 AM](docker/Screen%20Shot%202022-04-19%20at%209.44.21%20AM.png)

![Screen Shot 2022-04-19 at 9.46.09 AM](docker/Screen%20Shot%202022-04-19%20at%209.46.09%20AM.png)

![Screen Shot 2022-04-19 at 9.47.29 AM](docker/Screen%20Shot%202022-04-19%20at%209.47.29%20AM.png)

![Screen Shot 2022-04-19 at 9.49.32 AM](docker/Screen%20Shot%202022-04-19%20at%209.49.32%20AM.png)

![Screen Shot 2022-04-19 at 9.50.47 AM](docker/Screen%20Shot%202022-04-19%20at%209.50.47%20AM.png)

![Screen Shot 2022-04-19 at 11.43.17 AM](docker/Screen%20Shot%202022-04-19%20at%2011.43.17%20AM.png)

![Screen Shot 2022-04-19 at 11.44.06 AM](docker/Screen%20Shot%202022-04-19%20at%2011.44.06%20AM.png)

![Screen Shot 2022-04-19 at 11.44.59 AM](docker/Screen%20Shot%202022-04-19%20at%2011.44.59%20AM.png)

![Screen Shot 2022-04-19 at 11.47.33 AM](docker/Screen%20Shot%202022-04-19%20at%2011.47.33%20AM.png)

# docker应用部署

## mysql部署

![Screen Shot 2022-04-19 at 11.52.08 AM](docker/Screen%20Shot%202022-04-19%20at%2011.52.08%20AM.png)

![Screen Shot 2022-04-19 at 11.53.08 AM](docker/Screen%20Shot%202022-04-19%20at%2011.53.08%20AM.png)

![Screen Shot 2022-04-19 at 11.56.24 AM](docker/Screen%20Shot%202022-04-19%20at%2011.56.24%20AM.png)

![Screen Shot 2022-04-19 at 12.06.19 PM](docker/Screen%20Shot%202022-04-19%20at%2012.06.19%20PM.png)

![Screen Shot 2022-04-19 at 12.18.02 PM](docker/Screen%20Shot%202022-04-19%20at%2012.18.02%20PM.png)

![Screen Shot 2022-04-19 at 12.18.43 PM](docker/Screen%20Shot%202022-04-19%20at%2012.18.43%20PM.png)

![Screen Shot 2022-04-19 at 12.19.29 PM](docker/Screen%20Shot%202022-04-19%20at%2012.19.29%20PM.png)

![Screen Shot 2022-04-19 at 12.20.06 PM](docker/Screen%20Shot%202022-04-19%20at%2012.20.06%20PM.png)

![Screen Shot 2022-04-19 at 12.20.32 PM](docker/Screen%20Shot%202022-04-19%20at%2012.20.32%20PM.png)

![Screen Shot 2022-04-19 at 12.21.09 PM](docker/Screen%20Shot%202022-04-19%20at%2012.21.09%20PM.png)

## tomcat部署

以后项目写完了，直接放到tomcat目录下面，就完成了部署的工作

![Screen Shot 2022-04-19 at 12.22.52 PM](docker/Screen%20Shot%202022-04-19%20at%2012.22.52%20PM.png)

![Screen Shot 2022-04-19 at 12.23.26 PM](docker/Screen%20Shot%202022-04-19%20at%2012.23.26%20PM.png)

![Screen Shot 2022-04-19 at 12.25.31 PM](docker/Screen%20Shot%202022-04-19%20at%2012.25.31%20PM.png)

![Screen Shot 2022-04-19 at 12.25.45 PM](docker/Screen%20Shot%202022-04-19%20at%2012.25.45%20PM.png)

![Screen Shot 2022-04-19 at 12.26.07 PM](docker/Screen%20Shot%202022-04-19%20at%2012.26.07%20PM.png)

![Screen Shot 2022-04-19 at 12.26.22 PM](docker/Screen%20Shot%202022-04-19%20at%2012.26.22%20PM.png)

## Nginx部署

![Screen Shot 2022-04-19 at 12.29.09 PM](docker/Screen%20Shot%202022-04-19%20at%2012.29.09%20PM.png)

![Screen Shot 2022-04-19 at 12.30.00 PM](docker/Screen%20Shot%202022-04-19%20at%2012.30.00%20PM.png)

![Screen Shot 2022-04-19 at 12.30.53 PM](docker/Screen%20Shot%202022-04-19%20at%2012.30.53%20PM.png)

![Screen Shot 2022-04-19 at 12.32.32 PM](docker/Screen%20Shot%202022-04-19%20at%2012.32.32%20PM.png)

![Screen Shot 2022-04-19 at 12.33.43 PM](docker/Screen%20Shot%202022-04-19%20at%2012.33.43%20PM.png)

![Screen Shot 2022-04-19 at 12.34.24 PM](docker/Screen%20Shot%202022-04-19%20at%2012.34.24%20PM.png)

![Screen Shot 2022-04-19 at 12.34.56 PM](docker/Screen%20Shot%202022-04-19%20at%2012.34.56%20PM.png)

![Screen Shot 2022-04-19 at 12.35.08 PM](docker/Screen%20Shot%202022-04-19%20at%2012.35.08%20PM.png)

![Screen Shot 2022-04-19 at 12.36.16 PM](docker/Screen%20Shot%202022-04-19%20at%2012.36.16%20PM.png)

![Screen Shot 2022-04-19 at 12.35.31 PM](docker/Screen%20Shot%202022-04-19%20at%2012.35.31%20PM.png)

![Screen Shot 2022-04-19 at 12.36.27 PM](docker/Screen%20Shot%202022-04-19%20at%2012.36.27%20PM.png)

## Redis部署

![Screen Shot 2022-04-19 at 12.38.31 PM](docker/Screen%20Shot%202022-04-19%20at%2012.38.31%20PM.png)

![Screen Shot 2022-04-19 at 12.38.40 PM](docker/Screen%20Shot%202022-04-19%20at%2012.38.40%20PM.png)

![Screen Shot 2022-04-19 at 2.55.53 PM](docker/Screen%20Shot%202022-04-19%20at%202.55.53%20PM.png)

![Screen Shot 2022-04-19 at 2.56.07 PM](docker/Screen%20Shot%202022-04-19%20at%202.56.07%20PM.png)

![Screen Shot 2022-04-19 at 2.57.07 PM](docker/Screen%20Shot%202022-04-19%20at%202.57.07%20PM.png)

![Screen Shot 2022-04-19 at 2.57.26 PM](docker/Screen%20Shot%202022-04-19%20at%202.57.26%20PM.png)