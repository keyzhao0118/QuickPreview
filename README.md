# QuickPreview

**Quick preview, more than preview.**  
为 Windows 文件资源管理器预览窗格注入更多可能性的扩展项目。

---

## 🔍 项目简介

**QuickPreview** 是一个基于 Qt 开发的 Windows 预览窗格扩展插件。它的目标不仅是支持多种文件格式的快速预览，还希望为预览窗格带来“更有趣、更智能、更交互”的使用体验。

预览窗格，不止于“预览”。

我们不满足于传统意义上的只读展示：  
你甚至可以在 `.game` 文件中直接玩一盘 **俄罗斯方块**、**贪吃蛇**！

---

## ✨ 核心特性

- ✅ 支持常见文件格式的快速预览（文本、图像、压缩包等）
- 🧩 插件式架构，支持灵活扩展新的预览格式
- 🕹️ 创意预览：在 `.game` 文件中直接体验小游戏
- ⚙️ 基于 Qt 构建，可跨平台复用核心逻辑
- 💡 与 Windows Explorer 预览窗格深度集成，体验原生流畅

---

## 🗂️ 示例：可以预览什么？

| 文件类型 | 预览内容                        |
|----------|-------------------------------|
| `.txt`   | 高亮文本预览                   |
| `.zip`   | 结构化目录树、文件列表         |
| `.game`  | 俄罗斯方块、贪吃蛇、扫雷……     |
| `.json` | 折叠树形结构 + 高亮             |
| `.md`    | 渲染 Markdown 预览              |

（更多格式正在支持中，欢迎贡献 🎉）

---

## 📦 架构概览

项目采用模块化设计：

- `PreviewHost`: 宿主程序，负责加载 COM 组件、嵌入 Qt 窗口
- `QtUiCore`: 通用 UI 渲染模块，跨平台可复用
- `PreviewEngines`: 不同类型文件的预览器插件接口及实现
- `GameView`: 内置小游戏渲染模块

---

## 🚀 快速上手

> 暂未发布二进制安装包，开发者可以从源码构建运行。

```bash
git clone https://github.com/yourname/QuickPreview.git
cd QuickPreview
# 使用 CMake 构建
mkdir build && cd build
cmake .. -G "NMake Makefiles" -DCMAKE_PREFIX_PATH=path_to_qt
nmake
