# ACER-TX520-Hackintosh-Opencore
使用OpCore simplify GUI 自动生成 

宏碁 TravelMate TX520-G2-MG ，这个EFI 支持  macOS Sonoma 14.8.3（23J220） i5-8250u 15.6寸 黑苹果

需要在BIOS-Main-Touchpad 下改为 Basic
## Configuration

| 描述   | 详情                                                  |
| ------------------- | ------------------------------------------- |
| 电脑型号      |  宏碁TravelMate TX520-G2-MG|
| 处理器           | 英特尔酷睿i5-8250U处理器     |
| 内存              | 8 GB 2400 MHz DDR4              |
| SATA    | HP SSD S700 500GB| 原装固态硬盘是支持的但空间太小不适合双系统| 
| 显卡 | Intel UHD Graphics 620 2048 MB                     |
| 声卡         | Realtek ALC255     |
| 无线网卡       | Intel AC 7265  | 


## 正常工作的设备

- 显卡
    - 亮度调节: `SSDT-PNLF.aml` + `BrightnessKeys.kext`
- 无线网卡
    - 不需要拆机更换无线网卡
- 触摸板
    - 手势完美(需要在BIOS-Main-Touchpad 下改为 Basic
- 摄像头
    - 摄像头可以正常休眠
- 声卡 Realtek ALC255 
    - 自编译声卡ID：3
- 显示器
    - 修复休眠唤醒黑屏: 重命名 `_LID=>XLID` 配合使用 `SSDT-LID-Wake-After-Sleep.aml`
- 键盘
    - 音量和亮度调节 已经可以使用


## 不能正常工作的设备

- 独显 MX130

