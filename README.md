# Equalizer-gui For MPV Player

- Interactive 10-band audio equalizer GUI script for mpv media player with auto-save and persistence.
- 一款为 mpv 播放器打造的 10 段图形化音频均衡器（Equalizer GUI） Lua 脚本。具有屏幕分辨率大小自适应、现代设计风格、图形可视化调节、配置持久化自动保存与加载等特性。

![image](https://github.com/akFace/equalizer-gui/raw/main/images/Snipaste_2026-08-13_18-08-43.jpg)

## 📦 安装方法

1. 将 `equalizer-gui.lua` 复制到你的 mpv 配置目录下的 `scripts` 文件夹中：

- **Windows (Portable 便携版)**: `portable_config/scripts/equalizer-gui.lua`
- **Windows (安装版)**: `%APPDATA%/mpv/scripts/equalizer-gui.lua`
- **Linux / macOS**: `~/.config/mpv/scripts/equalizer-gui.lua`

2. 重启 mpv 播放器即可生效。

> 💡 **提示**：脚本会在 `script-opts/` 或 mpv 配置根目录下自动创建 `equalizer-gui.json` 用于持久化保存你的均衡器配置。

---

## ⌨️ 快捷键说明

| 快捷键 | 功能描述                                  |
| ------ | ----------------------------------------- |
| E      | 打开 / 关闭均衡器面板                     |
| R      | （面板打开状态下）重置所有频段增益为 0 dB |
| Enter  | （面板打开状态下）保存当前配置并关闭面板  |

---

## 🖱️ 鼠标与键盘操作指南

### 鼠标操作

- **按住左键拖拽推子**：上下调整对应频段的增益（带鼠标锁定，拖拽过程中超出面板范围也不会脱手）。
- **鼠标滚轮**：悬停在某个频段或选中频段时，滚动滚轮可按 0.5dB 步进微调。
- **右键单击推子**：将该单个频段快速重置为 0 dB。

### 键盘操作

- **← / →**：在 10 个频段之间切换当前选中的频段（选中频段高亮显示）。
- **↑ / ↓**：以 0.5dB 为单位增加或减少当前选中频段的增益。

---

## 🛠️ 配置与依赖

- 本脚本纯原生实现，仅依赖 mpv 自带的 `mp.utils` 库与内置 FFmpeg 音频滤镜（`equalizer`），无需额外安装任何第三方依赖。
