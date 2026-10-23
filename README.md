[English](README.md) | [简体中文](README.zh-CN.md)

# Workspace

| Repository              | Purpose                                                   |
| ----------------------- | --------------------------------------------------------- |
| [Shared][shared-readme] | Game logic, Everest support, formats and native rendering |
| [Unity][unity-readme]   | Unity host and editor tools                               |
| [Godot][godot-readme]   | Godot .NET host                                           |
| [Tools][tools-readme]   | Resource preparation, builds and module installation      |
| [Mods/TAS][tas-readme]  | Optional TAS module and Studio communication              |
| `Mods/<Helper>/`        | Helper modules and local rebuild recipes                  |

Randomizer and Generation share a repository. Submodules select the component revisions.

Supply the original game, supported Mod archives and the chosen host's dependencies.
The preparation entry builds the source ports, reconstructs the nine local
rebuild Mods from their original ZIPs and installs the runtime packages.

## Checkout

```sh
git clone https://github.com/CelesteResearch/Workspace.git
cd Workspace
git submodule update --init --recursive
```

The complete checkout includes the Helper repositories and the independent
`Mods/TAS/` module.

## Build and run

Desktop targets are Windows x64, Linux x64 and macOS x64. Apple Silicon uses x64 hosts and dependencies through Rosetta. Preparation requires PowerShell 7, .NET SDK 10, CMake 3.24+ and a platform C/C++ compiler. Game resources, FMOD and licensed editor dependencies are supplied separately.

Follow [Tools][tools-readme] to prepare the selected host. For Strawberry Jam
and its Helpers, provide the supported original ZIPs in the original game's
`Mods/` directory and add `-IncludeHelpers` to the preparation command.

Start Unity with Unity/Assets/Scenes/Game.unity, or Godot .NET with Godot/project.godot.

## Licenses

See [NOTICE.md](NOTICE.md) for Workspace terms and each component's LICENSE and NOTICE for its own terms.

[shared-readme]: https://github.com/CelesteResearch/Shared/blob/main/README.md
[unity-readme]: https://github.com/CelesteResearch/Unity/blob/main/README.md
[godot-readme]: https://github.com/CelesteResearch/Godot/blob/main/README.md
[tools-readme]: https://github.com/CelesteResearch/Tools/blob/main/README.md
[tas-readme]: https://github.com/CelesteResearch/TAS/blob/main/README.md
