# ACER-TX520-Hackintosh-Opencore
宏碁 TravelMate TX520-G2-MG ，这个EFI 支持 macOS Big Sur 11# TX520-G2-MG i5-8250u 15.6寸 黑苹果

需要在BIOS-Main-Touchpad 下改为 Basic
## Configuration

| 描述   | 详情                                                  |
| ------------------- | ------------------------------------------- |
| 电脑型号      |  宏碁TravelMate TX520-G2-MG|
| 处理器           | 英特尔酷睿i5-8250U处理器     |
| 内存              | 8 GB 2400 MHz DDR4              |
| SATA    | HP SSD S700 500GB| 
| 显卡 | Intel UHD Graphics 620 2048 MB                     |
| 声卡         | Realtek ALC255          |
| 无线网卡       | DW1280A  原生英特尔无线网卡驱动暂未支持，但未来会支持|


## 正常工作的设备

- 显卡
    - 亮度控制快捷键: 需要重命名 _Q01,_Q02 (F1 ~ F12 分别对应 _Q01 ~ _Q0C)，配合使用 `SSDT-BrightKey.aml`
    - 亮度调节: `SSDT-PNLF.aml` + `WhateverGreen.kext`
- 无线网卡
    - 需要拆机更换无线网卡(建议更换dw1820a)
- 触摸板
    - 手势完美(需要在BIOS-Main-Touchpad 下改为 Basic， 驱动'ApplePS2SmartTouchPad.kext’+ `VoodooI2C。kext` + `SSDT-OC-XOSI.aml`)
- 摄像头
    - 蓝牙和摄像头可能需要 `Hackintool.app` 内建usb才能正常休眠
- 声卡 Realtek ALC255 
    - 自编译声卡ID：3
- 显示器
    - 修复休眠唤醒黑屏: 重命名 `_LID=>XLID` 配合使用 `SSDT-LID-Wake-After-Sleep.aml`
- 键盘
    - 音量和亮度调节 已经可以使用


## 不能正常工作的设备

- 独显 MX130
