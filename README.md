docker 学习笔记


docker  镜像(images)  容器(container)  仓库(registry)

1、常用命令
    
    docker -v  client version
    
    docker version  Client info Server info 如果没有server信息 说明服务没有起来
    
    docker pull  Elasticsearch     拉去镜像
    
    docker run   镜像名称     启动后就为容器
    
    docker logs  [OPTIONS] CONTAINER 查看日志
    
    docker images   查看镜像
    docker image ls 
    
    docker ps 查看正在运行的容器
    docker ps -a  查看所有运行过的容器 和 正在运行的容器
    
    docker rmi [-f可选参数 强制]   nginx | [containerid]  删除镜像
    docker rm  移除container    用ps -a 查看
     
    
    docker -p 80:80   端口映射
    docker -v   挂存储卷
  
    
    docker exec -it  containerid(容器ID)
    docker stop containerid(容器ID)
    
    
    docker container prune  删除所有未运行的容器 
  
    
    docker run -d -p 3306:3306\  -d 后台运行  -p 端口映射  
      -v /soft/mysql/my.cnf:/etc/mysql/mysql.conf.d/mysqld.cnf\ -v 挂起配置文件 加载配置文件的顺序是先container内优先 
      -v /soft/mysql/data:/var/lib/mysql\  挂起 数据存储位置映射到本地目录位置  
      -e MYSQL_ROOT_PASSWORD=123456 --name mymysql mysql:5.7.18\  
        
  2、创建仓库
  
  
  
  
    