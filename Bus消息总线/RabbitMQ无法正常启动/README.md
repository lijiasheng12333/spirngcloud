# 安装rabbitMQ成功后，启动失败
最开始按步骤在rabbit_server-3.8.16\sbin目录下使用命令`rabbitmq-plugins enable rabbitmq_management`
结果提示  
![启动错误](https://github.com/lijiasheng12333/spirngcloud/blob/main/Bus消息总线/RabbitMQ无法正常启动/pic/mistake1.png)  
查阅资料发现大概率是因为rabbitMQ日志默认是存放在c盘用户名文件夹下，而本人电脑用户名是中文，因此会出现错误。  
解决办法，修改日志默认存放位置。  
首先使用管理员打开cmd命令，进入sbin目录下，然后尝试安装服务，并删除服务。  
![step1](https://github.com/lijiasheng12333/spirngcloud/blob/main/Bus消息总线/RabbitMQ无法正常启动/pic/step1.png)  
然后是关键的一步，先创建一个文件夹用于存放日志并在这里设置日志路径。  
![step2](https://github.com/lijiasheng12333/spirngcloud/blob/main/Bus消息总线/RabbitMQ无法正常启动/pic/step2.png)  
完成上述步骤后，再一次尝试安装服务，这一次会出现这样的效果。  
![step3](https://github.com/lijiasheng12333/spirngcloud/blob/main/Bus消息总线/RabbitMQ无法正常启动/pic/step3.png)  
这时候，我再次访问localhost:15672发现还是不行，进入本地服务，发现rabbitmq服务未启动，因此启动服务。
![step4](https://github.com/lijiasheng12333/spirngcloud/blob/main/Bus消息总线/RabbitMQ无法正常启动/pic/step4.png)  
完成！