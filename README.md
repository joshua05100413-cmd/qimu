# 启幕

安卓影视客户端，私人分发，仅供朋友使用。

## 安装

到 [Releases](../../releases/latest) 下载最新的 `.apk` 安装。

首次安装需要在系统设置里允许「安装未知应用」。

## 更新

App 启动时会自动检查新版本，有更新会弹窗提示，可以直接在 App 内下载安装。

## 发版流程（维护者）

1. 改 `android/app/build.gradle.kts` 里的 `versionCode`（只增不减）
2. 构建 APK
3. 创建 Release，**tag 必须写成 `v{versionCode}`**（例如 `v2`）
4. 把 APK 上传为该 Release 的 asset（扩展名必须是 `.apk`）

> ⚠️ 每次发版必须用**同一个 keystore** 签名，否则用户无法覆盖安装，只能卸载重装（本地观看记录会丢）。