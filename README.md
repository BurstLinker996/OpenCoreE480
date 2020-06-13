### ThinkPad E480使用OpenCore安装黑苹果
* 笔记本硬件配置如下：
    * CPU:英特尔® 酷睿™ i5-8250U
     
    * 处理器显卡:Intel® UHD Graphics 620
     
    * 独立显卡:Radeon RX 550（无法驱动，详情看[Catalina/Mojave硬件支持列表](https://blog.daliansky.net/Mojave-Hardware-Support-List.html)）
     
    * 声卡: Conexant SmartAudio HD
     
    * 有线网卡：Realtek RTL8106EUS
     
    * 无线网卡：Realtek RTL8821CE   (无法驱动，更换broadcom网卡，[参考网址](https://www.tonymacx86.com/threads/broadcom-wifi-bluetooth-guide.242423/#post-1664577))
     
#### 结合[官方示例](https://github.com/acidanthera/OpenCorePkg/tree/master/Docs)、[黑果小兵](https://blog.daliansky.net/)以及[cattyhouse](https://github.com/cattyhouse/oc-guide)提供的技术支持，整理出适用于上述机型的OpenCore配置。
#### 注意此仓库OpenCore配置仅适用于上述硬件配置，其他硬件仅供参考。本人成功安装macOS Catalina 10.15.2

## 引导方法：
1. 把整个仓库克隆到临时目录，把仓库目录里的EFI和com.apple.recovery.boot两个文件夹拷贝到OpenCore引导分区。
2. 根据[说明](https://github.com/cattyhouse/oc-guide/blob/master/oc-dmg-install.md)下载macOS Recovery到com.apple.recovery.boot目录下，并且在此目录
下面新建一个隐藏文件 .contentDetails，内容可以随便写, 比如 Mojave Boot From Recovery, 这个名字会出现在OpenCore的启动菜单上.
