# mpv-dark-box

这是一个自制的mpv osc脚本，使用了mpv原生![osc.lua](https://github.com/mpv-player/mpv/blob/master/player/lua/osc.lua)框架，主要视觉风格来自于![MPV-EASY-Player项目](https://github.com/422658476/MPV-EASY-Player/blob/master/mpv-easy-data/osc-style/osc-potplayer-box-knob-or-bar-0.lua)

## 预览

预览1

![预览1](https://github.com/maoiscat/mpv-dark-box/blob/main/preview1.png)

预览2

![预览2](https://github.com/maoiscat/mpv-dark-box/blob/main/preview2.png)

## 使用方法

1. 下载dark-box.lua，放在scripts目录
2. 在mpv.conf中配置osc=no
3. 运行

## 配置说明

与内置皮肤一样，在script-opts中编辑osc.conf来进行参数设置，大部分参数与内置皮肤是通用的，另有以下有几个改动：

1. font     --配置OSC字体
2. layout   --该脚本只有default一种风格
3. logotext --启动时LOGO下显示的文字，支持ASS格式代码
4. 圣诞帽被移除了

## 预览图的配置方案

### mpv.conf

```conf
osc=no
[Auto.Idle]
profile-cond=p["idle-active"]
profile-restore=copy-equal
osd-playing-msg=' '
title=' '
background=1.0
geometry=640
```

### osc.conf

```conf
font=Consolas
logotext={\\1c&H00\\bord0\\fs30\\fn微软雅黑 light\\fscx125}MPV{\\fscx100} 播放器
```

另外自行把mpv.exe的图标替换成空白图标就实现一致效果。
