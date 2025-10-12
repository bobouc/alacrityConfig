# Alacritty Terminal Configuration

一个现代化的终端配置集合，包含 Alacritty、Tmux 和 Zsh 的配置文件，用于提升开发效率和用户体验。

<img src="./Screenshot 2025-10-12 at 15.10.07.png" alt="Screenshot 2025-10-12 at 15.10.07" style="zoom: 33%;" />

## 📁 包含文件

- `alacritty.toml` - Alacritty 终端配置
- `.tmux.conf` - Tmux 终端复用器配置
- `.zshrc.bk` - Z Shell 配置备份
- `CLAUDE.md` - Claude Code 开发指南

## ✨ 主要特性

### Alacritty 配置
- 🖥️ 120x30 窗口尺寸，96% 透明度
- 🔤 MesloLGS NF 字体，15pt 大小
- 🎨 Dracula 风格配色方案
- ⌨️ 自定义快捷键（复制/粘贴/字体大小调整）

### Tmux 配置
- 🎯 Ctrl+A 前缀键（替代默认 Ctrl+B）
- 🖱️ 完整鼠标支持
- 📋 Vi 风格复制模式，支持系统剪贴板
- ⚡ 优化的窗格导航和调整快捷键

### Zsh 配置
- 🚀 Powerlevel10k 主题
- 🐙 Git 集成和自动补全
- 🔧 Conda 环境管理
- 🏠 Homebrew 路径配置

## 🚀 安装使用

1. **Alacritty 配置**：
   ```bash
   cp alacritty.toml ~/.config/alacritty/alacritty.toml
   ```

2. **Tmux 配置**：
   ```bash
   cp .tmux.conf ~/.tmux.conf
   ```

3. **Zsh 配置**：
   ```bash
   cp .zshrc.bk ~/.zshrc
   ```

## 🔧 依赖要求

- Alacritty 终端模拟器
- Tmux 终端复用器
- Zsh + Oh My Zsh
- MesloLGS NF 字体（支持 Powerline 符号）
- xclip (Linux) 或 pbcopy (macOS) 用于剪贴板集成

## 🎨 预览

配置提供了现代化的终端体验，包括：
- 半透明窗口效果
- 优化的配色方案
- 高效的键盘快捷键
- 智能的自动补全
- 直观的窗格管理

## 📝 注意事项

- `.zshrc.bk` 文件包含个人 API 配置，使用时请注意敏感信息
- 配置文件针对个人工作流进行了优化
- 字体选择支持 Powerline 和各种编程语言的图标显示

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进这个配置！