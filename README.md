# 📱 WebADB 控制台 (WebADB Console)

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0006--1511--466X-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0006-1511-466X)
[![WebUSB](https://img.shields.io/badge/Tech-WebUSB%20%2F%20WebADB-10b981)](https://developer.mozilla.org/en-US/docs/Web/API/WebUSB_API)

无需安装 ADB 工具包与电脑驱动，直接通过浏览器（Chrome / Edge 等）与 Android 设备建立 WebUSB 连接，实现一键激活玩机框架、硬件状态检测与自定义 ADB 命令调试。

---

## ✨ 核心特性

- ⚡ **零构建、零依赖、纯静态**：无需 Node.js / Vite 编译，原生 ESM 引入，单 HTML 即可直接运行。
- 🚀 **玩机框架一键激活**：
  - **Shizuku**（全自动路径探测与启动）
  - **Dhizuku**（Device Owner 激活）
  - **雹 Hail / 小黑屋 StopApp / 冰箱 IceBox**（Device Owner 激活）
  - **黑阈 Brevent / Thanox 淘米**（Shell 脚本激活）
- 📶 **Wi-Fi 局域网调试**：一键开启/关闭 5555 端口无线调试。
- 📊 **硬件信息实时看板**：连接成功即时读取并展示设备型号、Android 版本 (API 级别)、电池电量、SELinux 状态。
- ⌨️ **智能命令执行器**：支持自定义任意 ADB 命令，自动剔除粘贴内容中多余的 `adb shell` 前缀，支持回车一键执行。
- 🌐 **双语支持与智能跳转**：`index.html` 自动识别系统语言跳转至中文 (`zh_cn.html`) 或英文 (`en.html`) 界面。
- 🛡️ **100% 本地隐私安全**：所有 ADB 通信纯在浏览器本地内存运行，绝不上报或收集任何用户数据与设备标识。

---

## 🚀 部署指南 (Deployment)

由于本项目为纯静态结构，您可以将其部署在任何静态托管服务中：

### 1. GitHub Pages (推荐)
1. Fork 或克隆本仓库到您的 GitHub 账户。
2. 进入仓库 **Settings** ➡️ **Pages**。
3. **Branch** 选择 `main` / `/(root)` 并保存。
4. 几秒钟后即可获得专属的全球 CDN 访问地址。

### 2. 本地或其他 Web 服务器
直接将项目中的 `index.html`、`zh_cn.html`、`en.html` 放置于 Nginx、Apache、Caddy 或 Cloudflare Pages 的根目录即可。
> ⚠️ **注意**：由于现代浏览器安全策略（WebUSB API），页面必须通过 **HTTPS** 协议或 `http://localhost` 访问。

---

## ⚠️ 免责声明 (Disclaimer)

1. 本工具仅供技术交流与学术学习研究使用。
2. ADB 具备 Android 系统底层特权，请在执行高风险命令前仔细核对。
3. 因用户个人误操作（如卸载关键系统包、误刷分区等）导致的任何软硬件异常，开发者概不承担任何直接或间接责任。

---

## 📄 开源许可 (License)

本项目采用 **[GNU General Public License v3.0 (GPL-3.0)](./LICENSE)** 协议开源。

- 允许自由使用、研究、修改与分发。
- **衍生作品约束**：任何基于本项目二次开发、修改或衍生的作品，在公开发布时必须同样以 GPL-3.0 协议开源。

**作者 (Author)**: [aoooa](https://orcid.org/0009-0006-1511-466X)
