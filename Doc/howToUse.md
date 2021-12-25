<!--
 * @Author: HK560
 * @Date: 2021-12-25 11:03:31
 * @LastEditTime: 2021-12-25 22:49:38
 * @LastEditors: HK560
 * @Description: TTF2NorthStar使用翻译
 * @FilePath: \NorthStarCN_WIKI\Doc\howToUse.md
-->
# NorthstarClient（北极星客户端）帮助文档

## 基础使用步骤
1. 下载NorthStarCN最新版本文件,你可以在[这里下载](https://github.com/R2NorthstarCN/R2NorthstarCN_Launcher/releases)
2. 复制所有解压后的文件到游戏的根目录中 (目前仅支持origin客户端)
   - Steam – 打开 Steam>找到 Titanfall 2，将鼠标移动到游戏名称上，同时鼠标右键单击>在弹出的菜单中选择管理，再点击浏览本地文件。
   - Origin – 找到你的游戏安装目录（Titanfall2.exe在的地方）
3.	(可选) 如果想添加启动项，请新建文件名为 ns_startup_args.txt 的文本文件并在文本中添加相关参数
4.	点击 NorthstarLauncher.exe 运行启动

在加载成功打开游戏后，在游戏主界面你将会看到一条警告信息。提醒您使用NorthStar将自动发送由Origin账号信息生成的Token至NorthStar的MasterServers进行身份验证并用于多人游玩服务.请仔细阅读信息！
![info](https://cdn.jsdelivr.net/gh/HK560/MyPicHub@master/res/pic/Snipaste_2021-12-25_18-47-43.jpg)
>要使NorthStar正常工作，它需要通过NorthStar的主服务器进行身份验证。将会发送您的Origin账号的部分信息(如用户名）至主服务器MasterServer，账户信息不会被存储或用于任何其他目的。但MasterServer可以由任何人设置架设，请注意你所使用的NorthStar设置的MasterServer是否安全可信！

>如果您同意这一点，在该信息点击确定。可以随时在模组菜单中更改此选项。

接下来如图点击 運行 NorthStarCN 即可進入大廳
![](https://cdn.jsdelivr.net/gh/HK560/MyPicHub@master/res/pic/20211225224108.png)


## 关于模组(MOD)

客户端默认安装了三个模组，位于 Titanfall2\R2Northstar\mods 目录中。 你可以通过主菜单底部的模组按钮来访问他们。
- Northstar.Client - 各种用户界面和客户端更改，用以修复游戏错误并添加对模组的额外支持
- Northstar.Custom -额外游戏模式和武器，如泰坦投掷、感染和捉迷藏模式
- Northstar.CustomServers - 托管使用附加匹配设置的服务器的基本模组

## 服务器列表

客户端附带了服务器列表功能，可用于连接社区托管的服务器。
将鼠标悬停在服务器名称上会显示服务器启用了哪些模组以及这些模组的版本。
每个服务器都可以通过单击其名称连接游戏。
单击下方的“刷新”按钮，可以刷新服务器列表。
![](https://cdn.jsdelivr.net/gh/HK560/MyPicHub@master/res/pic/20211225224254.png)
## 如何直连服务器
如果服务器设置为私人模式且未显示在服务器列表中，则可以通过以下方式从控制台直接连接到该服务器：:
1.	按~打开命令控制台。如果您绑定了其他按键，则可以在“控制>设置>按键绑定”中更改它
2.	输入 connect <服务器ip地址>:<端口号> (默认端口号为37015)
例如：connect 127.0.0.1:37015

如果是游戏原版客户端想加入 (只有启用了 ns_auth_allow_insecure 1的服务器支持该功能):
1.	打开Origin，单击Titanfall 2并单击设置图标。
2.	点击 游戏属性 ，然后点击 进阶启动选项
3.	添加参数  +bind "按键" "connect <服务器ip地址>:<端口号>"(例如+bind "F12" connect 127.0.0.1:37015)
4.	打开游戏并选择单人游戏，例如挑战
5.	按下你在第三步中绑定的按键

## 游戏模式
- Sandbox（沙盒）
类似gmod ，但并没有还原
- Gun Game（枪械模式）
击杀敌人来获取其他武器直至游戏胜利
- Titan Tag
在泰坦中赚取分数，你可以通过摧毁别人的泰坦重新获得泰坦
- Infection（感染模式）
幸存者死亡时将会被感染。
- Frontier War（边防战争）
摧毁敌方的采集机，保护己方的采集机。
- Amped Killrace
从获得旗子开始，死亡之前击杀越多得分越高，游戏结束时得分最多的人获胜
- Fastball
侵入控制中心来赢得回合胜利并复活已死亡的队友
- Competitive CTF
CTF with custom settings for Comp games.

<!-- ## 参数
用于编辑listen server 或者de
|参数名  |注释  |
|---------|---------|
|ns_auth_allow_insecure     |    将此值保留为0，除非您希望允许用户在没有主服务器(MasterServer)身份验证/检查的情况下加入     |
|ns_erase_auth_info     |     将此值保持为1，除非您经常进行游戏测试，并发生游戏崩溃。这样您就不必通过每次都进行主服务器验证    |
|ns_masterserver_hostname     |    主服务器的主机名     |
|ns_player_auth_port     |     可以是任意端口，但请确保它是通过tcp端口转发的    |
|ns_report_server_to_masterserver     |    此服务器是否应向主服务器报告本身     |
|ns_report_sp_server_to_masterserver     |     如果服务器在单人地图上启动，是否应向主服务器报告自身    |
|ns_server_name     |    服务器名称     |
|ns_server_desc     |   服务器描述      |
|ns_server_password     |   服务期密码      |
 -->

## 建立私人比赛房间服务器
要在Northstar上建立私人比赛（房间），请在游戏大厅并按下Private Match（私人比赛）。
虽然创建了一局比赛房间，但其他人仍然无法加入，因此您需要开放2个端口以允许其他人加入。


> 默认情况下，您需要转发的端口为37015-37020 UDP和8081 TCP，如果端口正常工作，您的服务器将会显示在服务器列表中，并且其他客户端能够连接到您的服务器。


## 开启独立的服务器端
专用的服务器端允许您在不必使用完整客户端的情况下托管服务器，从而使得服务器更轻量级，更易于长期托管。专用的服务器端仍在开发测试中，所以在使用的同时，预计会出现一些bug。
>NorthStarCN团队正在整合体积更小的仅适合用于作为服务端的文件，待整合完毕你可以使用其在您的服务器部署，之后下载链接会在此发布。

要在Northstar中启用服务器端, 使用 -dedicated参数加载NorthstarLauncher.exe。你可以手动添加这个参数，也可以使用 r2ds.bat批处理文件来完成这个操作。

当使用服务器端时,游戏参数将从 ns_startup_args_dedi.txt 和 ns_startup_args.txt中加载

### 服务器端补充说明

> 目前，服务器端仍然需要DirectX 11才能正常工作，这通常需要一个物理GPU，尽管程序在使用时几乎不使用GPU的处理能力，但这可能是一个需要修复的问题，尤其是在无GPU的设置上。因此，添加启动参数 -softwared3d11 可强制DirectX在软件模式下运行。
> 虽然这不是理想情况，但它是目前真正服务器端的最佳解决方案。令人惊讶的是程序几乎不使用任何CPU时间，尽管它占用大约1GB的RAM。
> 关于RAM的占用，服务器端目前也占用了大量RAM，通常为1.5-2GB；预计会随着后期的开发而降低。

# 服务器/私人比赛房间 配置
无论您使用的是私人比赛还是服务器端，都希望您至少稍微修改一下默认配置。虽然我确实认为默认配置设置得非常完善了，但是更改服务器的名称或密码，或是增加服务器的tickrate是您需要做的事情。

可以在R2Northstar/mods/Northstar.CustomServers/mod/cfg/autoexec_ns_server.cfg中修改服务器配置，它将在服务器启动时执行。

以下是一系列可用于服务器配置的变量和命令：

|参数名称  |描述  |默认值  |
|---------|---------|---------|
|ns_server_name     |您的服务器在服务器列表中的名称，不支持中文|     "Unnamed Northstar Server"    |
|ns_server_desc     |  您的服务器在服务器列表中的描述，不支持中文|"server description"|
|ns_server_password     |如果客户端直接连接并且您使用的是不安全的身份验证，则加入服务器所需的密码|""|
|ns_report_server_to_masterserver     |您的服务器是否向主服务器报告自身，以便身份验证和在服务器列表中显示|1|
|ns_report_sp_server_to_masterserver|设置单人模式中，您的服务器是否向主服务器报告自身
|ns_masterserver_hostname|MasterServer域名|"tf2cn.wolf109909.top"|
|ns_auth_allow_insecure     |允许客户端在不使用主服务器进行身份验证的情况下加入您的服务器。主服务器目前是允许客户端直接连接到您的IP而不是通过服务器列表进行验证|    0     |
|ns_erase_auth_info     |您的服务器是否应该在使用身份验证信息后清除该验证信息，这对于游戏开发非常有帮助，但通常应保持为1|     1    |
|ns_player_auth_port     |用于服务器本地身份验证服务器的端口，这是我们前面转发的TCP端口|8081|
|everything_unlocked     |是否在服务器上解锁所有物品、武器等|1|
|ns_should_return_to_lobby     |游戏结束后，服务器是否应返回私人比赛大厅，如果为0，则将转到游戏列表中的下一个地图/模式|1|
|net_chan_limit_mode     |如果为0，则不限制单个客户端的网络通道处理时间。如果为1，则踢出超时的客户端。如果为2，则在控制台中记录超时的客户端|2|
|net_chan_limit_msec_per_sec     |在net_chan_limit_模式下触发响应之前，客户端每秒可以使用的服务器网络通道处理时间的毫秒数|10|
|base_tickinterval_mp     |在服务器上运行每个tick之间的延迟，tickrate将为1除以该值|0.016666667|
|sv_updaterate_mp     |服务器每秒向已连接的玩家发送信息的最大次数，如果玩家的cl_updaterate_mp值低于服务器的数值，则其速率与服务器同步|20|
|sv_max_snapshots_multiplayer     |本地存储用于重播的快照数，数值应设置为sv_updaterate_mp*15|300|
|net_data_block_enabled|不太确定这个，有听过数据块传输会有安全问题吗？没有发现禁用后有任何影响|0|
|host_skip_client_dll_crc     |服务器是否允许已修改client.dll的客户端连接游戏，用于铁驭颜色的编辑MOD|1|
|sv_querylimit_per_sec|客户端每秒可以发送到此服务器而不会被阻止的无连接数据包的数量|10|


-------
## 其他说明

以上内容均翻译自[NorthStar官方WIKI](https://github.com/R2Northstar/Northstar/wiki)，并进行了适当的补充修改。
目前文章较混乱，后期会整理。


下面是一些其他我们想说的。
### 关于无法连接游玩
需要注意的是目前NorthStar的多人联机基本都是基于起源引擎自带的局域网联机的，控制台输入connect 命令来连接主房间。

所以如果进入不了别人的房间很有可能是房主的ip并非公网ip或者没有设置端口转发之类的，国内的网络环境较差，各种复杂的原因都有可能。

所以想要确保能正常使用游玩NorthStar，请尽量使服务器地址和客户端地址ip为公网ip,并设置好端口转发。


**其他信息待补充**