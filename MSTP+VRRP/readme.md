#  MSTP&VRRP

多生成树协议(MSTF)与虚拟路由器冗余协议(VRRP)结合实验



+ 使用了VRRP协议实现当边境路由(网关)宕机的时候，可以使备份路由充当网关的角色，而终端用户对此无感，即实际上网关路由发生了变化，但是用户终端并不需重新设置网关

+ 使用了聚合链路，使得我们可以将多个以太网捆绑为一条逻辑的以太网链路，不仅可以实现链路冗余，还可以实现负载分担

+ 拓扑图

  ![](https://github.com/gangan786/Network_eNSP/blob/master/MSTP+VRRP/image/%E6%8B%93%E6%89%91%E5%9B%BE.png?raw=true)



+ 参考：[https://blog.csdn.net/qq_35428201/article/details/82709137](https://blog.csdn.net/qq_35428201/article/details/82709137)

