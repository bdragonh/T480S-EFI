
## 简介

- Lenovo ThinkPad T480s Hackintosh EFI ，包含基础驱动，修改三码后开箱即用。
- 适用版本：macOS Catalina 10.15.5。

- This repository is a working progress of the clover folder used to install catalina on Lenovo ThinkPad T480s.

## 前提

1. 更换硬盘为 Samsung SSD 970 EVO 1TB：
2. 更换网卡为 Fenvi BCM94352Z
3. 更新显示器 2K 8BIT屏幕 (原装屏幕只是1080p 6bit会有严重的色带问题)

## 硬件说明

### 硬件配置

Lenovo ThinkPad T480s

- Intel i7-8550U
- 24GB RAM ( 8G板载 + 16单条 )
- Samsung SSD 970 EVO 1TB
- Fenvi BCM94352Z
- 2K 8BIT屏

### 硬件使用状态

* [x] 集成显卡 UHD620
* [x] 屏幕亮度调节（小太阳）
* [x] 有线网
* [x] 无线网（隔空投屏，隔空投递）
* [x] 蓝牙
* [x] 电池状态 
* [x] hidpi (1440*810 完美）
* [x] 声音
* [x] SD 卡读取
* [x] 触控板（手势完美）
* [x] Fn+F1-F12（FN快捷键完美）
* [x] 小红点
* [x] 雷电3 （没有测试，应该好使。）
* [x] 休眠唤醒
* [x] 个人文件保险箱
* [ ] ~~启动转换助理~~
* [ ] ~~独立显卡 mx150~~
* [ ] ~~指纹识别器~~

## 使用方法

复制EFI到EFI分区并用Clover Configurator App打开config.plist 

修改三码

1. 编辑 `config.plist` 中的 SMBIOS 内容：
    - BoardSerialNumber: 修改示例编码中的 Z 字母为随机数字与字母
    - SerialNumber: 修改示例编码中的 Z 字母为随机数字与字母
    - SmUUID: 随机生成一个 UUID，通过 [https://www.uuidgenerator.net/](https://www.uuidgenerator.net/) 获取

2. 编辑 `config.plist` 中的 RtVariables 内容：

    - MLB：使用上面第一步中修改后的 BoardSerialNumber

3. 编辑 `config.plist` 中的 SystemParameters 内容：
    - CustomUUID：使用第一步中生成的 UUID

## 必装工具

- one-key-hidpi : 一键开启 macOS HiDPI
- ThinkpadAssistant : 开启THINKPAD驱动FN多功能键位
- only-sleep : 不允许MACOS进行休眠，只允许睡眠。 

## 遗留问题

1. Hidpi 只能使用 1440*810，超过此分辨率的情况下休眠后唤醒会花屏（雪花点）
2. 个人文件保险箱 会使用CPU进行加密解密 T2芯片无解 （会拉慢文件IO）
3. 长期休眠后，出现关机自动启动的情况。（假如不使用ONLY-SLEEP.APP进行设置 长期使用会有关机重启的问题）

## 致谢

- GITHUB中黑苹果的所有爱好者们
