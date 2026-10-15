# 红果盒子

非官方的红果短剧第三方客户端，个人自用。

**本仓库只用于发布安装包和应用内检查更新，不包含源代码。**

## 下载

在 [Releases](https://github.com/Fatal0607/hongguobox-releases/releases) 下载最新版本：

| 平台 | 文件 |
|---|---|
| Android 手机 / 平板 | `hongguobox-0.4.0-android.apk` |
| macOS（Apple 芯片） | `hongguobox-0.4.0-macos.dmg` |

## 安装

### Android

仅提供 arm64-v8a（64 位 ARM）手机 / 平板 APK，不支持 32 位 ARM 或 x86 设备。下载后打开安装；首次安装需在系统设置中允许「安装未知应用」。

### macOS

适用于 macOS 12+、Apple 芯片。下载 `hongguobox-0.4.0-macos.dmg` 并打开，将「红果盒子.app」拖入「Applications / 应用程序」。替换旧版本前请先退出应用。

应用使用 ad-hoc 签名，尚无 Developer ID、未经 Apple 公证。首次打开若被系统拦截，可选择以下一种方法：

1. 尝试打开后，到「系统设置 → 隐私与安全性」点击「仍要打开」（macOS 12 对应「系统偏好设置 → 安全性与隐私 → 通用」）。
2. 确认安装包来源为本发布仓库后，在终端执行：

   ```sh
   xattr -dr com.apple.quarantine /Applications/红果盒子.app
   ```

   这会去除下载隔离标记，仅需一次；重新下载或更新后若再次出现拦截，可对新安装的应用再执行一次。应用内沙盒下载也可能触发隔离；若系统显示「已损坏」且没有「仍要打开」，请使用第二种方法。

## 更新

应用启动时及「我的 → 关于 → 检查更新」会读取本仓库最新 Release 中的 `latest.json`，有新版本时提示下载。macOS 会将 DMG 保存到「下载」并打开，随后需手动拖入「应用程序」替换；Android 下载校验后打开系统安装器。

**0.2.0 升级说明**：旧版清单解析只接受 macOS zip，无法读取新版 DMG 清单（包括 Android 端）。Mac 用户请从 Releases 手动下载并安装 0.4.0 一次；Android 0.2.0 用户也需手动安装新版，之后可使用应用内更新。

## 声明

- 本应用为非官方第三方客户端，与字节跳动、红果短剧官方无任何关联，也未获得授权。
- 仅供个人学习与交流，禁止用于任何商业用途。
- 应用不存储、不分发任何影视内容；内容版权归原权利方所有。
- 部分组件来自 [it00021hot/hongguo-desktop](https://github.com/it00021hot/hongguo-desktop)，遵循 [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/)；完整许可与第三方声明随安装包附带（应用内「我的 → 关于 → 开源许可与声明」）。
