###  注意如果网卡用的不是DW1820A，那么需要修改config.plist，可以采用config.plist_without_dw1820a,把此文件重命名为config.plist

# 9600K-ROG-B360I-UHD630 for macOS Catalina（10.15.7）

## 硬件配置

| 硬件      | 型号                                              |
| --------- | ------------------------------------------------- |
| CPU       | i5 9600K                                          |
| 主板      | Asus ROG Strix B360-i                             |
| 内存      | 阿斯加特（Asgard）16GB 3000频率 DDR4 * 2          |
| 固态      | 铠侠（Kioxia）RC10 500GB SSD ,西数黑盘SN750 250GB |
| 显示器    | AOC Q24P2C 23.8英寸2K                             |
| 电源      | 迎广肖邦150w铜牌                                  |
| 散热      | IS40X                                             |
| 机箱      | 迎广肖邦                                          |
| 线材      | 显示器附带DP线                                    |
| 网卡&蓝牙 | DW1820A                                           |

## BIOS设置：

- CFGLock➡️Disabled
- VT-d➡️ Disabled
- 大于4G地址空间解码➡️Enabled
- DVMTPre-Allocated➡️128M
- Systemtime and Alarm Source ➡️Legacy RTC
- SATA模式选择 ➡️AHCI 必须设置
- legacyUSB支持 ➡️Enabled
- XHCIHand-off ➡️Enabled
- 快速启动 ➡️Disabled
- 开启CSM ➡️Disabled
- 安全启动状态 ➡️关闭
- 操作系统类型 ➡️其他操作系统
- 另外在BIOS设置中，cpu选项下注意开启英特尔虚拟化技术,否则mac下面启动docker会报错

## 驱动：

------

**Lilu.kext** 插件 必装

| 设备      |              | kext                                                         |
| --------- | ------------ | ------------------------------------------------------------ |
| 显卡      | UHD630       | WhateverGreen.kext                                           |
| 有线网卡  | Intel® I219V | IntelMausi.kext                                              |
| 声卡      | ALC887       | AppleALC.kext                                                |
| USB       | 按需定制     | XHCI-unsupported.kext USBInjectAll.kext USBPort.kext USBPower.kext |
| Wi-Fi     | DW1820a      | AirportBrcmFixup.kext                                        |
| 蓝牙      | DW1820a      | BrcmBluetoothInjector.kext BrcmFirmwareData.kext BrcmPatchRAM3.kext |
| SMBus设备 |              | VirtualSMC.kext SMCProcessor.kext SMCSuperIO.kext            |

DW1820A驱动参考黑果小兵博客,注意如果网卡用的不是DW1820A，那么需要修改config.plist，可以采用config.plist_without_dw1820a

## 工作情况

- 板载有线网卡
-  板载声卡
-  核显
-  USB
-  Wi-Fi
-  Bluetooth
-  CPU温度
-  风扇转速
-  AirDrop(隔空投递)
-  Handoff(接力)
-  睡眠 唤醒 关机 重启

##### 基本8/9代集显CPU都可以用这一套，记得自己生成三码

