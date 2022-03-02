# education
将`GOPATH`设置为`/root/go`,拉取项目：
```
cd $GOPATH/src && git clone https://github.com/sxguan/education.git
```
在`/etc/hosts`中添加：
```
127.0.0.1  orderer.example.com
127.0.0.1  peer0.org1.example.com
127.0.0.1  peer1.org1.example.com
```
添加依赖：
```
cd education && go mod tidy
```
运行项目：
```
./clean_docker.sh
```
在`127.0.0.1:9000`进行访问


## fix questions 2022-03-02
* modify GOPATH /root/go/src path 
> ./config.yaml change  /root/go/src to self path . 
* fix dial unix /host/var/run/docker.sock: connect: no such file or directory   
> https://blog.csdn.net/qq_27376871/article/details/109496787
* login account
> admin/123456