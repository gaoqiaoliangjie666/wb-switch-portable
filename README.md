# WorkBuddy 换号器 · 便携版下载

Windows x64 绿色单文件，双击即用，无需安装。

## 下载

最新版请到 [Releases](../../releases/latest) 页面。

| 版本 | 文件 |
|---|---|
| v0.1.47 | `workbuddy-switch-0.1.47-win32-x64-portable.exe` |

## 国内加速下载

GitHub 直连在国内不稳定。把下载链接前面拼上 `https://gh-proxy.com/` 即可加速：

```
https://gh-proxy.com/https://github.com/gaoqiaoliangjie666/wb-switch-portable/releases/latest/download/workbuddy-switch-0.1.47-win32-x64-portable.exe
```

## 使用说明

- 双击 exe 即可运行，账号数据保存在 `%USERPROFILE%\.wb-switch\accounts.json`，跨版本共用。
- 换新版本时直接下载覆盖 exe 即可，账号数据不受影响。

## 校验

下载后可用 PowerShell 校验文件完整性：

```powershell
Get-FileHash .\workbuddy-switch-0.1.47-win32-x64-portable.exe -Algorithm SHA256
```
