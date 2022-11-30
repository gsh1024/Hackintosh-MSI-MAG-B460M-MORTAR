# 微星 B460M 迫击炮 + i5 10400

## 版本

[0.8.7](/guoshuohui/Hackintosh-MSI-MAG-B460M-MORTAR/0.8.3)

[0.8.4](/guoshuohui/Hackintosh-MSI-MAG-B460M-MORTAR/main)

[0.8.3](/guoshuohui/Hackintosh-MSI-MAG-B460M-MORTAR/0.8.3)

## 简介

该 EFI 基于 `XIII` 的 [OC 0.8.3 Dev](https://heipg.cn/efi/msi-b460m-mortar-i5-10500-uhd630-rx570-opencore-083-dev.html) 修改，他已不再维护，为了能 “完美” 匹配最新的 [Monterey 12.5.1 OC 0.8.4 Dev](https://heipg.cn/macos/macos-monterey-12-5-1-21g83-opencore-084-clover-r5148-firpe.html) 引导镜像，我对其 EFI 的 `OC` 和 `Kexts` 进行了升级，下载和安装之前，请 `仔细` 阅读本文所有内容，特别是 `注入三码` 和 `USB定制`。

- 着重解决了启动时各类 `OCS: No schema xxx` 报错信息。
- 修改主题为 `Acidanthera\GoldenGate`，更加简洁漂亮，适配 4K 显示。
- 去掉了开机跑码功能，启动效果更具 “MacOS 风格”。
- 启动选择等待时间由 5 秒 改为 3 秒。
- 关闭了开机声音，没啥用。

## 硬件：

- i5 10400 带核显
- MSI MAG B460M MORTAR（迫击炮无 WIFI 版）
- 美商海盗船复仇者LPX DDR4 2666 8 * 2
- 西部数据 WD Blue SN570 500GB SSD M2
- 蓝宝石 RX460 896SP 免驱
- Fenvi FV-HB1200 免驱

以上是我的配置，除了 CPU、主板、显卡、硬盘、网卡有一定的要求之外，其他配置你可以随意。

## 运行

目前所有的功能，包括驱动、休眠、双系统、硬解、蓝牙、WiFi、投送、随航等，都正常且运行非常稳定，MSI 的 B460 迫击炮算得上是目前最完美的黑苹果主板之一了。

## 注意

- 一定要自己 `注入三码`，不要用我当前 `EFI` 中的，这样才能正常的使用 `App Store` 等服务，教程参考 [OpenCore生成三码，修复苹果服务无法使用](https://heipg.cn/tutorial/macserial-and-iservice-opencore.html)，这里我推荐文中的 `GenSMBIOS` 工具。
- 不是所有的机箱 USB 都和我的一样，一定要自己定制，可以参考[USB定制新姿势：Windows下定制黑苹果USB接口详细攻略](https://heipg.cn/tutorial/customize-usb-port-windows.html)，很简单。
- CPU 核显驱动最高只能到 10 代，之后的 CPU 请自带独显。
- 独显支持列表参考 [2022年黑苹果macOS Big Sur/Monterey显卡支持列表，持续更新中](https://heipg.cn/tutorial/gpu-support-for-hackintosh.html)
- 硬盘避免使用三星的，例如 970EVO/PLUS/PRO，其他品牌诸如 PM981(a)/PM991/S2200/A2000/600P 等也尽量不要，如果你刚好用了三星的，可以参考 [如何升级三星970EVO Plus固件以支持黑苹果安装](https://heipg.cn/tutorial/updating-970evo-plus-for-macos.html)。
- 网卡选择博通免驱的就 OK，牌子随意，推荐 `Fenvi`，大部分时候用网线，对 WIFI 速率要求不高，主要是给蓝牙设备、投送、随航用。
- 双系统最好用双硬盘，`EFI` 完美隔离，可以避免非常多麻烦事。

## 疑问

不知有无什么方法让我的 RX 460 在 Geekbench 5 中跑满？目前才 2 万多分。。。