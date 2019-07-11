# speech-robot

本项目已结束，基本不会再更新

项目相关信息列出如下:
+ 开发板为 6818
+ 板载系统为 Linux
+ 项目关注点在 Linux 的应用层
+ 涉及到的知识点主要是 文件I/O 线程

如果想通过其他开发板复现本项目，需要更改本项目的配置文件 [project.h](/inc/project.h)

需要修改的地方如下

+ MMAP_LENGTH 需要定义为开发板的屏幕尺寸大小
+ UI_XXX_XXX_PATH 需要更改为开发板上相应图片的路径
+ PICTS_MAX_LEN 为[相册](pic.c)中的图片总数
+ PICT_LOAD_PATH 为[相册](pic.c)的图片存储路径
+ MY_SERVER_IP 为提供语音识别电脑的 IP
+ [游戏](game.c)需要使用另外一个 [fb_2048 的项目](https://github.com/greedyhao/fb_2048)的内容，需要下载下来

项目整体结构如下

```
.
├── build.sh        旧版编译脚本
├── common.c
├── download.sh
├── game.c          游戏
├── imgs            图片文件目录
├── inc
├── lib
├── main.c
├── Makefile
├── music.c         音乐播放器
├── others
├── pic.c           相册
├── project_set.c   项目整体架构建设
├── README.md
├── sound.c         语音控制
├── upload.sh
└── video_player.c  视频播放
```

others/asr_record_demo 这个文件就是用来提供语音识别的，提供5个关键字 启动游戏 播放音乐 播放视频 启动相册 退出，使用时电脑时间需要在 2016 年

others/alsa.tar.gz 需要安装到开发板

-----

# 项目进程

这是学校安排在粤嵌实训时的项目，目前是第三天，觉得还有点意思

## 第二天

完成项目整体框架的搭建

## 第三天

+ 更换了系统主题UI
+ 实现了音乐播放功能
+ 实现了相册切换功能

## 第四天

+ 完成视频的播放暂停

## 第五天

+ 完成游戏的功能

## 第六天

+ 完成语音控制
