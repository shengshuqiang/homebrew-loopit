# homebrew-loopit

Loopit Game Playground 的 macOS Apple Silicon Homebrew tap。正式可安装的版本以 `Casks/loopit-game-playground.rb` 和对应构建的安装验证结果为准。

## 发布准备

维护者在 macOS 上将拟分发的 ZIP 传给 `scripts/prepare-cask`。脚本核对应用标识、构建号、架构、签名完整性和 macOS 分发检查，再生成绑定该 ZIP 的 SHA-256 的 Cask。

模板使用 GitHub Release 地址。上传前须确认该版本获准在此公开仓库分发。受限内测文件应保留原有访问范围。

## 异机验证

GitHub Actions 使用独立的 Apple Silicon Mac，通过 HTTPS 拉取 tap。已有正式 Cask 时，它还会下载并安装该版本，回读实际应用的版本、构建和隔离标记，然后检查代码签名、Gatekeeper 和 XProtect。工作流分别显示安装源检查和真实安装检查的状态。
