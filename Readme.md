# 基于Spring Cloud实现的简易微服务商城
## 一、主要技术栈

SpringBoot+SpringCloud Alibaba+Mysql+MybatisPlus+Nacos+OpenFeign+SpringCloud Gateway+Docker+Nginx

## 二、项目描述

该平台是一个类似网页版淘宝商城，用户可以注册、查询商品、搜索商品、增减购物车商品、下单/取消订单、支付订单等功能。整个项目分为商品、购物车、交易、支付、用户五个业务模块，同时包含网关、api、工具模块common三个功能模块。

## 三、具体实现

1、使用Nacos作为服务注册中心和配置中心，使用OpenFeign实现微服务之间的远程调用，保证各平台的协同工作。

2、统一认证模块中，使用JWT令牌实现无状态登录，结合SpringCloud Gateway实现路由过滤及登录校验，并使用拦截器将用户信息保存到ThreadLocal中实现线程隔离。

3、使用Nacos配置中心实现网关规则热更新。

4、前端采用Nginx部署，实现反向代理和负载均衡。
