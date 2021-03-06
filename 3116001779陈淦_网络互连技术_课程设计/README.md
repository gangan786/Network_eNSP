# 网络互连课程设计

网络拓扑图

![](https://github.com/gangan786/Network_eNSP/blob/master/3116001779%E9%99%88%E6%B7%A6_%E7%BD%91%E7%BB%9C%E4%BA%92%E8%BF%9E%E6%8A%80%E6%9C%AF_%E8%AF%BE%E7%A8%8B%E8%AE%BE%E8%AE%A1/image/%E6%8B%93%E6%89%91%E5%9B%BE.png?raw=true)

需求及所应用的技术

+ 整个网络总共分为四个区，分别是用户区，前端开发区，服务端开发区，最后一个区为模拟公网环境的公共区域。所有在局域网内部的设备均能互相访问，而且对于局域网内的所有终端设备都具有与公网进行通信的能力（NAT）。
+ 其中用户区的用户数量较大，且需要保证该区域要有一定的抗干扰容错性能，减少无用信息对带宽的占用。所以综上考虑三层架构的方式来构建用户区的网络设计，使用VLAN技术将用户群划分为三个区域，并且隔离广播域。使用MSTP多生成树协议防止产生环路。对于充当路由功能的三层交换机之间来说，使用VRRP实现虚拟路由的冗余备份。

+ 在前端开发区除了实现对局域网内所有终端的互相访问之外，还需要对服务端开发区开放的服务进行访问。

+ 在服务端开发区，需要对公网暴露FTP和HTTP服务（NAT Server），实现对外提供业务服务。

+ 对整个路由区域使用OSPF路由协议，实现不同区域之间的互连互通。