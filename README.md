#The project introducing

> 项目使用JavaScript语言在nodejs平台上编写，基于tcp协议，采用命令行式的人机交互方式，查看所有在线用户，显示用户ip和名字，支持可以向所有在线局域网用户聊天，和某一在线用户聊天，聊天记录保存到本地数据库(模拟数据库形式)，基于ip地址屏蔽某一用户，查看本地记录以及向指定目标ip发送<1M的文件


# 完成期间所遇到的问题:
	
# 项目业务逻辑
	![](http://i.imgur.com/ULTOcaW.png)

# 项目描述:
- 使用net模块实现网络数据的传输
- 使用fs,path模块对文件的读写
- 使用readline模块实现命令行输入
- 使用blue.js实现对数据库的操作
- 对常规协议封装，数据库增删改查操作封装，配置文件的封装，数据库数据原型的封装，以及面向对象的数据库操作方式(oodb)，和对命令行输入操作封装以实现解耦合，随没有达到最大的解耦合，但是在一定程度上提高了代码的可读性，维护性，扩展性

# 使用方法
> 开启服务器 server.js

> 开启客户端 client.js

- c    获取当前在线人数信息
- b:*:xxxxx  向所有在线客户端发送xxxxx
- p:targetIp:xxx  向targetIp发送xxx
- e  退出
- lookrecord   查看记录
- s:ip:文件路径  向指定目标ip发送文件

- client.config   配置文件


		{
		    "prohibitIp":["666666"], // 拒绝接受信息的ip列表
		    'fileReceiveDir':'./download',  // 默认文件接收位置
		      // 服务器
		    "host":"127.0.0.1", 
		    "port":3030           
		}