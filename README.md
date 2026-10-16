# 硬件学习资料库

个人硬件 / PCB 设计学习资产，用于跨设备同步。仓库为 **私有**。

## 内容

### 学习成果

| 文件 | 说明 |
|---|---|
| `硬件学习路线.md` | 总体学习路线图（分阶段推进） |
| `STM32F103C8T6最小系统板_从零到打样.md` | 从零画第一块 STM32 最小系统板的教程 |
| `ESP32硬件设计指南_精读笔记.md` | Espressif《ESP32 硬件设计指南》精读笔记 |
| `硬件进阶_方向B_EMC与信号完整性笔记.md` | 方向 B 五主题总览：环路辐射 / 地平面分割 / 跨分割 / 去耦 / PDN 阻抗 |
| `硬件进阶_方向B_主题3与5_去耦与PDN笔记.md` | 去耦网络与 PDN 阻抗精读（村田 / Xilinx / TI 三文档对照） |
| `13概念自查清单.html` | 阶段 2 的 13 个核心概念自查清单（可交互） |

### 厂商文档库 `硬件设计指南文档/`

11 篇官方 PDF：

- **基础**：ST AN2586（STM32F10xxx 硬件开发入门）
- **时钟**：ST AN2867（晶振振荡器设计指南）
- **EMC**：TI SZZA009（降低 EMI 的 PCB 设计指南）
- **地平面**：ADI MT-031（地平面与 AGND/DGND）
- **去耦 / PDN**：Murata 数字 IC 电源噪声抑制与去耦应用手册（中 / 英）、Xilinx XAPP623（中 / 英）、TI SPRAC76（Sitara PDN）
- **参考体系**：ESP32 硬件设计指南（中 / 英）

## 在另一台电脑上使用

首次获取：

```bash
git clone https://github.com/Hai299/hardware-study.git
```

日常同步：

```bash
git pull                          # 开工前先拉取
git add -A
git commit -m "更新笔记"
git push
```

## 同步规则说明

本仓库的工作目录里另有约 **38 GB** 无关文件（机械臂 SDK、venv、安装包、培训资料等）
以及凭据文件（`github token.txt`、`账号.txt`）。这些**全部不会**进入版本控制，
由 `.gitignore` 的**白名单机制**保证：先 `/*` 忽略一切，再逐项 `!` 放行。

因此在本地新增学习文件后，需要在 `.gitignore` 的「学习成果」区**登记一行**，
否则该文件不会被同步。

> 换行符由 `.gitattributes` 统一为 LF 存储，跨 Windows / Linux / macOS 不会产生整文件 diff。
