java
====


#简介
--------
安装JDK和JRE的puppet模块。



#安装
-----

##安装概述
* 安装JDK
* 配置环境变量
	
#配置

将安装文件放置在files文件夹内。

编辑init.pp文件

```
    java::setup { "example.com-jdk_6u35":
      ensure        => 'present',
      source        => 'jdk-6u35-linux-x64.tar.gz',
      deploymentdir => '/home/example.com/apps/jdk-6u35',
      user          => 'example.com',
      pathfile      => '/home/example.com/.bashrc'
    }
```

#参数说明
------


`ensure`
保持软件包的状态

`source`
源码包的名称。    
**只支持tar.gz和.gz格式的文件**


`deploymentdir`
安装目录

`user`
用户


`pathfile`
更新变量信息

#测试
------------
Puppet版本
Puppet 2.6.x, 2.7, 3.x.

已测试系统
* CentOS 5.9
* CentOS 6.4
* Debian 6.0 
* Ubuntu 12.04
* OpenSuSE 12.1 (x64)

