# void Image Viewer

一款轻量级 Windows 图片查看器，支持 GIF/WEBP 动画。  
可以尽可能快地打开和显示 BMP、GIF、ICO、PNG、JPG、TIF 和 WEBP 图片。  
可以尽可能准确地播放 GIF/WEBP 动画。  

[下载](#下载)<br/>
[功能](#功能)<br/>
[编译](#编译)<br/>
[安装程序](#安装程序)<br/>
[参见](#参见)<br/>
<br/><br/><br/>



功能
----
- **多语言支持**：英语（美国）和简体中文。
  - 程序启动时自动检测系统语言。
  - 界面已完整翻译，包括菜单、对话框、工具栏、状态栏和文件关联。
  - 本地化源文件：`src/localization_en_us.h`、`src/localization_zh_cn.h`、`src/localization.c`。

- 支持 GIF/WEBP 动画播放，可调节动画速率。
- 幻灯片放映，可调节间隔（250 毫秒至 1 分钟，或自定义间隔）。
- 缩放模式：最佳适应、填充窗口、1:1、平移和扫描。
- 旋转、重命名、复制/移动、删除、打印、设置为桌面壁纸。
- 可自定义键盘快捷键（选项 -> 控件）。
- 集成 Everything 搜索，可打开搜索结果。

<br/><br/><br/>



下载
----
**简体中文版（本仓库）：**

- 中文版安装包：https://github.com/sanyectop/voidImageViewer_ChineseVer/releases

**英文原版：**

- https://github.com/voidtools/voidImageViewer/releases
- https://www.voidtools.com/forum/viewtopic.php?t=5623
<br/><br/><br/>



编译
----
要求：Visual Studio 2026（v145 工具集）或更高版本。

```bat
msbuild vs2026\voidImageViewer.sln /p:Configuration=Release /p:Platform=x64 /m
```

输出：`vs2026\x64\Release\voidImageViewer.exe`

编译配置：Debug / Release；平台：Win32 / x64 / ARM / ARM64。
<br/><br/><br/>



安装程序
--------
要求：NSIS 3.x（https://nsis.sourceforge.io/Download），并已加入 PATH。

先编译应用程序（见[编译](#编译)），然后运行：

```powershell
.\nsis\build_installer.ps1 -Arch x64 -VsVersion vs2026 -BuildConfig Release -Lang Chinese
```

参数：
- `-Arch`：`x86` 或 `x64`（默认：`x86`）
- `-VsVersion`：`vs2026`、`vs2019` 等（默认：自动检测）
- `-BuildConfig`：`Release`、`Debug` 等（默认：`Release`）
- `-Lang`：`Chinese` 或 `English`（默认：`Chinese`）

输出：`nsis\voidImageViewer-<版本>.<架构>.<语言>-Setup.exe`

注意：安装向导界面使用英文以避免编码乱码；中文版在界面中以英文标注 "Chinese Version"，文件名保留 `zh-CN` 后缀。
<br/><br/><br/>



void Image Viewer 主窗口：

![Void Image Viewer Image View](https://www.voidtools.com/voidImageViewer.Image.View10.gif)
<br/><br/><br/>



void Image Viewer 常规选项：

![Void Image Viewer Options General](https://www.voidtools.com/voidImageViewer.Options.General10.png)
<br/><br/><br/>



void Image Viewer 视图选项：

![Void Image Viewer Options View](https://www.voidtools.com/voidImageViewer.Options.View10.png)
<br/><br/><br/>



void Image Viewer 控件选项：

![Void Image Viewer Image Controls](https://www.voidtools.com/voidImageViewer.Options.Controls10.png)
<br/><br/><br/>



参见
----
https://www.voidtools.com/forum/viewtopic.php?t=5623
