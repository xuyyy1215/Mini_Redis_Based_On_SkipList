# Mini_Redis_Based_On_SkipList
## 目标： 

1.搞定跳表，实现底层的存储数据结构。

2.使用类redis语句，进行增删改查。

3.使用网络编程技术，将redis部署到服务器。

4.负载均衡技术。

### 1.跳表

提高跳表的查询效率：使用随机的方法确定每个节点将占据的层次数。随机化方法有待调整。

3.29日，跳表的结构基本完成。

缺陷：对于模板的支持不够好，虽然使用了泛型编程，但是现在只支持string，int，等基本类型。但是使用其他自定义类型还是需要重新定义比较器才行。

### 2.sql语句

使用set 进行存储于修改
使用get 进行查询
使用del 进行删除
使用load 从disk中读取数据
使用dump 将数据存入disk

### 3.服务器部署

使用socket 或者libevent，部署客户端和服务器。

4.2日，完成服务器的部署。使用socket技术，主要需要关注的是，socket连接断开后，client与server需要及时发现连接断开并销毁连接对象，退出线程。

### 4.负载均衡

....
