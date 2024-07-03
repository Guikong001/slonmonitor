**[English](https://github.com/Guikong001/PID-Bark-monitor/blob/main/README_en.md)**

## 使用方法

### 本脚本部分

下载本仓库脚本sljiankong，给予运行权限后，使用 ./sljiankong 即可使用。也可以将文件通过root权限放置到/usr/bin下供所有用户使用。

非root用户可以保存在自己的脚本目录下，添加到环境变量即可。

### Bark设置

在iOS app stroe下载Bark后，获取Bark app内的密钥内容，将该密钥通过 -m 选项传递给脚本即可使用。

如果使用自行搭建的Bark推送服务器，使用-s 选项将地址传递给脚本即可。注意，如果服务器为https://abc.example.com ，只需要传递abc.example.com即可，不要加https。同时不支持http://服务器。

## 命令目录

`用法: sljiankong [选项]... 

选项:

  -p PID列表    添加pid编号，可以添加多个，使用;隔开，如添加多个PID，请把所有PID使用英文单引号包裹

  -t 标题        更换推送标题

  -c 监控间隔    监控间隔（单位：秒）

  -w 进程间隔    当前正在运行进程的监控间隔（单位：秒）

  -m 密钥        设置Bark推送服务的密钥

  -s 主机        设置为你的自定义Bark服务器

  -h, --help     显示此帮助信息并退出

  -v, --version  显示版本信息并退出`

<br/>

## 用途

可以用于监测生信分析过程中需要长时间运行的计算程序。例如本人在SNP监测中，需要长时间多线程使用GATK 4进行变异检测。可以用于监测当前的变异检测过程。对任务结束时间有一个大致的了解。

<br/>

## 后续优化计划：

1、细化进程状态的获取

2、密钥存储功能
