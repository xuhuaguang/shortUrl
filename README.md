## urls 短链接生成服务

#### 此服务实现的想法来自于知乎对于短链接生成的一些讨论。
[https://www.zhihu.com/question/29270034](https://www.zhihu.com/question/29270034)
#### 本人是参考 @iammutex这位大神的想法来实现的，但有所不同的是，为保证同一个长地址每次转出来都是一样的短地址，这位的想法是创建一个临时表，储存最近几个小时内生成的短链接，过期后淘汰。
#### 本人的想法是 创建一个 key-value，key为长连接的md5值，value为该长连接对应的短链接。






## 配置部署


```
# REDIS (RedisProperties)
# Redis数据库索引（默认为0）
spring.redis.database=0
# Redis服务器地址
spring.redis.host=localhost
# Redis服务器连接端口
spring.redis.port=6379
# Redis服务器连接密码（默认为空）
spring.redis.password=

# 连接超时时间（毫秒）
spring.redis.timeout=500
# 指定redis生成器初始值，最小为1，最大为1024
me.eae.urls.idGenerator.RedisIdGenerator.startNum=1
```
## 项目截图

![输入图片说明](https://gitee.com/uploads/images/2018/0408/133706_856b75e2_778825.png "QQ截图20180408133008.png")

转载地址：https://gitee.com/hao_jiayu/urls    如有问题，劳烦通知删除，谢谢。
