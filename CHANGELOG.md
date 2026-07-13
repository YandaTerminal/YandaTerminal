# Changelog

## v0.11.0 (2026-07-13)

### 🚀 新功能 / Features
_(无变更 / No changes)_

### 🐛 修复 / Bug Fixes
_(无变更 / No changes)_

### 🔧 其他 / Other Changes
_(无变更 / No changes)_

---

**Full diff**: https://github.com/YandaTerminal/yanda-terminal/compare/v0.11.0...v0.11.0

### 下载 / Download

| Platform | File |
|----------|------|
| Android | `app-release.apk` |
| iOS | `yanda-terminal-ios.ipa` |
| HarmonyOS | `entry-default-unsigned.hap` |
| Windows | `YandaTerminal_0.11.0_x64-setup.exe` |
| Linux | `YandaTerminal_0.11.0_amd64.AppImage` |
| macOS | `YandaTerminal_0.11.0_aarch64.dmg` |

> PWA: https://yanda.dpdns.org


## v0.11.0 (2026-07-13)

### 🚀 新功能 / Features
_(无变更 / No changes)_

### 🐛 修复 / Bug Fixes
_(无变更 / No changes)_

### 🔧 其他 / Other Changes
_(无变更 / No changes)_

---

**Full diff**: https://github.com/YandaTerminal/yanda-terminal/compare/v0.11.0...v0.11.0

### 下载 / Download

| Platform | File |
|----------|------|
| Android | `app-release.apk` |
| iOS | `yanda-terminal-ios.ipa` |
| HarmonyOS | `entry-default-unsigned.hap` |
| Windows | `YandaTerminal_0.11.0_x64-setup.exe` |
| Linux | `YandaTerminal_0.11.0_amd64.AppImage` |
| macOS | `YandaTerminal_0.11.0_aarch64.dmg` |

> PWA: https://yanda.dpdns.org


## v0.11.0 (2026-07-13)

### 🚀 新功能 / Features
- feat(tauri): 实现与 Android 原生客户端的全部功能对等 / feat(tauri): achieve full feature parity with Android native client
  1. Secure storage (CRITICAL): Rust keyring crate wraps OS credential store
  2. Grade/exam foreground polling: notify-foreground.ts implements setInterval +
  3. Settings UI: grade/exam notification toggles now visible on Tauri.
  4. App lifecycle: sdk-provider.tsx listens to tauri://focus to refresh
  5. Deep links: tauri-plugin-deep-link registered with ysuclient:// scheme.
- feat(android): 实施 setSkipSystemProxy 以进行直接连接旁路 / feat(android): implement setSkipSystemProxy for direct connect bypass
- feat(login): 在对话框中显示技术错误并提供可读的详细信息 / feat(login): show technical errors in dialog with readable detail
- feat(login): 对用户名输入进行反跳验证码检查 / feat(login): debounced captcha check on username input
- feat: 实施 Tauri 桌面无操作适配器 / feat: implement Tauri desktop no-op adapters
- feat: Tauri 桌面端口、多平台构建、删除 obfuscate-web / feat: Tauri desktop port, multi-platform builds, remove obfuscate-web
- feat: Tauri 桌面移植 + Android CI + 分析修复 / feat: Tauri desktop port + Android CI + analysis fixes
- feat(harmony): 实现 OTA 热更新 CapacitorUpdater 桥接 / feat(harmony): Implement OTA hot update CapacitorUpdater bridge
- feat(harmony): 实现 WidgetBridge 桌面卡片 Form + App 事件/convertFileSrc/Filesystem/Device 原生能力桥接 / feat(harmony): Implement WidgetBridge desktop card Form + App event/convertFileSrc/Filesystem/Device native capability bridging
- feat(harmony): 实现 WidgetBridge 桌面卡片(Form) / feat(harmony): Implement WidgetBridge desktop card (Form)
- feat(harmony): 增加 WidgetBridge handler 数据缓存层 / feat(harmony): Add WidgetBridge handler data caching layer
- feat(harmony): 实现课程提醒闹钟 / feat(harmony): Implement course reminder alarm clock
- feat(harmony): 实现 YsuNotify 后台轮询与通知发布 / feat(harmony): Implement YsuNotify background polling and notification publishing
- feat(ota): GitHub-Release 直连优先，失败自动 fallback 到 Worker 代理 / feat(ota): GitHub-Release gives priority to direct connection, and will automatically fallback to the Worker agent if it fails.
- feat(ci): 将 PWA 捆绑包发布到 OTA 的 Web 资产版本 / feat(ci): publish PWA bundle to web-assets release for OTA
- feat: 自托管代理支持 (SCF/FC) + 设置指南 + 登录横幅 / feat: self-hosted proxy support (SCF/FC) + setup guide + login banner
- feat(worker): 结构化请求日志记录（方法/路径/状态/ms/ip/国家/地区） / feat(worker): structured request logging (method/path/status/ms/ip/country)
- feat(ios): 添加iOS平台+CI未签名IPA构建（手动调度） / feat(ios): add iOS platform + CI unsigned IPA build (manual dispatch)
- feat: 登录页面后端模式选择器+PWA下载链接 / feat: login page backend mode selector + PWA download links
- feat(ota): 在应用更新之前验证发布提交 SSH 签名 / feat(ota): verify release commit SSH signature before applying updates
- feat: 集成 Worker 代理、反馈、公告和凭证符号链接 / feat: integrate Worker proxy, feedback, announcement and credential symlinks
- feat(worker): 初始化 Cloudflare Worker 后端 / feat(worker): initialize Cloudflare Worker backend
- feat(worker-config): 添加客户端 Worker 配置和代理脚手架 / feat(worker-config): add client-side Worker config and proxy scaffolding
- feat: 将浏览器配置文件伪装集成到 TS 网络层和 CAS 中 / feat: integrate browser profile camouflage into TS network layer and CAS
- feat(android): OkHttp浏览器配置文件伪装 / feat(android): OkHttp browser profile camouflage
- feat: 为 OkHttp 伪装添加共享浏览器配置文件模块 / feat: add shared browser profile module for OkHttp camouflage

### 🐛 修复 / Bug Fixes
- fix(scripts): 变更日志多模式 grep 和简化的 build_section / fix(scripts): changelog multi-pattern grep and simplified build_section
- fix: 强大的轮询模式+双向代理建议 / fix: robust polling patterns + bidirectional proxy suggestion
  1. WeChat MFA polling: tight loop with bare 'continue' on error replaced with exponential backoff (2s/4s/8s/16s/32s) and max 5 consecutive errors before giving up. Normal poll interval added (2s) between successful requests.
  2. Proxy suggestion dialog: now bidirectional. When direct connect fails, suggests switching to cloud proxy. When cloud proxy fails, suggests switching to direct. Auto-detects network errors (Failed to fetch, timeout, ECONNREFUSED, etc).
  3. Foreground notification polling: skip when page is hidden (visibilityState === 'hidden') to save battery and bandwidth.
- fix(tauri): 可靠的平台检测+网络错误时自动建议代理 / fix(tauri): reliable platform detection + auto-suggest proxy on network error
  1. Tauri platform detection timing: isTauri() checked window.__TAURI_INTERNALS__ at first render, but Tauri 2 injects it after React hydrate. Added useNativePlatform() hook that re-checks on mount + 100ms delay. Also enabled withGlobalTauri in tauri.conf.json for window.__TAURI__ as backup signal. Login page now uses the hook instead of static calls.
  2. Auto-suggest proxy on network failure: when a native client (Capacitor) gets a network error during login (Failed to fetch, timeout, ECONNREFUSED), a dialog suggests switching to cloud proxy mode. User can accept (one-click switch) or dismiss.
- fix(login): 通过直接连接隐藏本机应用程序上的代理警告 / fix(login): hide proxy warning on native apps with direct connect
- fix: 默认本机客户端直接连接而不是 Worker 代理 / fix: default native clients to direct connect instead of Worker proxy
  1. cookie.ts refreshWorkerProxyState: default to direct connect on Capacitor+Tauri, Worker only on PWA/Web
  2. settings.ts useWorkerProxy default: false (was true)
  3. settings.ts merge migration: old users with useWorkerProxy=true migrate to false
- fix(tauri): 修复 9 个运行时错误（资源 ID 无效 + 禁止标头） / fix(tauri): fix 9 runtime errors (resource id invalid + forbidden headers)
  1. Forbidden headers warnings (accept-encoding, connection, origin, referer):
  2. unhandledRejection 'resource id is invalid' (14 occurrences):
- fix(tauri): 修复窗口不显示+添加开发/构建命令 / fix(tauri): fix window not showing + add dev/build commands
- fix(harmony): 实现剩余的无操作桥接方法 / fix(harmony): implement remaining no-op bridge methods
  1. AppHandler.exitApp: was empty body. Now calls abilityContext.terminateSelf() to properly close the app, matching UpdaterHandler.reload() pattern.
  2. HttpHandler.downloadFile: was returning 'not supported' error. Now uses @ohos.request downloadFile API, matching UpdaterHandler's proven download pattern. Returns { path } on success.
  3. UpdaterHandler.setChannel: was returning success without persisting. Now stores channel to preferences via KEY_CHANNEL, matching @capgo/capacitor-updater behavior.
- fix: 完整的半成品平台存根 / fix: complete half-finished platform stubs
  1. notify-tauri.ts: stale comment said 'background polling not supported' — now references notify-foreground.ts which implements it.
  2. HarmonyOS YsuNotifyHandler: checkBatteryOptimization/requestIgnoreBatteryOptimization were returning makeNotImplemented error. HarmonyOS has no equivalent to Android battery optimization (background task model is different). Now return default values (ignored:true / ok) so the settings UI doesn't show errors. Removed the unused makeNotImplemented method.
- fix(ci): 添加 shell: bash 到 HarmonyOS 查找 HAP 步骤 / fix(ci): add shell: bash to HarmonyOS Find HAP step
- fix(harmony): 在构建中使用 cp 而不是 xcopy 进行 dist 复制。 嘘 / fix(harmony): use cp instead of xcopy for dist copy in build. sh
- fix(harmony): 将 MSYS2 路径转换为 ​​Windows 路径，以便在构建中进行 xcopy。 嘘 / fix(harmony): convert MSYS2 paths to Windows paths for xcopy in build. sh
- fix(harmony): 对自托管 CI 运行程序使用绝对工具链路径 / fix(harmony): use absolute toolchain path for self-hosted CI runner
- fix(harmony): env 脚本覆盖 PROJECT_ROOT 破坏 CI 路径 / fix(harmony): env script overwrites PROJECT_ROOT breaking CI paths
- fix(harmony): 未设置签名机密时允许未签名的 HAP 构建 / fix(harmony): allow unsigned HAP build when signing secrets not set
- fix(harmony): 修复 env 脚本语法错误和 PATH 污染 / fix(harmony): fix env script syntax errors and PATH pollution
- fix(cas): 清除 TGC 反弹时的所有 CAS cookie，而不仅仅是 CASTGC / fix(cas): clear all CAS cookies on TGC bounce, not just CASTGC
- fix(login): 在登录 UI 中将 Tauri 识别为本机应用程序 / fix(login): recognize Tauri as native app in login UI
- fix(cookie): 过期 Max-Age=0 cookie 而不是发送空值 / fix(cookie): expire Max-Age=0 cookies instead of sending empty values
- fix(cas): 手动 hop reAuth follow 以避免 Worker 代理 cookie 混合 / fix(cas): manual hop reAuth follow to avoid Worker proxy cookie mixing
- fix(cas): 遵循 reAuth 重定向链正确建立会话 / fix(cas): follow reAuth redirect chain to establish session properly
- fix(cas): 在 MFA POST 之前刷新 reAuth 会话以防止 206302 / fix(cas): refresh reAuth session before MFA POSTs to prevent 206302
- fix(cas): 在 cookie 清除之前检测 getLoginPage 中的 IP 冻结页面 / fix(cas): detect IP freeze page in getLoginPage before cookie clear
- fix(cas): 当 getLoginPage 获取非登录 HTML 时清除过时的 reAuth cookie / fix(cas): clear stale reAuth cookies when getLoginPage gets non-login HTML
- fix(cas): 遵循 reAuthCheck 重定向链正确初始化 reAuth 会话 / fix(cas): follow reAuthCheck redirect chain to properly initialize reAuth session
- fix(cas): 在 MFA 请求 MFACode POST 中注入桌面配置文件标头 / fix(cas): inject desktop profile headers in MFA requestMFACode POSTs
- fix(cas): 解析 MFA 发送代码响应中的 CAS errCode/消息字段 / fix(cas): parse CAS errCode/message fields in MFA send-code response
- fix(android): 从 CI 中的环境变量读取签名密码 / fix(android): read signing passwords from env vars in CI
- fix(cookie): 以斜杠结尾的路径匹配被破坏 / fix(cookie): pathMatches broken for paths ending with slash
- fix(cas): 允许在授权 SSO 链中重定向至 CAS 登录 / fix(cas): allow redirect TO CAS login in authorize SSO chain
- fix(cas): 通过手动跃点授权跨域 cookie 路由 / fix(cas): authorize with manual hops for cross-domain cookie routing
- fix(cas): 授权从服务 URL 开始建立 JWXT 会话 / fix(cas): authorize starts from service URL to establish JWXT session
- fix(cas): 在授权中中断而不是抛出 CAS 登录弹跳 / fix(cas): break instead of throw on CAS login bounce in authorize
- fix(cas): 在授权重定向链后添加门户预热 GET / fix(cas): add portal warm-up GET after authorize redirect chain
- fix(cas): 授权使用带有环路防护的手动重定向跃点 / fix(cas): authorize uses manual redirect hops with loop guard
- fix(mfa): 强大的会话验证+始终显示微信选项 / fix(mfa): robust session validation + always show WeChat option
  1. MFA submit: check CASTGC cookie in jar after redirect follow, not just URL match. Cookie is a more reliable signal of session establishment.
  2. WeChat MFA: always show option on all devices. Non-tablet shows '不推荐' suffix and defaults to SMS. Tablet defaults to WeChat.
- fix: 通过 Worker 代理路由所有外部获取 / fix: route all external fetches through Worker proxy
  1. WeChat QR image (open.weixin.qq.com/connect/qrcode/) — <Image> direct load fails CORS. Added fetchWechatQrImage() that fetches blob via _fetch and returns object URL.
  2. feedback.ts checkFeedbackReplies — direct fetch to api.github.com for issue comments. Routed through Worker /proxy with base64 body decode.
  3. commit-signature.ts — only called from updater on native platforms, no PWA impact. No fix needed.
- fix(cas): 通过Worker代理路由微信MFA+修复授权重定向循环 / fix(cas): route WeChat MFA through Worker proxy + fix authorize redirect loop
  1. initiateWechatMFA: WeChat OAuth page fetch (open.weixin.qq.com) now goes through Worker proxy instead of direct fetch (CORS on PWA).
  2. pollWechatQR: WeChat poll endpoint (lp.open.weixin.qq.com) now goes through Worker proxy.
  3. authorize: switched from redirect:'follow' (which loops 10x when CAS bounces back to login) to redirect:'manual' with early login-bounce detection.
- fix(login): 在卡片标题中显示应用程序名称而不是学生 ID 占位符 / fix(login): show app name instead of student ID placeholder in card title
- fix(cas): 始终在 POST 之前获取新的登录页面，以避免过时的执行令牌 / fix(cas): always fetch fresh login page before POST to avoid stale execution token
- fix(cas): 从登录 POST URL 中删除缓存破坏程序 / fix(cas): remove cache-buster from login POST URL
- fix(worker): 使公告响应模式与客户保持一致 / fix(worker): align announcement response schema with client
- fix(worker): 允许 *。 终端长度。 页。 CORS 中的开发预览起源 / fix(worker): allow *. terminal-length. pages. dev preview origins in CORS
- fix(pwa): 删除安全。 md 回退，修复 CORS 和崩溃回归 / fix(pwa): remove SECURITY. md fallback, fix CORS and crash regressions
  1. worker-config.ts still had SECURITY.md raw fetch fallback (pre-steganography). Removed fetchConfigFromGitHub and extractEncryptedPayload. Worker config now env-only from logo steganography at build time.
  2. announcement.ts direct fetch to github.com on PWA hits CORS. Added isCapacitor guard: PWA without Worker config returns null instead of attempting doomed direct fetch.
  3. sdk-provider.tsx analytics prompt onClose called checkAnnouncementsThenUpdates() without catch. Unhandled rejection crashed the app. Wrapped in .catch().
- fix(auth): 推迟 setHasHydrated 以匹配设置水合 / fix(auth): defer setHasHydrated to match settings hydration
- fix(settings): 推迟 setHasHydrated 以避免 React 19 水合 TDZ / fix(settings): defer setHasHydrated to avoid React 19 hydration TDZ
- fix(ota): 将缓存清除添加到版本中。 json 和 dist. 压缩网址 / fix(ota): add cache-busting to version. json and dist. zip URLs
- fix(native): 安全存储动态导入+电容桥加固 / fix(native): secure storage dynamic import + capacitor bridge hardening
- fix(native): 加强 isCapacitor 检测以防止假网桥 / fix(native): harden isCapacitor detection against fake web bridges
- fix(pwa): 解决 TDZ、OTA 稳健性和启动超时问题 / fix(pwa): resolve TDZ, OTA robustness, and startup timeout issues
- fix: 工作日志记录、重定向语义和 JSON 解析安全 / fix: worker logging, redirect semantics and JSON parse safety
- fix: 删除 Tauri 功能 JSON 中的尾随逗号 / fix: remove trailing comma in Tauri capabilities JSON
- fix: 通过 Worker 代理传递重定向模式以获得正确的 CAS 响应 / fix: pass redirect mode through Worker proxy for correct CAS response
- fix: 打破 TDZ 循环 dep，在重新加载时恢复自定义代理秘密 / fix: break TDZ circular dep, restore custom proxy secret on reload
- fix: 扩展 CAS 错误提取、在推送上部署工作人员、添加调试片段 / fix: expand CAS error extraction, deploy worker on push, add debug snippet
- fix: 通过worker cookie jar（PWA）获取验证码图像 / fix: fetch captcha image through worker cookie jar (PWA)
- fix: 禁用 terser 压缩以消除 TDZ 错误 / fix: disable terser compress to eliminate TDZ errors
- fix: 延迟加载 i18n 字典以避免 Turbopack 块中的 TDZ / fix: lazy-load i18n dictionaries to avoid TDZ in Turbopack chunks
- fix(ci): web-assets 标签必须指向发布存储库提交 / fix(ci): web-assets tag must point to release repo commit
- fix: 缓存页面标头 + 减少简洁传递以避免 TDZ / fix: cache headers for Pages + reduce terser passes to avoid TDZ
- fix(ci): 使用布尔力进行标签更新并处理丢失的标签 / fix(ci): use boolean force for tag update and handle missing tag
- fix: 始终显示代理输入（禁用状态），添加应用程序。 返回 i18n / fix: always show proxy inputs (disabled state), add app. back i18n
- fix: 设置存储迁移+使旧工人无效。 开发缓存 / fix: settings store migration + invalidate old workers. dev cache
  1. useWorkerProxy was undefined in persisted settings (old version
  2. Worker config cached the old .workers.dev endpoint (TTL 7 days).
- fix: 禁用 terser mangle，从 tsconfig 中排除本机目录 / fix: disable terser mangle, exclude native dirs from tsconfig
- fix(ci): 将GITHUB_TOKEN传递给decrypt-worker-config以避免429 / fix(ci): pass GITHUB_TOKEN to decrypt-worker-config to avoid 429
- fix: 同步 pnpm 锁。 具有简洁依赖项更改的 yaml / fix: sync pnpm-lock. yaml with terser dependency change
- fix(ci): 将 NEXT_PUBLIC_YANDA_PROXY_SECRET 传递给 PWA 和 iOS 构建 / fix(ci): pass NEXT_PUBLIC_YANDA_PROXY_SECRET to PWA and iOS builds
- fix: 将 javascript-obfuscator 替换为 terser / fix: replace javascript-obfuscator with terser
- fix(ci): 将 build-pwa 恢复为独立作业，拆分部署工作人员 / fix(ci): restore build-pwa as independent job, split deploy-worker
- fix: 混淆器标识符冲突 + 公告 CORS / fix: obfuscator identifier collisions + announcement CORS
- fix(ci): 添加页面部署，删除虚假的 dist/** 版本 / fix(ci): add Pages deploy, remove bogus dist/** release
- fix: 默认为 Capacitor 上的 Worker 代理 + 嵌入代理密钥 / fix: default to Worker proxy on Capacitor + embed proxy secret
- fix: isCapacitor() 在 ESM 构建 + Worker 端点更新中损坏 / fix: isCapacitor() broken in ESM build + Worker endpoint update
- fix(ci): 将节点增加到 22（pnpm 11 需要 >=22） / fix(ci): bump node to 22 (pnpm 11 requires >=22)
- fix(ci): 固定 account_id 以跳过 /memberships 查找 (9106) / fix(ci): pin account_id to skip /memberships lookup (9106)
- fix: Capacitor默认是直连，不是Worker代理 / fix: Capacitor defaults to direct connection, not Worker proxy
- fix: CapacitorHttp 在 Capacitor 下无法访问。 v6+ 中的插件 / fix: CapacitorHttp not accessible under Capacitor. Plugins in v6+
- fix(cookie): 将工作代理标头值强制转换为字符串 / fix(cookie): coerce worker proxy header values to string
- fix(worker): 解决学术代理中的工作人员类型错误 / fix(worker): resolve Worker type errors in academic proxy

### 🔧 其他 / Other Changes
- chore(tauri): 将版本更改为 0。 11. 0 / chore(tauri): bump version to 0. 11. 0
- chore(cas): 删除临时调试日志记录 / chore(cas): remove temporary debug logging
- chore(worker): 在牧马人配置中启用可观察性日志 / chore(worker): enable observability logs in wrangler config
- chore: 使用新徽标端点触发 PWA 重建 / chore: trigger PWA rebuild with new logo endpoint
- chore: 修复部署工作流程中的 pnpm 版本 / chore: fix pnpm version in deploy workflow
- chore: 更新构建工具和部署工作流程 / chore: update build tooling and deployment workflow
- chore: 将反馈和OTA迁移到YandaTerminal/YandaTerminal / chore: migrate feedback and OTA to YandaTerminal/YandaTerminal
- chore: 将包重命名为 com. youwenqwq. ysuclient 到 org. 方式。 终端。 重生 / chore: rename package from com. youwenqwq. ysuclient to org. way. terminal. reborn
- docs: CAS/cookie/worker/direct-connect 修复的全面根本原因分析 / docs: comprehensive root cause analysis of CAS/cookie/worker/direct-connect fixes
- docs: 记录所有会议结果 — 13 个回归 + 架构课程 / docs: record all session findings — 13 regressions + architecture lessons
- docs: 在此记录 PWA 公共领域。 dpdns。 组织 / docs: record PWA public domain here. dpdns. org
- docs(jwmobile): 添加探索文档和提交的 JS 示例 / docs(jwmobile): add exploration doc and committed JS samples
- docs(jwxt): 使用经过验证的字段和端点更新时间表、培训计划和评估文档 / docs(jwxt): update schedule, training-plan and evaluation docs with verified fields and endpoints
- docs: 记录 OTA 的 CDN 缓存破坏缓解措施 / docs: record CDN cache-busting mitigation for OTA
- docs: 创纪录的生产。 split() OTA 调查和修复 / docs: record production . split() OTA investigation and fixes
- docs: YSU CAS + JWXT 全接口逆向基准文档 + iOS/鸿蒙修复 / docs: YSU CAS + JWXT full interface reverse benchmark document + iOS/Hongmeng repair
- docs: 更新研究文档并确认根本原因并修复 / docs: update research doc with confirmed root cause and fix
- docs(obfuscation): 添加混淆计划和惰性工作者密钥检查 / docs(obfuscation): add obfuscation plan and lazy worker key check
- refactor(ci): 将变更日志生成提取到 script/generate-changelog。 py / refactor(ci): extract changelog generation to scripts/generate-changelog. py
- refactor: 支持新旧加密配置格式 / refactor: support both old and new encrypted config formats
- refactor: 简化加密配置格式 / refactor: simplify encrypted config format
- ci: 添加 Google 翻译以生成双语变更日志 / ci: add Google Translate for bilingual changelog generation
- ci: 双语变更日志，包含下载表 + 发布正文更新 / ci: bilingual changelog with download table + release body update
- ci: 自动生成变更日志。 md 来自发布时的常规提交 / ci: auto-generate CHANGELOG. md from conventional commits on release
- ci: 覆盖 web-assets 标签上现有的发布资产 / ci: overwrite existing release assets on web-assets tag
- ci(harmony): GitHub Actions 增加 HarmonyOS HAP 发布任务 / ci(harmony): GitHub Actions adds HarmonyOS HAP release task
- ci: PWA 自动推送；仅 Worker/iOS 手动调度 / ci: PWA auto on push; Worker/iOS manual dispatch only

---

**Full diff**: https://github.com/YandaTerminal/yanda-terminal/compare/96bf430...v0.11.0

### 下载 / Download

| Platform | File |
|----------|------|
| Android | `app-release.apk` |
| iOS | `yanda-terminal-ios.ipa` |
| HarmonyOS | `entry-default-unsigned.hap` |
| Windows | `YandaTerminal_0.11.0_x64-setup.exe` |
| Linux | `YandaTerminal_0.11.0_amd64.AppImage` |
| macOS | `YandaTerminal_0.11.0_aarch64.dmg` |

> PWA: https://yanda.dpdns.org
