# milkdrop2-musikcube
a port of the amazing milkdrop2 visualizer to musikcube

most of the code was pulled straight from the [official Milkdrop2 source code](https://sourceforge.net/projects/milkdrop2/), but some was adapted from the [XBMC plugin](https://github.com/oO-MrC-Oo/Milkdrop2-XBMC).

Clone this repository next to the musikcube checkout. Install Visual Studio 2026 with Desktop development with C++ and a Windows SDK. From Developer PowerShell, build the plugin with:

```powershell
MSBuild.exe .\milkdrop2-musikcube.sln /restore /p:RestorePackagesConfig=true /p:Configuration=Release /p:Platform=x64 /m
```

MSBuild restores the pinned Microsoft D3DX NuGet package and stages the plugin, resources, and runtime DLLs under the sibling musikcube checkout's `bin64\Release` directory. Use `/p:Configuration=Debug` to stage a Debug build.
