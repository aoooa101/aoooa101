# WebADB 控制台

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0006--1511--466X-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0006-1511-466X)

👉 **在线使用**：[https://aoooa101.github.io/aoooa-webadb/](https://aoooa101.github.io/aoooa-webadb/)

基于 WebUSB 的免驱动浏览器端 ADB 工具。用数据线连接手机即可在网页里激活 Shizuku、Dhizuku 或直接运行 ADB 命令。

## 功能

- **框架激活**：支持自动定位启动 Shizuku，以及一键填入 Dhizuku / 雹 (Hail) / 小黑屋 / 冰箱 / 黑阈 / Thanox 的激活指令。
- **无线调试**：一键开启/关闭 5555 端口无线 ADB。
- **设备信息**：连接后自动读取机型、Android 版本、当前电量与 SELinux 状态。
- **自定义命令**：支持输入任意 shell 命令（自动过滤粘贴内容里多余的 `adb shell` 前缀，按回车直接执行）。
- **纯前端运行**：没有后端，不收集数据，通过浏览器原生 WebUSB 接口直连。
- **多语言**：根据浏览器语言自动进入中文或英文页面。

## 部署

项目没有构建步骤，不需要安装 Node.js。直接将 `index.html` 放到任意静态服务器（如 GitHub Pages、Cloudflare Pages 或 Nginx）即可（页面已内置中英文切换，无需额外文件）。

> **注意**：WebUSB API 要求页面必须运行在 HTTPS 环境或 `http://localhost` 下。

## 致谢

本项目重度依赖以下开源项目，特此致谢：

- [ya-webadb](https://github.com/yume-chan/ya-webadb)（@yume-chan/adb 系列）— 浏览器端 ADB 协议实现与 WebUSB 连接层，让"网页里跑 ADB"成为可能（MIT 协议）。
- [esm.sh](https://esm.sh) — ESM 模块公共 CDN 分发服务，提供上述库的在线加载。

## 免责声明

本工具仅供技术研究与个人日常玩机使用。ADB 具有系统底层权限，请在执行高风险命令前自行核对，因误操作导致的设备异常由操作者自行承担。

## 开源协议

本项目采用 [GPL-3.0](./LICENSE) 协议开源。任何基于本项目修改的衍生作品在分发时需保持 GPL-3.0 开源。

作者：[aoooa](https://orcid.org/0009-0006-1511-466X)
