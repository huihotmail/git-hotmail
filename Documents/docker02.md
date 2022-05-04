就就docker02

# docker镜像原理

docker镜像的本质是文件

Bootfs rootfs fs: file system

Bootfs:内核是一样的

rootfs：不一样(厂商改动的是这一部分 )

不可以在Linux的系统上，安装一个windows的docker，因为内核不同，不好复用

tomcat镜像是暴露给外面用户看到的，其实还包括：jdk rootfs镜像。所以tomcat镜像会很大，比直接下载要大一些，因为是个叠加的结构

下一层镜像可以给上一层镜像复用

只读：是不可以修改。如果可以修改，别人就不可以复用了

![Screen Shot 2022-04-19 at 5.44.38 PM](docker02/Screen%20Shot%202022-04-19%20at%205.44.38%20PM.png)

![Screen Shot 2022-04-19 at 5.53.27 PM](docker02/Screen%20Shot%202022-04-19%20at%205.53.27%20PM.png)

![Screen Shot 2022-04-19 at 5.54.19 PM](docker02/Screen%20Shot%202022-04-19%20at%205.54.19%20PM.png)

![Screen Shot 2022-04-19 at 5.54.45 PM](docker02/Screen%20Shot%202022-04-19%20at%205.54.45%20PM.png)

![Screen Shot 2022-04-19 at 5.54.59 PM](docker02/Screen%20Shot%202022-04-19%20at%205.54.59%20PM.png)

![Screen Shot 2022-04-19 at 5.55.22 PM](docker02/Screen%20Shot%202022-04-19%20at%205.55.22%20PM.png)

![Screen Shot 2022-04-19 at 5.56.19 PM](docker02/Screen%20Shot%202022-04-19%20at%205.56.19%20PM.png)

![Screen Shot 2022-04-19 at 5.56.28 PM](docker02/Screen%20Shot%202022-04-19%20at%205.56.28%20PM.png)

# docker镜像的制作/dockerfile

## 容器转换为镜像(了解)

镜像不可以传输，但是将镜像转换为的压缩文件可以传输

目录挂载，就不会被写入到镜像

目录是通过数据卷的方式传进来的，commit提交的时候，数据卷是不会生效的

![Screen Shot 2022-04-19 at 6.00.32 PM](docker02/Screen%20Shot%202022-04-19%20at%206.00.32%20PM.png)

![Screen Shot 2022-04-19 at 10.10.08 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.10.08%20PM.png)

![Screen Shot 2022-04-19 at 10.12.27 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.12.27%20PM.png)

![Screen Shot 2022-04-19 at 10.12.58 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.12.58%20PM.png)

![Screen Shot 2022-04-19 at 10.14.10 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.14.10%20PM.png)

![Screen Shot 2022-04-19 at 10.14.31 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.14.31%20PM.png)

![Screen Shot 2022-04-19 at 10.16.46 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.16.46%20PM.png)

![Screen Shot 2022-04-19 at 10.19.04 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.19.04%20PM.png)

![Screen Shot 2022-04-19 at 10.20.11 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.20.11%20PM.png)

## dockerfile

Docker file是用来制作镜像的文件

![Screen Shot 2022-04-19 at 10.23.19 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.23.19%20PM.png)

![Screen Shot 2022-04-19 at 10.23.33 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.23.33%20PM.png)

![Screen Shot 2022-04-19 at 10.33.44 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.33.44%20PM.png)

![Screen Shot 2022-04-19 at 10.35.20 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.35.20%20PM.png)

![Screen Shot 2022-04-19 at 10.42.09 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.42.09%20PM.png)

## dockerfile案例

![Screen Shot 2022-04-19 at 10.28.06 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.28.06%20PM.png)

![Screen Shot 2022-04-19 at 10.46.27 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.46.27%20PM.png)

/ 表示工作目录，centos进入的是 / 目录

![Screen Shot 2022-04-19 at 10.29.13 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.29.13%20PM.png)

## 自定义centos

指定当前dockerfile的文件路径： -f

设置新的镜像的名称和版本 ： -t![Screen Shot 2022-04-19 at 10.50.25 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.50.25%20PM.png)

![Screen Shot 2022-04-19 at 10.51.55 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.51.55%20PM.png)

![Screen Shot 2022-04-19 at 10.52.50 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.52.50%20PM.png)

![Screen Shot 2022-04-19 at 10.54.15 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.54.15%20PM.png)

![Screen Shot 2022-04-19 at 10.57.26 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.57.26%20PM.png)

![Screen Shot 2022-04-19 at 10.58.13 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.58.13%20PM.png)

## dockerfile案例：部署springboot

alt + p:传文件 sftp 

![Screen Shot 2022-04-19 at 10.59.31 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.59.31%20PM.png)

![Screen Shot 2022-04-19 at 10.59.39 PM](docker02/Screen%20Shot%202022-04-19%20at%2010.59.39%20PM.png)

```
到maven下的package打包，然后出现下图的build success
```



![Screen Shot 2022-04-19 at 11.33.00 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.33.00%20PM.png)

![Screen Shot 2022-04-19 at 11.33.13 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.33.13%20PM.png)

![Screen Shot 2022-04-19 at 11.33.22 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.33.22%20PM.png)

![Screen Shot 2022-04-19 at 11.36.49 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.36.49%20PM.png)

![Screen Shot 2022-04-19 at 11.33.37 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.33.37%20PM.png)

![Screen Shot 2022-04-19 at 11.34.05 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.34.05%20PM.png)

![Screen Shot 2022-04-19 at 11.34.54 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.34.54%20PM.png)

![Screen Shot 2022-04-19 at 11.35.31 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.35.31%20PM.png)

将jar包添加到dockerfile 容器中，一启动容器，就有了

![Screen Shot 2022-04-19 at 11.39.51 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.39.51%20PM.png)

![Screen Shot 2022-04-19 at 11.40.07 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.40.07%20PM.png)

![Screen Shot 2022-04-19 at 11.41.19 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.41.19%20PM.png)

![Screen Shot 2022-04-19 at 11.41.41 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.41.41%20PM.png)

![Screen Shot 2022-04-19 at 11.42.50 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.42.50%20PM.png)

![Screen Shot 2022-04-19 at 11.43.36 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.43.36%20PM.png)

# Docker compose

![Screen Shot 2022-04-19 at 11.45.43 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.45.43%20PM.png)

![Screen Shot 2022-04-19 at 11.47.22 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.47.22%20PM.png)

![Screen Shot 2022-04-19 at 11.47.38 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.47.38%20PM.png)



![Screen Shot 2022-04-19 at 11.55.15 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.55.15%20PM-0384514.png)

app里面部署了springboot的项目，之前通过镜像直接启动容器

之后装了nginx之后，通过反向代理，来访问容器里面的springboot项目

所以：直接通过nginx反向代理来访问app

![Screen Shot 2022-04-19 at 11.55.31 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.55.31%20PM.png)

![Screen Shot 2022-04-19 at 11.56.17 PM](docker02/Screen%20Shot%202022-04-19%20at%2011.56.17%20PM.png)

![Screen Shot 2022-04-20 at 12.08.09 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.08.09%20AM.png)

![Screen Shot 2022-04-20 at 12.09.13 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.09.13%20AM.png)

## 做nginx的反向代理

![Screen Shot 2022-04-20 at 12.10.18 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.10.18%20AM.png)

![Screen Shot 2022-04-20 at 12.11.21 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.11.21%20AM.png)

![Screen Shot 2022-04-20 at 12.12.49 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.12.49%20AM.png)

![Screen Shot 2022-04-20 at 12.13.11 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.13.11%20AM.png)

![Screen Shot 2022-04-20 at 12.13.58 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.13.58%20AM.png)

# docker私有仓库搭建

s![Screen Shot 2022-04-20 at 12.16.43 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.16.43%20AM.png)

![Screen Shot 2022-04-20 at 12.18.49 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.18.49%20AM.png)

![Screen Shot 2022-04-20 at 12.18.07 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.18.07%20AM.png)

![Screen Shot 2022-04-20 at 12.19.54 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.19.54%20AM.png)

![Screen Shot 2022-04-20 at 12.20.57 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.20.57%20AM.png)

# docker上传 

上传到私有仓库

![Screen Shot 2022-04-20 at 12.22.22 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.22.22%20AM.png)

![Screen Shot 2022-04-20 at 12.23.02 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.23.02%20AM.png)

![Screen Shot 2022-04-20 at 12.24.39 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.24.39%20AM.png)

![Screen Shot 2022-04-20 at 12.26.57 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.26.57%20AM.png)

# docker拉取

![Screen Shot 2022-04-20 at 12.28.00 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.28.00%20AM.png)

![Screen Shot 2022-04-20 at 12.28.20 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.28.20%20AM.png)

# docker和虚拟机的区别

![Screen Shot 2022-04-20 at 12.32.02 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.32.02%20AM.png)

![Screen Shot 2022-04-20 at 12.31.35 AM](docker02/Screen%20Shot%202022-04-20%20at%2012.31.35%20AM.png)