# dianping
黑马点评
简化版大众点评
项目简介:本项目是一个类似于大众点评等打卡类APP的点评类项目。实现了短信登陆、探店点评、优惠券秒杀、每日签到、好友关注、粉丝关注博主后，主动推送博主的相关博客等多个模块。
用户可以浏览首页的推荐内容，搜索附近的商家，查看商家的详情和评价以及发表探店博客，抢购商家发布的限时秒杀商品。

## 克隆完整项目
git clone https://github.com/haopengmai/dianping.git
## 前端环境部署
nginx-1.18.0   启动nginx.exe
## 后端环境部署
在application.yaml文件中，Mysql和Redis的配置需要自行更改

## 后端部分功能做了优化
### 优化点1:高并发的情境下采用消息队列RabbitMQ来优化秒杀下单，减轻数据库的压力。
### 优化点2:登录模块，暂时使用个人用户邮箱发送短信验证码->（后续使用阿里云短信服务实现短信登录功能)
### 优化点3:使用Redis中的ZSET数据结构+时间窗口思想，进行用户限流