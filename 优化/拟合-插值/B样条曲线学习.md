# B样条曲线

## 1. 简介和基本定义（这里用的是阶数，可以不看）

![preview](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101309760.jpeg)

![preview](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101325259.jpeg)

![preview](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101310011.jpeg)

## 2. B样条的性质（$\bigstar$这里用的是次数）

[B样条曲线的一些基本性质_何伯特的博客-CSDN博客_b样条曲线性质](https://blog.csdn.net/weixin_43795921/article/details/107808824)



![](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101343632.png)

![img](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101344046.png)



- u的定义域为(u_p, u_n+1)

- **第i+1个控制点Pi只影响区间（ui，ui+p+1）之间的曲线**（p是基函数的次数）

- **在任何一个节点区间 [ui, ui+1), 最多有 p+1个p 次基函数非零，即：Ni-p,p(u), Ni-p+1,p(u), Ni-p+2,p(u), …, Ni-1,p(u) 和 Ni,p(u)。（且这些基函数的累加和为1）**
- 强制第一个节点和最后一个节点的**重复度**为p+1，那么产生的曲线就会分别与第一个控制点和最后一个控制点的第一边和最后一边相切，且曲线会经过第一个控制点和最后一个控制点。也就是所谓的clamped B样条曲线。



## 3. 插值：追赶法反求控制点

[三次B样条插值及其误差分析 - 豆丁网 (docin.com)](https://www.docin.com/p-1511846558.html)



![image-20220810133723120](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101337230.png)

![image-20220810133850118](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101338193.png)

![image-20220810133919609](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101339695.png)

![image-20220810133931098](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101339162.png)





![image-20220810135347017](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101353084.png)

![image-20220810135355260](https://cdn.jsdelivr.net/gh/acryan54/images@main/pic/202208101353320.png)

- u的定义域为(u_p, u_n+1)

- 注意首末型值点与u_p, u_n+1 (u_m-p)对应，中间型值点和节点一一对应，于是u_p, ... , u_n+1 (u_m-p) 对应 V_0, ... V_r, 