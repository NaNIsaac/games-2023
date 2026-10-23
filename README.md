# games-2023

Finished: hobby projects from 2023, kept as they were. No further changes are planned.

Small games and sketches written in C++ as hobby projects in 2023, using raylib and openFrameworks
and built with Visual Studio on Windows.

| Folder | What it is | Build notes |
|---|---|---|
| [FlatPhysics](FlatPhysics) | 2D rigid-body physics engine with a slingshot game prototype (raylib) | [FlatPhysics/README.md](FlatPhysics/README.md) |
| [ShootingGame](ShootingGame) | Slingshot shooting game on the FlatPhysics engine (raylib) | [ShootingGame/README.md](ShootingGame/README.md) |
| [PlaneFight](PlaneFight) | Vertical-scrolling shooter (raylib) | [PlaneFight/README.md](PlaneFight/README.md) |
| [ScreenSaver](ScreenSaver) | Particle and animation scenes (openFrameworks) | [ScreenSaver/README.md](ScreenSaver/README.md) |

ShootingGame grew out of FlatPhysics: it is built on a copy of the same engine and still uses the
`FlatPhysics` project name.

## Relation to the standalone repositories

Each folder was imported with `git subtree` from a repository of its own, which keeps the original commit
history (the `Add '<folder>/' from commit` merges in the log):

| Folder | Standalone repository | Imported from commit |
|---|---|---|
| FlatPhysics | [NaNIsaac/FlatPhysics](https://github.com/NaNIsaac/FlatPhysics) | `80388e1` |
| ShootingGame | [NaNIsaac/ShootingGame](https://github.com/NaNIsaac/ShootingGame) | `d732776` |
| PlaneFight | [NaNIsaac/PlaneFight](https://github.com/NaNIsaac/PlaneFight) (private) | `cd604ce` |
| ScreenSaver | [NaNIsaac/ScreenSaver](https://github.com/NaNIsaac/ScreenSaver) (private) | `be99f8d` |

On 2026-10-23 the working files of each folder were identical to the standalone repository's, apart from
line endings. The standalone repositories also keep their other branches (for example `Kim`, `Lee` and `Yong`
in FlatPhysics), which are not part of this repository.

## Building

Verified on 2026-10-23 with MSBuild from the Visual Studio 2022 Build Tools (MSVC 14.44), Debug / x86,
without source changes: FlatPhysics, ShootingGame and PlaneFight build (PlaneFight needs
`-p:PlatformToolset=v143` on a machine without toolset v142). ScreenSaver was not built: it needs an
openFrameworks tree around it. The exact commands are in each folder's README.
