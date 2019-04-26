# Update 2019/04/13


-----------------------------------------------------------
## PND
-----------------------------------------------------------

[]关机无法WOL

[]有时候休眠后也无法WOL

[]将现有的遇到的坑的关键点记录下来。。。。 

[]MAC 热键休眠...

-----------------------------------------------------------
[x]固态盘的trim问题。（check2台机）

[x]cpu变频问题,我的是8700k+z370 变频没问题，也是用的typePlugin 最低是0.8Ghz。

[x]鼠标有点飘，，，关闭鼠标加速，，，看看是怎么回事？

[x]//评估office for mac、 wps for mac、office in VM 的方案。。。(WPS for mac)

[x]dummy144.kext的作用?

[x]Mojave是否需要刻意洗白？(填三码) 登录icloud/激活iMessage,Facetime?

[x]测试音频直接从主板驳接是否有声。(音质如何,netease的设置音质配置一下先)

[x]4K 硬解码 如何开启

[x]无线网卡/蓝牙， airdrop handoff

[x]Clover设置启动倒计时3秒进mac 手动干涉进Windows

[x]安装配置开发环境(itrem2、xcode等)

[x]OpenWRT是否可配置第二个时间胶囊给不同的mac使用? 还是共用一个? 

[]//开启B360的HDMI屏显？

[x]精读tonymacx86的教程

[x]Check 家里两条线， 一条DP2DP， 另一条 MiniDP2MiniDP， 是否都有?

[x]macbook 切换英文版，浅色模式， 否则跑Unibeast会出问题

[x]注册tonymacx86

[x]Windows 系统备份 迁移到 ssd 120G，留NVMe的250G给mac系统

[x]蓝宝石 rx 570

[x]//无线网卡和蓝牙套件, 暂时先不买住,airdrop /handoff  暂无吸引力

[x]//89.99 那台机器的 amd 显卡： AMD Radeon(TM) R5 340X (mojave 不可用，新dell拆机)

[x]//尝试在intel B360的集显（HDMI）上安装Mojave (快进入安装界面黑屏无屏显，估计是不支持hdmi)

[x]移植改键的软件过来。

[x]制作一个1T盘的CCC克隆镜像，带efi，recovery，克隆，时间机器的移动盘。

[x]里面虚拟化一个Windows，一些特殊的软件可以 临时开了用，不用切双系统

-----------------------------------------------------------

## Changelog

### 2019/04/13

    初次从MSI的迫击炮的EFI Fork过来的，改动并修补一些。 GPU为蓝宝石矿卡rx570(免驱)
    华擎的这块板为B360的并且没有DP口，hack比较麻烦，所以直接买了块矿卡直接驱动



### 2019/04/13

    Update Clover 4919 && Support HDMI、DVI
    
### 2019/03/31

    1.Update Clover 4915 fix applertc patch for 10.14.4+. thanks to RodionS
      Cleanup iGPU values and fix force reboot when wakes up with an HDMI connected in 10.14+
    2.Remove ‘Fix RTC _STA bug’ patch

### 2019/03/28

    1、Exclude new framebuffer patchers because of its instability
    2、Do not support HDMI、DVI for the moment

### 2019/03/25
    
    1、Update Clover 4895 Support macOS Mojave 10.14.4
    2、Compatible with the latest BIOS version && Support DP、HDMI、DVI
    3、Update USB Patches
    4、Replace VBoxHfs-64.efi with HFSPlus.efi
    5、Update AppleALC && Lilu && WhateverGreen
    


### 2019/01/25

    1、Fix Audio (Layout ID 15) and use Hackintool driver UHD630
    2、Update Clover version 4862 support macOS 10.14.4 beta1
    3、It is highly recommended to upgrade to the latest version to solve USB problems






CPU:i5 8400
GPU:UHD630
SSD:SAM 960PRO
SMBIOS:2018 Mac mini


MSI B360m Mortar Hackintosh EFI FILE

    macOS Mojave 10.14.4

    Clover version:4895

    WhateverGreen 1.2.7

    USB3.0 5G

    HibernationFixup 1.2.4

    Lilu version:1.3.5

    AppleALC:1.3.6
    
    
# Recommend to modify your SMBIOS
Link of tutorial：http://sleele.com/2019/03/21/smbios/
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/SMBIOS.png)
    
### Recommend BIOS version 7B23v12
MSI B360 BIOS download link https://cn.msi.com/Motherboard/support/B360M-MORTAR
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/BIOS.png)

# Detail:
 [My Blog: sleele.com/2018/12/01/hackintosh/ ](http://sleele.com/2018/12/01/hackintosh/ "Blog")

![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-5.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-2.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-8.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-12.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-13.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-6.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-4.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-7.png)
![示例图片加载失败](https://raw.githubusercontent.com/SuperNG6/pic/master/Hackintosh%20images/image-1.png)



# Kenny's Hackintosh 坑录

- Clover Configurator 的挂载EFI分区功能无法使用，点了没反映，，，搞得我还装一个专门的傻逼工具EFI Mounter v3的什么装载工具。。。其实是因为我当时下载的 Clover Configurator 版本太低 4.x，，，升级到5.x 问题fix。。。顺滑无比。

- 安装的时候卡无法显示，B360的HDMI无解（事实上，很多HDMI都不太好，建议买带DP的主板，或直接上蓝宝石的显卡），后来买了块蓝宝石的rx570 直接解决问题

- 无法识别intel核显，与clover有关（直接用的微星迫击炮的b360的clover，导致集显无法驱动） ，删掉相关的的显卡的驱动注入代码即可在mac识别核显，

- 无法开启很h264/h265的4K硬解，clover configurator 里面Graphics的Inject Intel 勾选， ig-platform-id选择UHD630第三个ID“0x3E9B0007”，有个教程里建议用第一个ID“0x3E910003”说快一些，测试过用第一个id会导致h265可以硬解，h264无法硬解，，， 用第三个id"0x3E9B0007"可完美硬解 （再次测试，确实如此）

- dummy144.kext 这个与是否可以开启核显无关。。。不是必须的，测试后可以删除这个驱动

- Devices的 IntelGFX的 Fake ID 看看是否有必要选择正确？。。。 0x3E928086 （可以不填，不是必须的）

- 声卡 驱动