## 燕大终端 (YandaTerminal Reborn) 项目现状公告

发布时间：2026-08-21

为了让【燕大终端】项目在遵循 GPLv3 开源协议的前提下，能够更规范、安全、可持续地维护，我们已完成数字基础设施与项目架构的升级。

---

### 📌 项目现状说明

1. **项目管理与基础设施**
   - 燕大终端（YandaTerminal Reborn）由社区去中心化协同维护。
   - 所有部署节点、官方邮箱 (`yanda_terminal@proton.me`)、Cloudflare 云服务及签名密钥均已集中管理与安全配置。

2. **最新版本与平台策略**
   - 最新 Release **`v0.12.0`** 已发布（版本号已回归正常编号，此前的 `0.19.x` 编号废弃）。
   - 当前支持 **PWA Web 端**（https://yanda.dpdns.org，可安装、支持离线外壳与自动更新）与 **Android APK**（支持 OTA 热更新）。
   - 为保证社区版的可维护性，iOS / HarmonyOS / 桌面端（Tauri）目标已停止维护。鸿蒙 NEXT 与桌面用户可直接使用 PWA 版本，体验一致。

3. **近期更新摘要**
   - PWA 全面升级：标准 Web App Manifest、Service Worker 离线缓存、安装引导与自动更新提示。
   - 微信扫码 MFA 登录流程修复与加固。
   - Web 端自定义头像与背景功能修复。

---

### 📬 联系与参与方式
- **官方邮箱**：`yanda_terminal@proton.me`
- **问题反馈**：欢迎通过 GitHub Issues 或邮件与我们交流。

感谢所有燕大同学的支持！
