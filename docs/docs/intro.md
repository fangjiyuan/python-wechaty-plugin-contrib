---
title: "介绍"
sidebar_position: 1
---

# 介绍

![](/img/intro/plugin-intro.png)

插件系统提供了模块化的管理，能够让不同业务的代码隔离开，特别是针对于复杂的业务。

在处理不同业务时，通常选择将指定业务封装成一个插件，实现业务的高内聚低耦合。wechaty社区也欢迎大家贡献自己的插件，从而快速实现某些简单功能。

## 快速开始

* 安装

```shell
pip install wechaty wechaty-plugin-contrib
```

* 使用

```python
from wechaty import Wechaty
from wechaty_plugin_contrib import DingDongPlugin
```

## 特性

* 简易settings加载和存储，让开发者轻松实现插件配置扩展
* wechaty-ui：一个快速开发高服用性的插件UI框架
* 内置scheduler，并提供简易方法实现90%的任务调度
* 基于Quart构建Web服务，支持快速Http/WebSocket服务开发能力
* ...

## Wechaty-UI 设计理念

[wechaty-ui](http://github.com/wechaty/wechaty-ui)是近段时间发起的一个项目，旨在为插件提供高扩展性的UI开发能力，同时统一的UI框架可适用于多语言Wechaty，甚至是可直接复用一套UI，管理不同版本Wechaty插件的UI。设计的整体的框架图如下所示：

![](/img/intro/plugin-structure.png)

1. Bot是可以提供UI能力的，并且多种语言Wechaty都是可以支持这种能力，其中包括go-wechaty，py-wechaty，ts-wechaty等。
2. UI能力是通过WebService的方式暴露出去，使用Http协议。
3. wechaty-ui提供统一的UI管理能力，能够自动生成不同插件的UI配置管理界面，以及UI界面能力。

## 插件列表

| 插件名称                                                     | 作者                                  | 功能描述                                           |
| ------------------------------------------------------------ | ------------------------------------- | -------------------------------------------------- |
| [DingDongPlugin](https://github.com/wechaty/python-wechaty-plugin-contrib/blob/master/src/wechaty_plugin_contrib/contrib/ding_dong_plugin.py) | [@wj-Mcat](http://github.com/wj-Mcat) | 发送`ding`，回复`dong`                             |
| [InfoLoggerPlugin](https://github.com/wechaty/python-wechaty-plugin-contrib/blob/master/src/wechaty_plugin_contrib/contrib/info_logger.py) | [@wj-Mcat](http://github.com/wj-Mcat) | 根据关键字打印好友或群聊的信息，并保存到日志当中   |
| [InfoDownloaderPlugin](https://github.com/wechaty/python-wechaty-plugin-contrib/blob/master/src/wechaty_plugin_contrib/contrib/info_downloader.py) | [@wj-Mcat](http://github.com/wj-Mcat) | 通过浏览器下载所有好友以及群聊的相关信息           |
| [OnFriendShipPlugin]()                                       | [@wj-Mcat](http://github.com/wj-Mcat) | 处理好友申请的事件                                 |
| [OnRoomJoinPlugin]()                                         | [@wj-Mcat](http://github.com/wj-Mcat) | 处理群聊群友加入的事件                             |
| [RasaRestPlugin]()                                           | [@wj-Mcat](http://github.com/wj-Mcat) | Rasa Server的Connector连接工具，可实现与Rasa的打通 |
|                                                              |                                       |                                                    |
|                                                              |                                       |                                                    |
|                                                              |                                       |                                                    |
|                                                              |                                       |                                                    |
|                                                              |                                       |                                                    |

