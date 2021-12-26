<!--
 * @Author: HK560
 * @Date: 2021-12-26 21:07:29
 * @LastEditTime: 2021-12-27 00:30:00
 * @LastEditors: HK560
 * @Description: 
 * @FilePath: \NorthStarCN_WIKI\Doc\hostServer.md
 * My Blog: https://blog.hk560.top
-->
# 如何架设服务器？
## 须知
NorthStarCN 提供架设服务器方案。通过架设服务器，使用NorthStasrCN的玩家将能在服务器列表中看到使用NorthStarCN架设的服务器房间，并加入游玩。

使用NorthStarCN专用的服务器端允许您在不必使用完整客户端的情况下托管服务器，从而使得服务器更轻量级，更易于长期托管。专用的服务器端仍在开发测试中，所以在使用的同时，预计会出现一些bug。


## 前提条件
- 一台至少 4核4G内存 的服务器或主机（我们知道这要求很高，但目前2c的服务器仍存在不少问题无法架设，未来可能会支持2c）
- 该服务器或主机拥有公网IP
- 该服务器或主机使用windows10的系统（目前不支持win7，linux下wine端正在研究开发中）

## 步骤
请严格按顺序执行以下步骤
1. 给服务器系统安装DX11组件，并各种微软通用运行库
2. 安装橘子客户端Origin
3. 下载 **专用精简的的服务端游戏本体([下载连接](https://share.weiyun.com/Xibwduya) @超级牛肉干 提供)** 
   
   或者你直接把完整的泰坦陨落2下载下来也行...
4. 下载最新的NorthStarCN客户端，并将客户端文件覆盖到第3.步的本体文件中
5. 运行Origin注册表恢复器，这个可以再网上搜索下载
6. 为你的服务器进行配置，请参考[Wiki](https://github.com/R2NorthstarCN/NorthStarCN_WIKI/wiki/%E5%BF%AB%E9%80%9F%E5%B8%AE%E5%8A%A9%E6%96%87%E6%A1%A3)中的【服务器/私人比赛房间 配置】项目
7. 为你的服务器配置端口，或有需要则也设置端口转发：
    - 开启 37015 至 37020 的端口 协议为UDP 
    - 开启 `认证端口` 协议为TCP ，此`认证端口`即 第5.步中你为`ns_player_auth_port`设置的端口号，默认是8081
8. 启动并登陆Origin
9. 点击运行第4.步最后本体文件中r2ds.bat即可启动服务端
   
  ![](https://cdn.jsdelivr.net/gh/HK560/MyPicHub@master/res/pic/Snipaste_2021-12-26_22-28-24.jpg)

如图显示这样，没有其他额外的错误提示即算成功。

接下来就可以打开游戏看看服务器列表有没有你的服务器
    


------
## 待补充完善。。。。