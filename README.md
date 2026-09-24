# WorkBuddy 换号器 · 便携版下载

Windows x64 绿色单文件，双击即用，无需安装。

> 这是**个人镜像分发仓库**，只放已经构建好的便携包，不含源码。
> 源码与官方版本请见 [changexbc/workbuddy-switch](https://github.com/changexbc/workbuddy-switch)。

---

## 一、下载最新版

| 方式 | 链接 |
|---|---|
| 发布页（推荐） | [Releases](../../releases/latest) |
| 直链 | `.../releases/latest/download/workbuddy-switch-0.1.47-win32-x64-portable.exe` |

### 国内加速下载

GitHub 直连在国内不稳定（实测 60 秒都下不完 22MB）。在链接前面拼上 `https://gh-proxy.com/`
即可加速，实测 **9 秒**下完：

```
https://gh-proxy.com/https://github.com/gaoqiaoliangjie666/wb-switch-portable/releases/latest/download/workbuddy-switch-0.1.47-win32-x64-portable.exe
```

备用镜像：`https://ghfast.top/`（同样可用，实测 9 秒）。

---

## 二、全部版本

| 版本 | 文件 |
|---|---|
| v0.1.47（最新） | `workbuddy-switch-0.1.47-win32-x64-portable.exe` |
| v0.1.46 | `workbuddy-switch-0.1.46-win32-x64-portable.exe` |
| v0.1.45 | `workbuddy-switch-0.1.45-win32-x64-portable.exe` |
| v0.1.41 | `workbuddy-switch-0.1.41-win32-x64-portable.exe` |
| v0.1.39 | `workbuddy-switch-0.1.39-win32-x64-portable.exe` |
| v0.1.37 | `workbuddy-switch-0.1.37-win32-x64-portable.exe` |
| v0.1.36 | `workbuddy-switch-0.1.36-win32-x64-portable.exe` |
| v0.1.30 | `workbuddy-switch-0.1.30-win32-x64-portable.exe` |

把版本号替换进这个模板即可下载任意版本：

```
https://gh-proxy.com/https://github.com/gaoqiaoliangjie666/wb-switch-portable/releases/download/v<版本>/workbuddy-switch-<版本>-win32-x64-portable.exe
```

---

## 三、使用说明

- 双击 exe 即可运行，**绿色免安装**。
- 账号数据保存在 `%USERPROFILE%\.wb-switch\accounts.json`，**跨版本共用**，覆盖 exe 不受影响。
- 升级新版本：直接下载新 exe 覆盖旧的即可。

## 四、校验下载完整性

```powershell
Get-FileHash .\workbuddy-switch-0.1.47-win32-x64-portable.exe -Algorithm SHA256
```

最新版 v0.1.47 的 SHA256：

```
7AA83437D8D1B5C0A2703FFAE030663363C1FE0FD62768B27D6B9CD8DD4BB22C
```

---

## 五、关于程序内的"检查更新"

**重要：程序内的自动更新无法使用本仓库，请忽略它。**

官方原版的自动更新（点击"立即更新"）走的是 **Tauri updater 硬编码端点 + minisign 签名校验**：

- 下载端点固定写死在 exe 里，指向 `changexbc/workbuddy-switch`，**不会读取设置里的 owner/repo**；
- 更新包必须是官方私钥签名的 `.sig` 文件，本地构建的便携包无法伪造签名。

因此设置页里的 owner/repo 只影响「检测到新版本」的显示，改成本仓库后并**不会**让程序从这里下载。
本仓库的定位就是**手动下载分发**：来这里下最新便携包，覆盖旧 exe 即可。

> 若想让程序真正支持从本仓库自动更新，需要改源码（新增"下载便携包 + 生成替换脚本"逻辑），
> 官方原版不含该能力。
