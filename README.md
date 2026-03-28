# Config support

Ghostty & Alacritty terminal config, with Tmux / Yazi / Zsh for a dev-friendly workflow.

<img src="./Screenshot 2026-03-28 at 12.54.37.png" alt="Terminal Preview" style="zoom: 33%;" />

## 目录结构

```
.
├── alacritty.toml          # Alacritty 终端配置
├── ghostty/
│   └── config              # Ghostty 终端配置
├── yazi/
│   ├── yazi.toml           # Yazi 主配置
│   ├── keymap.toml         # Yazi 快捷键映射
│   └── package.toml        # Yazi 插件依赖
├── .tmux.conf              # Tmux 配置（当前使用）
├── .tmux.conf.alright      # Tmux 备用配置
├── .zshrc.bk               # Zsh 配置备份
└── README.md
```

## 终端配置

### Ghostty

| 配置项 | 值 |
|---|---|
| 窗口尺寸 | 120 x 30 |
| 内边距 | 10px |
| 字体 | MesloLGS NF, 15pt |
| 配色 | Dracula |
| 光标 | Block, `#97979b` |
| 输入时隐藏鼠标 | 开启 |

配置路径：`~/.config/ghostty/config`

### Alacritty

| 配置项 | 值 |
|---|---|
| 窗口尺寸 | 120 x 30 |
| 透明度 | 96% + Blur |
| 字体 | MesloLGS NF, 15pt |
| 配色 | Dracula |
| 选中自动复制 | 开启 |

快捷键：

| 快捷键 | 功能 |
|---|---|
| `Ctrl+Shift+C` | 复制 |
| `Ctrl+Shift+V` | 粘贴 |
| `Ctrl +/-` | 调整字体大小 |
| `Ctrl+0` | 重置字体大小 |

配置路径：`~/.config/alacritty/alacritty.toml`

## Tmux

| 配置项 | 值 |
|---|---|
| 前缀键 | `Ctrl+A`（替代默认 Ctrl+B） |
| 鼠标支持 | 完全启用 |
| 复制模式 | Vi 风格 |
| 历史记录 | 100,000 行 |
| 真彩色 | 256color + RGB |

快捷键：

| 快捷键 | 功能 |
|---|---|
| `Alt + 方向键` | 切换窗格 |
| `Shift + 方向键` | 调整窗格大小（5px） |
| `F5` | 重载配置 |
| `y` (复制模式) | 复制到系统剪贴板 |
| `q` (复制模式) | 退出复制模式 |
| `Enter` (复制模式) | 复制并退出 |

配置路径：`~/.tmux.conf`

## Yazi

基于终端的高速文件管理器，启用了以下增强：

| 配置项 | 值 |
|---|---|
| 显示隐藏文件 | 开启 |
| 布局比例 | 1:2:8 |
| 排序 | 按修改时间倒序 |
| 行模式 | 显示文件大小 |
| 预览限制 | 1000 x 1000 |

插件：[rich-preview](https://github.com/AnirudhG07/rich-preview) — 支持 CSV / Markdown / RST / Jupyter / JSON 富文本预览

自定义快捷键：

| 快捷键 | 功能 |
|---|---|
| `J` / `K` | 滚动预览 |
| `e` | 打开文件（编辑器） |
| `V` | 以只读模式在 Neovim 中预览 |
| `y` | 复制文件路径 |
| `T` | 在当前目录打开 Shell |
| `p` | 智能进入（目录进入 / 文件打开） |

配置路径：`~/.config/yazi/`

## Zsh

- **主题**：Powerlevel10k（即时提示）
- **插件**：git, zsh-autosuggestions
- **环境**：Homebrew + Conda（Miniforge3）

配置路径：`~/.zshrc`

## 安装

```bash
# 1. 安装字体（必须）
# 下载 MesloLGS NF：https://github.com/romkatv/powerlevel10k#meslo-nerd-font

# 2. 终端配置（按需选择其一）
cp alacritty.toml ~/.config/alacritty/alacritty.toml
# 或
cp ghostty/config ~/.config/ghostty/config

# 3. Tmux
cp .tmux.conf ~/.tmux.conf

# 4. Yazi
cp -r yazi/ ~/.config/yazi/

# 5. Zsh（需先安装 Oh My Zsh 和 Powerlevel10k）
cp .zshrc.bk ~/.zshrc
```

## 依赖

| 依赖 | 用途 |
|---|---|
| MesloLGS NF 字体 | Powerline 图标和编程连字 |
| Oh My Zsh + Powerlevel10k | Shell 主题 |
| Tmux (>= 3.2) | 终端复用 |
| Yazi | 文件管理器 |
| pbcopy (macOS) / xclip (Linux) | 系统剪贴板 |

## 注意事项

- `.zshrc.bk` 中包含 API 配置占位符，使用前请替换为个人密钥
- Ghostty 配置从 Alacritty 配置转换而来，ANSI 颜色由 Ghostty 自动处理
- `.tmux.conf.alright` 为备用 Tmux 配置（鼠标选择后自动退出复制模式）
