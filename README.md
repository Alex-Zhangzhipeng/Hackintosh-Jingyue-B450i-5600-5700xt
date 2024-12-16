# Hackintosh-Jingyue-B450i-5600-5700x

## 1. 项目简介

此项目提供了适用于 **[精粤 B450i]** 的 Hackintosh EFI 文件，基于 OpenCore 引导。支持 macOS **Sequoia 15.x** 的安装和使用。

## 2. 硬件支持

以下是适配的硬件清单：

| 硬件组件     | 型号                           | 兼容性       |
| ------------- | ------------------------------ | ------------ |
| 处理器       | AMD Ryzen 5 5600               | ✅ 完美支持  |
| 核显         | 如果有请使用NootedRed            | 无 |
| 独显         | Rx5700xt 红魔                  | ✅完美支持   |
| 无线网卡      |Intel AX200  （OCLP）           | ✅ 不完美支持  |
| 声卡         | Realtek ALC897                 | ✅ 完美支持  |
| 硬盘         | WD SN550                       | ✅ 完美支持  |

> **注意：** 请确保硬件与表格中的兼容性一致，否则可能需要额外修改 EFI。

## 3. 环境要求

- macOS 版本：**Sequoia 15.x**
- OpenCore 版本：**1.0.1**
- BIOS 设置：
  - 关闭安全启动 (Secure Boot)
  - 关闭CSM支持，否则会导致进入系统后自动重启
  - 启用 AHCI 模式
  - 禁用 VT-d
  - 启用 XHCI Hand-off

## 4. 安装指南

### 4.1 准备工作

1. 下载 macOS 安装镜像并制作启动 U 盘。
2. 将此仓库中的 EFI 文件夹复制到启动 U 盘的 EFI 分区内。

### 4.2 BIOS 设置

按照上方 "环境要求" 部分调整 BIOS。

### 4.3 安装 macOS

1. 插入启动 U 盘，启动时选择 U 盘引导。
2. 使用 OpenCore 菜单选择安装 macOS。
3. 按提示完成安装。

### 4.4 替换 EFI

安装完成后，将此仓库中的 EFI 文件夹复制到目标硬盘的 EFI 分区，替换原有文件。

## 5. 功能支持与已知问题

### 5.1 功能支持

- Wi-Fi 和蓝牙：✅（支持 Intel AX200）（15以后需要OCLP，具体操作参考Bilibili）
- 声卡：✅（使用 AppleALC 注入 ID：13）
- 睡眠与唤醒：✅（仅支持电源键唤醒）

### 5.2 已知问题

- 睡眠唤醒无法使用键盘直接唤醒

## 6. 注意事项

1. 本 EFI 文件仅供学习和研究使用，请勿用于商业用途。
2. 请定期更新 OpenCore 和 Kexts 以获取最新功能和修复。

## 7. 鸣谢

特别感谢以下项目和社区：

- [OpenCore 开发团队](https://github.com/acidanthera)
- [Dortania 安装指南](https://dortania.github.io/)
- [黑苹果社区](https://www.tonymacx86.com/)

**声明：此项目为个人分享，仅供学习交流，请尊重版权和法律。**
