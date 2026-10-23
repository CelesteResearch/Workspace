[English](README.md) | [简体中文](README.zh-CN.md)

# Workspace

| 仓库                          | 用途                                       |
| ----------------------------- | ------------------------------------------ |
| [Shared][shared-readme-zh-cn] | 游戏逻辑、Everest 支持、格式解析和原生渲染 |
| [Unity][unity-readme-zh-cn]   | Unity 宿主及编辑器工具                     |
| [Godot][godot-readme-zh-cn]   | Godot .NET 宿主                            |
| [Tools][tools-readme-zh-cn]   | 资源准备、构建及模块安装                   |
| [Mods/TAS][tas-readme-zh-cn]  | 可选 TAS 模块及 Studio 通信                |
| `Mods/<Helper>/`              | Helper 模块及本地重建配方                  |

Randomizer 与 Generation 位于同一仓库。子模块指定各组件版本。

提供原始游戏、支持的 Mod 压缩包及所选宿主的依赖后，统一准备入口会构建源码移植项目，
从原始 ZIP 重建 9 个 Mod，并安装运行包。

## 获取源码

```sh
git clone https://github.com/CelesteResearch/Workspace.git
cd Workspace
git submodule update --init --recursive
```

完整检出包含全部 Helper 仓库，以及独立的 Mods/TAS 模块。

## 构建与运行

桌面目标为 Windows x64、Linux x64 和 macOS x64；Apple Silicon 使用 Rosetta 运行 x64 宿主和依赖。准备环境需要 PowerShell 7、.NET SDK 10、CMake 3.24+ 及对应系统的 C/C++ 编译器。游戏素材、FMOD 与需授权的编辑器依赖由使用者另行提供。

按 [Tools][tools-readme-zh-cn] 准备所选宿主。使用草莓酱及其 Helper 时，将支持版本的原始 ZIP
放在原游戏的 `Mods/` 目录，在准备命令中加上 `-IncludeHelpers`。

Unity 入口为 Unity/Assets/Scenes/Game.unity，Godot .NET 入口为 Godot/project.godot。

## 许可证

工作区条款见 [NOTICE.md](NOTICE.md)，各组件条款见对应 LICENSE 和 NOTICE。

[shared-readme-zh-cn]: https://github.com/CelesteResearch/Shared/blob/main/README.zh-CN.md
[unity-readme-zh-cn]: https://github.com/CelesteResearch/Unity/blob/main/README.zh-CN.md
[godot-readme-zh-cn]: https://github.com/CelesteResearch/Godot/blob/main/README.zh-CN.md
[tools-readme-zh-cn]: https://github.com/CelesteResearch/Tools/blob/main/README.zh-CN.md
[tas-readme-zh-cn]: https://github.com/CelesteResearch/TAS/blob/main/README.zh-CN.md
