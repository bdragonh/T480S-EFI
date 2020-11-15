
## 简介

- Lenovo ThinkPad T480s Hackintosh EFI ，基于OC包含基础驱动，修改三码后开箱即用。
- 适用版本：macOS Catalina 10.15.x,可以正常升级10.15的小版本 （不支持BIG SUR不要升级）
- 带OC引导界面主题  （按空格可以 显示恢复引导）  SIP状态 ENABLE 系统更安全

## 前提

1. 更换硬盘为 Samsung SSD 970 EVO 1TB：
2. 更换网卡为 Fenvi BCM94352Z
3. 更新显示器 2K 8BIT屏幕 (原装屏幕只是1080p 6bit会有严重的色带问题)

## 硬件说明

### 硬件配置

Lenovo ThinkPad T480s

- Intel i7-8550U
- 24GB RAM ( 8+16 )
- Samsung SSD 970 EVO 1TB
- Fenvi BCM94352Z
- 2K 8BIT屏

### 硬件使用状态

* [x] 集成显卡 UHD620
* [x] 有线网
* [x] 无线网（隔空投屏，隔空投递）
* [x] 蓝牙 
* [x] 电池状态 
* [x] hidpi (1440*810 完美）
* [x] 声音
* [x] SD 卡读取
* [x] 触控板（多点触摸手势全开）
* [x] Fn+F1-F12 PtrSc（FN快捷键完美,PtrSc支持需要设置键盘快捷键 默认为CTRL+COMMAND+3 改为 F13）
* [x] 小红点
* [x] 雷电3 （没有测试，应该好使。）
* [x] 休眠唤醒
* [x] 个人文件保险箱 （打开后 假如看不到启动项可以按F3）
* [x] USB全部端口 （多个USB不会出现供电问题）
* [ ] ~~启动转换助理~~ （双系统需要自己手动安装 不要使用启动转换助理）
* [ ] ~~独立显卡 mx150~~ 
* [ ] ~~指纹识别器~~ 

## 使用方法

- 复制EFI到EFI分区 编辑EFI/OC/config.plist 修改SystemSerialNumber、SystemUUID、MLB三码
- 改快捷键设置  【将屏幕图片存储成文件】 改为 PrtSc 备注：看到快捷提示为F13即可

## 必装工具

- one-key-hidpi : 一键开启 macOS HiDPI
- ThinkpadAssistant : 开启THINKPAD驱动FN多功能键位

## 遗留问题

1. Hidpi 只能使用 1440*810，超过此分辨率的情况下休眠后唤醒会花屏 （还好14寸屏幕 最完全的分辨率就是1440*810）
2. 个人文件保险箱 会使用CPU进行加密解密 因为没有T2芯片 （TPM芯片 不支持苹果系统 无解 只能闲置让CPU解码）
3. 双系统WIN10 设备管理器会有两个其它设备无法识别 （蓝牙 USB 独立显卡 指纹 都能正常工作 不影响正常使用）

## 致谢

- MSzturc/ThinkpadAssistant https://github.com/MSzturc/ThinkpadAssistant
- daliansky/OC-little https://github.com/daliansky/OC-little
- neobi281/T480s-OC-Hackintosh https://github.com/neobi281/T480s-OC-Hackintosh
- GITHUB中黑苹果的所有爱好者们
