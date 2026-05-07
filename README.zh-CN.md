<div align="center">
  <img src="https://raw.githubusercontent.com/awemorris/suika3/refs/heads/main/docs/img/logo-mid.png" alt="Suika3 Logo" width="480" hspace="20">
  <h1 align="center" style="border-bottom: none">
    <a href="https://suika3.vn">Suika3</a>：
    现代、超便携的全栈式<br>
    2D 游戏运行时，内置视觉小说 DSL
  </h1>
  <p>
    我们怀着对移动设备的深切热爱<br>
    让 Suika3 焕发生机——<br>
    那些被主流 3D 引擎所遗忘的平台。<br>
    <br>
    这是一款功能强大、生产就绪的游戏引擎，<br>
    适用于视觉小说及各类 2D 游戏，<br>
    专为在您所选择的任意平台上完美运行而设计。
  </p>
  <a href="https://discord.gg/YZsq9u9Mgr"><img src="https://img.shields.io/badge/suika3.vn-Discord-orange"></a>
  <img src="https://img.shields.io/badge/License-ZLib-orange.svg">
  <img src="https://img.shields.io/github/stars/awemorris/suika3.svg?style=flat&logo=github&colorB=orange&label=stars">
  <img src="https://img.shields.io/github/forks/awemorris/suika3.svg">
</div>

---

<div align="center">
  <p>
    我们自研的 JIT/AOT 脚本基础设施<br>
    让您能够将完全相同的游戏<br>
    同时发布到 Steam 和 App Store，<br>
    彻底消除传统移植的烦恼！
  </p>
  <img src="https://img.shields.io/badge/Desktop-Windows%20%2F%20macOS%20%2F%20Linux%20%2F%20Chromebook%20%2F%20Raspberry%20Pi-blue"><br>
  <img src="https://img.shields.io/badge/Mobile-iOS%20%2F%20Android%20%2F%20HarmonyOS%20NEXT-blue"><br>
  <img src="https://img.shields.io/badge/Console-Switch%20%2F%20PS5%20%2F%20Xbox-blue"><br>
  <img src="https://img.shields.io/badge/Web-Emscripten-blue"><br>
  <img src="https://img.shields.io/badge/Exotic-FreeBSD%20%2F%20NetBSD%20%2F%20OpenBSD%20%2F%20Solaris%20%2F%20Haiku-blue"><br>
  <img src="https://img.shields.io/badge/Store-App%20Store%20%2F%20Play%20Store%20%2F%20Microsoft%20Store%20%2F%20Steam%20%2F%20itch%2eio%20%2F%20App%20Gallery-green"><br>
  <br>
</div>

---

<!-- SCREENSHOT -->
<div align="center">
  <a href="https://noctvm.io/test/">
    点击在浏览器中试玩！<br>
    <img src="https://github.com/awemorris/suika3/blob/main/docs/img/screenshot-20260406.webp" alt="Suika3 示例游戏截图"><br>
  </a>
  Suika3 现在拥有一个由 Suika3 本身编写并自托管的精美启动器！<br>
  <img src="https://github.com/awemorris/suika3/blob/main/docs/img/screenshot-20260429.webp" alt="Suika3 启动器截图"><br>
</div>

---

## 简介

- **目标：** 移动端优先，同时可在任何平台运行
- **高性能：** 原生实现，以 C 语言编写
- **混合脚本：** JIT 虚拟机，并支持 AOT 回退以满足 App Store 合规要求
- **广泛平台：**
    - **桌面端：** Windows、macOS、Linux、Chromebook、Raspberry Pi
    - **移动端：** iOS、Android、HarmonyOS NEXT
    - **Web：** WebAssembly
    - **主机：** Xbox（GDK）、PS5/Switch/Xbox（通过 Unity 集成）\[需要开发套件\]
    - **更多：** FreeBSD、NetBSD、OpenBSD、Solaris、Haiku
- **用户群体：** 专业创作者、独立工作室、企业团队。

---

## 安装

### 下载完整 SDK

[下载 Suika3-SDK-Full.zip](https://github.com/awemorris/suika3/releases/latest/download/Suika3-SDK-Full.zip)

请参阅 [快速入门指南](docs/mkdocs-en/docs/getting-started.md)。

### 包管理器

Linux（Flathub）：
```
flatpak install --user flathub vn.suika3.engine
flatpak run vn.suika3.engine
```

macOS（Homebrew）：
```
brew tap awemorris/suika3
brew install suika3
```

FreeBSD（Ports）：
```
pkg install suika3
```

### 从源代码构建

请参阅 [build.md](docs/mkdocs-en/docs/build.md) 了解各平台的详细说明。

```
# 克隆仓库
git clone https://github.com/awemorris/suika3.git
cd suika3

# 创建构建目录
mkdir build && cd build

# 构建并安装
cmake .. && cmake --build . --parallel && sudo cmake --install .

# 运行示例
cd ../game
suika3
```

---

## Visual Studio Code 语法高亮

由 `@lalalll-lalalll` 开发了一款出色的 VS Code 扩展，支持 Suika3 语法高亮，包括 `NovelML`、`Ray`、`GUI` 和 `Anime` 文件。

查看：[NovelML-Helper](https://github.com/lalalll-lalalll/NovelML-Helper)

安装此扩展时，请访问该仓库并从 [Releases 页面](https://github.com/lalalll-lalalll/NovelML-Highlighter/releases) 下载 .vsix 文件，然后在 VS Code 中安装。

<img src="https://raw.githubusercontent.com/awemorris/suika3/refs/heads/main/docs/img/syntax-highlighter-3.png" alt="安装高亮插件 1" width="320" hspace="20">

---

## VS Code 集成

### Copilot 补全

由于 SDK 包含项目内的完整文档，Copilot 可以参考这些文档，因此您可以使用 Copilot 聊天和/或补全功能来编写 `NovelML` 和 `Ray`。

### 桌面端执行

使用 `Visual Studio Code` 打开解压后的文件夹。

- 点击命令栏，选择 `Run Task --> Suika3: Run`（或直接按 `Ctrl-Shift-B`）
- Suika3 将立即启动！

<img src="https://raw.githubusercontent.com/awemorris/suika3/refs/heads/main/docs/img/vscode-2.webp" alt="VSCode 2" width="640" hspace="20">

- 任何脚本错误都将显示在 `PROBLEMS` 标签页中。
- 您可以点击错误直接跳转到源代码中对应的行。

<img src="https://raw.githubusercontent.com/awemorris/suika3/refs/heads/main/docs/img/vscode-3.webp" alt="VSCode 3" width="640" hspace="20">

### iOS 和 Android 端执行

曾经梦想在短短一分钟内成为 iOS/Android 开发者吗？使用 Suika3，就是这么简单。

- 一键操作：
    - 选择 `Suika3: Build iOS IPA` 或 `Suika3: Build Android APK` 任务，Suika3 将自动构建应用并安装到您通过 USB 连接的智能手机上。
- Android 端：
    - 在手机上开启"开发者模式"和"USB 调试"
    - Suika3 端无需手动配置
    - 无需 Android Studio
    - 无需付费许可证
    - 构建过程中将自动下载 JDK 和 Android SDK
- iOS 端：
    - 需要 Xcode 15+（免费）
    - 在 iPhone 模拟器上测试无需付费许可证
    - 在真实 iPhone/iPad 上测试需要"Apple Developer Program"（99 美元/年）

我们真诚地相信，Suika3 是世界上最为简洁流畅的工具之一，用于创作并向商店发布 iPhone、iPad 和 Android 应用！

即使您还没准备好发布，想象一下当朋友们看到您的游戏流畅运行在 iPhone 上时的表情——您将成为当天的明星。

如果您正在寻找发行商支持您的项目，拥有一个可玩的高质量移动端演示就是您的终极武器。它的说服力远超任何 PPT 提案！

---

## 介绍

Suika3 是一款专为商业移动端应用开发而精心打造的生产级视觉小说与 2D 游戏引擎，由 Suika3 项目开发，领导者为 Awe Morris。

使用 Suika3 制作的游戏由 `NovelML` 和 `Ray` 脚本平台驱动。

- **NovelML**（"演戲標記"）：一种基于标签的、人类可读的、可扩展的 DSL，专为视觉小说设计。它提供简洁的声明式标签，用于无缝的对话和场景控制。开发者可以使用 `Ray` 添加自定义标签。

- **Ray**（"光陰腳本"）：Suika3 的强大脚本语言。在桌面平台上使用高速 JIT 编译器（Sun-Ray JIT VM；代号"諏訪武叡"），并可编译为原生二进制文件（Lunar-Ray AOT 编译器；代号"少彥智叡"），用于生产或移动端环境，同时也有解释器（Ubi-Ray 解释器；代号"天滿梅貴"）。我们的原生技术 Ray，不仅能制作视觉小说，还能制作各类 2D 游戏。（Ray 代号："神威/和光全球之天媛"）

尽管 Suika3 被设计为专业工具，您也完全可以纯粹出于兴趣使用它——毕竟，兴趣是每个伟大社区背后的驱动力。

> [!TIP]
> Suika3 是一款雄心勃勃的引擎，诞生于超过 25 年的独立研发，我们正与早期采用者共同塑造它的未来。

---

## 核心特性

Suika3 采用现代技术构建，提供：

- **高性能**：由 Ray JIT 驱动，在综合基准测试中，执行速度比解释器后端快 2.5-4.5 倍。

- **轻量**：即使在树莓派等发展中地区使用的低配硬件上，也能以 60 fps 流畅运行。

- **真正的可移植性**：采用"移植到任何地方"的策略设计，确保与几乎所有现代平台兼容。

- **可扩展**：NovelML 可以使用 Ray 语言无缝扩展。开发者只需编写名为 `Tag_*()` 的 Ray 函数，即可实现自定义标签。

- **精密架构**：我们的`故事-视图-逻辑架构`简化了游戏开发。`NovelML` 管理游戏的时间线和流程，`GUI` 和 `Anime` 驱动 UI/UX，而 `Ray` 封装复杂的实现细节。

- **可靠**：我们遵循结构化的`质量保证`流程，交付可靠的软件。

- **移动端 UI/UX：** 默认 UX 以移动端为优先，采用汉堡菜单。由于移动端可用性和商店审核风险，消息窗口上的桌面风格小按钮不是主要目标。

- **省电：** 在 60 fps 游玩过程中，Core Ultra 5 228V 上的 CPU 使用率仅为 1%，Apple M5 上为 8%，Apple A15 Bionic 上为 20%，非常适合外出时长时间游玩！防止手机或笔记本过热——真的很"酷"！

- **长期支持：** 凭借高度可移植的代码库，我们的引擎旨在支持 2030 年代、2040 年代及以后的未来平台。LTS 版本包含至少 10 年的 Bug 修复支持。

---

## 目录

- [看板（状态）](#kanban-status)
- [快速入门指南](#getting-started-guide)
- [本地构建](#building-locally)
- [快速浏览](#quick-look)
- [软件包](#packages)
- [示例](#examples)
- [为何选择 Ray？](#why-ray)
- [技术概览](#technical-overview)
- [垃圾回收](#garbage-collection)
- [兼容性列表](#compatibility-list)
- [文档](#documentation)
- [国际化](#internationalization)
- [第三方库](#third-party-libraries)
- [CMake 预设](#cmake-presets)
- [代码库与成熟度](#codebase--maturity)
- [质量保证](#quality-assurance)
- [采用状态](#adoption-status)
- [仓库结构](#repository-structure)
- [资源文件格式](#asset-file-formats)
- [游戏打包与发行](#game-packaging-distribution)
- [引擎功能列表](#engine-feature-list)
- [截图](#screenshots)
- [版本策略](#versioning-policy)
- [许可证](#license)
- [支持与联系](#support--contact)
- [社区](#community)
- [贡献](#contribution)
- [传承：伟大的旅程](#lineage-the-grand-journey)
- [为何选择 Suika3？：我们的理念](#why-suika3-our-philosophy)
- [常见问题](#faq)

---

## 看板（状态）

**当前版本为 `26.05.x`：**

- 质量每日提升，`26.05.x` 现已被视为稳定版本。
- 我们目前处于`质量稳定期`（2026 年 4 月 1 日 - 6 月 30 日），为即将发布的 `Suika3 26.07 LTS`（计划于 2026 年 7 月 1 日）做准备。
- 虽然可能仍存在一些轻微 Bug，但在 LTS 发布前将全部解决。
- 所有问题的详细列表可在 [BUGS.md](BUGS.md) 中找到。
- 详情请参阅[质量保证](#quality-assurance)。

**当前状态：**

- ✅ 清理 Suika2 代码库（OpenNovel）（2024 年 6 月 - 2024 年 11 月）
- ✅ 实现脚本语言（NoctLang）（2024 年 12 月 - 2025 年 3 月）
- ✅ 实现 2D 游戏引擎（Playfield Engine）（2025 年 3 月 - 2025 年 10 月）
- ✅ 实现标签执行引擎（Suika3）（2026 年 1 月 - 2026 年 2 月）
- ✅ 将所有 C 函数重构为稳定的"C API"（2026 年 1 月 - 2026 年 2 月）
- ✅ 用 C 实现所有标签（2026 年 1 月 - 2026 年 2 月）
- ✅ 为 Ray 封装"C API"（2026 年 2 月 - 2026 年 3 月）
- ✅ API 冻结（2026 年 3 月 7 日）
- ✅ GUI 动画实现（2026 年 3 月 10 日）
- ✅ 代码冻结（2026 年 3 月 12 日）
- ✅ 里程碑：`Suika3 26.04（=LTS RC1）`（2026 年 4 月 1 日）
- ✅ 里程碑：`Suika3 26.05（=LTS RC2）`（2026 年 5 月 1 日）
- 里程碑：`Suika3 26.06（=LTS RC3/GM）`（2026 年 6 月 1 日）
- 目标：`Suika3 26.07 LTS` 公开发布（2026 年 7 月 1 日）

**剩余任务：**
- 文档：`SRS：系统需求规范`
- 文档：`SDS：系统设计规范`

---

## 快速入门指南

另见 [快速入门指南](docs/mkdocs-en/getting-started.md)

本指南将帮助您通过几个简单步骤快速启动您的第一个视觉小说项目。

### 安装

让我们先让引擎运行起来，见证奇迹的发生！

**Windows：**
- **下载并解压**
    - 下载 [Suika3-full.zip](https://github.com/awemorris/suika3/releases/latest/download/Suika3-full.zip) 并解压到您喜欢的文件夹。
- **启动**
    - 打开文件夹并运行 `suika3.exe` 以启动示例游戏！

**macOS：**
- **下载并解压**
    - 下载 Suika3-SDK-Full.zip 并解压到您喜欢的文件夹。
- **挂载磁盘镜像**
    - 进入 `SDK/macos/` 并打开 `Suika3.dmg`。
- **设置应用包**
    - 将 DMG 中的 `Suika3` 应用复制到与 `suika3.exe`（及数据文件夹）相同的位置。
    - 注意：应用包必须与您的游戏数据位于同一目录才能正常运行。
- **启动**
    - 双击 `Suika3` 应用以启动示例游戏！

**Linux：**
- **下载并解压**
    - 下载 Suika3-full.zip 并解压到您喜欢的目录。
- **安装 Flatpak 包**
    - 进入 `SDK/linux/` 并打开 `Suika3.flatpak`（或运行 `flatpak install --user Suika3.flatpak`）。
    - 这将 `.novel` 和 `.ray` 文件与 Suika3 引擎关联。
- **启动**
    - 打开解压后的文件夹，双击 `start.novel` 启动示例游戏！

### 个性化您的故事（`start.novel`）

现在，让游戏说出您想要的内容。

- **打开：**
    - 在项目文件夹中找到 `start.novel` 文件，用您喜欢的文本编辑器打开它。
- **编辑：**
    - 在文件开头添加以下标签：
    ```
    [text text="Hello, world! This is my first game."]
    ```
- **测试：**
    - 保存文件并再次运行 Suika3。您应该能在屏幕上看到新消息！

- **编辑：** 用以下命令替换现有文字：
```
[text text="Hello, world! This is my first game."]
```
- **测试：** 保存文件并再次运行 `suika3.exe`。您应该能在屏幕上看到新消息！

### 深入了解（高级技巧）

您可以轻松更改游戏的屏幕尺寸。

- **定位：** 在编辑器中打开 `main.ray` 文件。
- **修改：** 找到 `func setup()` 部分。您可以在此更改分辨率和窗口标题：
```
// 当窗口打开时调用
func setup() {
    return {
        width:      1280,            // 游戏宽度
        height:     720,             // 游戏高度
        title:      "My First Game", // 游戏标题
        fullscreen: false            // 设为 true 以进入全屏模式
    };
}
```

`main.ray` 文件底部包含用 `Ray` 编写的核心游戏逻辑。除非您进行高级自定义，否则最好保持这些函数不变：

- `func start()`：游戏启动时调用一次。
- `func update()`：每帧调用以处理游戏逻辑。
- `func render()`：更新完成后每帧调用以绘制屏幕上的所有内容。

```
// 在游戏开始前调用
func start() {
    // 在此加载插件
    // Suika.loadPlugin("testplugin");

    // 请勿删除以下行
    Suika.start();
}

// 在帧渲染前调用
func update() {
    // 请勿删除以下行
    Suika.update();
}

// 每帧渲染时调用
func render() {
    // 请勿删除以下行
    Suika.render();
}
```

> [!TIP]
> 这些函数是驱动 Suika3 的 `Playfield Engine` 的核心机制。Suika.start()、Suika.update() 和 Suika.render() 必须保留在原位，才能使游戏正常运行。

---

## 快速浏览

### NovelML

`start.novel` 文件示例如下：

```
# 显示背景图
[bg file="bg/coast.png" time="0.5"]

# 显示角色图
[ch center="ch/midori-normal.png" time="0.5" fade="normal"]

# 显示问题文字
[text text="请选择一个名字。"]

# 显示选项
[choose
    name="choose_result"
    text1="三月"
    text2="四月"
    text3="五月"
]

# 根据选择结果分支
[if lhs="${choose_result}" op="==" rhs="March"]
    [set name="name" value="March"]
[elseif lhs="${choose_result}" op="==" rhs="April"]
    [set name="name" value="April"]
[else]
    [set name="name" value="May"]
[endif]

# 显示文字
[text name="${name}" text="你好！我的名字是 ${name}。"]
```

---

## 示例

发行版 zip 中包含[示例游戏](game)。

查看 `game/` 文件夹，内含：
- 演示项目
- 示例资源
- NovelML 用法
- Ray 用法

---

### 为何选择 Ray？

- **即时迭代：** 无需编译等待。内置 JIT 编译器在编辑后立即运行脚本，您可以实时调整游戏并看到效果。

- **真正的原生性能：** 在 iOS、Android 和主机上以全速运行扩展。即使在 JIT 受限的平台上，借助 AOT，您也无需牺牲性能。Ray 是原生技术。

- **沙箱模型：** 脚本无法访问任意文件/网络。只能通过引擎管理的 API 访问游戏资源和存档数据。

- **顺利通过商店审核：** 大幅降低被拒的风险。由于最终构建通过 AOT 生成原生代码，您将轻松通过 App Store 和主机认证。

- **易学易用，功能强大：** 受 JavaScript 启发的语法对初学者友好，同时为复杂系统提供了资深开发者所期望的深度灵活性。

- **长期稳定性：** 由于我们自研该语言，您不会受到上游项目重大变更的影响。我们掌控并拥有完整技术栈，因此您的脚本将永远保持兼容。

简而言之，由于找不到一个能将 JIT、AOT 和解释器整合到单一项目的实用免费语言，我们自己创造了一个。

---

## 技术概览

如果以下规格令您兴奋，您大概来对地方了。

Suika3 不只是一个带脚本的 SDL 封装。它拥有自己的渲染和音频后端，以及自己的脚本语言，将其定位为一个完全独立的游戏引擎。

### 核心架构

Suika3 基于 `PlayField Engine`，一个全面的 2D 游戏引擎。这意味着 Suika3 可以使用 Playfield API 完全扩展。

Playfield Engine 最初专为 Suika3 开发。"Playfield"这个名称是 Awe 在 SIE PlayStation 固件团队工作期间受 PlayStation 启发而取的。

```
+------------------------------+
|        NovelML (Tags)        | --> 将扩展到其他游戏类型
+------------------------------+
|     Plugin Tags (by Ray)     | --> Ray 可以编译成原生二进制！
+------------------------------+
|       Base Tags (by C)       |
+------------------------------+
|       Ray Wrapper API        |
+------------------------------+
|         Suika3 C API         |
+------------------------------+
|       Playfield C API        |
+---------------+--------------+
|   StratoHAL   |   NoctLang   |
+---------------+--------------+
|       Operating System       |
+------------------------------+
```

- **脚本**：集成 [NoctLang](https://github.com/awemorris/NoctLang)，一种专为游戏脚本设计的小巧而强大的语言。

* **渲染**：支持原生 DirectX 9/11/12、Metal、OpenGL、OpenGL ES 和 WebGL，兼容性广泛。

* **音频**：通过原生 DirectSound 或 XAudio2（Windows）、Audio Unit（macOS/iOS）、ALSA（Linux）、OSS（BSD）等 API 提供轻量级音频支持。

### StratoHAL

StratoHAL 起源于 2001 年开发的 2D 游戏引擎代码库，采用 Zlib 许可证，拥有卓越稳定性的良好记录。

历经四分之一世纪从 Windows 9x 时代不断演进，StratoHAL 已扩展支持 macOS、Linux、iOS、Android、WebAssembly 和 Unity。它在智能手机上可靠运行已超过十年。

尽管 SDL3 已作为流行的自由/开源软件替代方案存在，StratoHAL 还额外提供：

- 与 SDL3 相同的主要平台支持。

- 独特地通过 Unity 集成提供主机支持，源代码树中不依赖任何受 NDA 限制的代码。

- 针对旧平台的软件 3D 渲染。

### 平台支持与组件

|平台类型  |操作系统/平台       |图形                 |音频                  |SDK                  |
|---------------|--------------------|-------------------------|-----------------------|---------------------|
|桌面端        |Windows             |DirectX 12/11/9          |DirectSound            |Win32 API            |
|               |macOS               |Metal                    |Audio Unit             |AppKit (Objective-C) |
|               |ChromeOS            |WebGL 2                  |OpenAL (Emscripten)    |Emscripten (C)       |
|               |Linux               |OpenGL 3                 |ALSA                   |C, X11 or Wayland    |
|               |*BSD                |OpenGL 3                 |/dev/dsp \| /dev/audio |C, X11               |
|               |Solaris 11          |Software                 |/dev/dsp               |C, X11               |
|               |Solaris 10          |Software                 |/dev/audio             |C, X11               |
|               |Qt                  |OpenGL 3                 |Qt Sound               |Qt                   |
|移动端         |iOS                 |Metal                    |Audio Unit             |UIKit (Objective-C)  |
|               |Android             |OpenGL ES 2              |OpenSL ES              |Android NDK          |
|               |HarmonyOS NEXT      |OpenGL ES 2              |OpenSL ES              |OpenHarmony SDK      |
|Web            |WebAssembly (Wasm)  |WebGL 2                  |OpenAL (Emscripten)    |Emscripten (C)       |
|主机        |Unity               |Unity                    |Unity                  |Unity Native Plugin  |
|               |Xbox Series X\|S    |DirectX 12               |XAudio2                |Microsoft GDK        |

### 主机 Unity 插件说明

Playfield Engine 为包括 Windows 64 位和游戏主机在内的平台提供 Unity 插件二进制文件。这些二进制文件完全使用官方版本的 LLVM/Clang 工具链构建（无专有 SDK）。

对于 Xbox 系列，您可以直接使用原生 Microsoft GDK 移植版，无需通过 Unity。

### NoctLang

```
Ray = NoctLang + Suika3 API + Playfield API
```

**NoctLang** 是一种专为应用内脚本设计的轻量级脚本语言。其面向游戏的语法强调清晰性、即时启动和与引擎的紧密集成。

内置 JIT 编译器支持广泛的 CPU 架构，覆盖大多数游戏主机和智能手机，包括：

- ✅ Intel x86（Xbox）[jit-x86.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-x86.c)
- ✅ AMD64/x86_64（PS4/PS5/Xbox One/Xbox series X|S）[jit-x86_64.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-x86_64.c)
- ✅ ARMv5-ARMv7（Nintendo DS/PS Vita）[jit-arm32.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-arm32.c)
- ✅ Arm64（Switch/Switch2）[jit-arm64.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-arm64.c)
- ✅ PowerPC 32（Wii/GameCube）[jit-ppc32.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-ppc32.c)
- ✅ PowerPC 64（PS3/Xbox 360）[jit-ppc64.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-ppc64.c)
- ✅ MIPS32（PS1/PSP）[jit-mips32.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-mips32.c)
- ✅ MIPS64（N64/PS2）[jit-mips64.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-mips64.c)
- ✅ RISC-V 32（未来设备）[jit-riscv32.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-riscv32.c)
- ✅ RISC-V 64（未来设备）[jit-riscv64.c](https://github.com/awemorris/suika3/blob/main/external/PlayfieldEngine/external/NoctLang/src/core/jit-riscv64.c)

这些架构支持良好，至少它们都通过了[测试套件](external/PlayfieldEngine/external/NoctLang/tests/run-syntax.sh)。

但以下架构由于缺少开发机器，目前尚不支持（仅限解释器）：

- ❌ SH-4（Dreamcast）（运行解释器）
- ❌ Sun SPARC（运行解释器）
- ❌ HP PA-RISC（运行解释器）
- ❌ Motorola 68000（运行解释器）
- ❌ Loongson（运行解释器）
- ❌ IBM Z（运行解释器）
- **挑战：** 如果您拥有其中一台，请提供 3 天的 SSH 访问开发环境。我们可以移植过去 ;-)

### AOT 编译

对于 JIT 受限的平台（如移动端或主机），NoctLang 可以至少回退到解释器模式，以及使用 C 源代码后端的现代 AOT（提前编译）——即使在严格受控的环境中也能确保完全兼容。

详情请参阅 [AOT](docs/mkdocs-en/docs/aot.md)。

### 脚本执行模式

|平台          |模式               |
|------------------|-------------------|
|Windows x86       |JIT                |
|Windows x64       |JIT                |
|Windows arm64     |JIT                |
|macOS x86_64      |JIT                |
|macOS arm64       |JIT                |
|Linux x86         |JIT                |
|Linux x86_64      |JIT                |
|Linux armv7       |JIT                |
|Linux arm64       |JIT                |
|iOS               |Interpreter or AOT |
|Android           |Interpreter or AOT |
|HarmonyOS NEXT    |Interpreter or AOT |
|WebAssembly       |Interpreter or AOT |
|Unity Plugin      |Interpreter or AOT |
|Xbox              |Interpreter or AOT |
|FreeBSD           |JIT                |
|NetBSD            |JIT                |
|OpenBSD           |Interpreter or AOT |
|Solaris 11 x86_64 |JIT                |
|Solaris 11 Sparc  |Interpreter or AOT |

### 运行时占用

Suika3 的占用空间非常小。

| 操作系统           | 二进制大小  | 内存占用                |
|--------------|--------------|-----------------------------|
| Windows 11   | 2 MB         | 任务管理器中约 300 MB  |
| Windows 2000 | 3 MB         | 任务管理器中约 8 MB    |

> [!TIP]
> 由于现代图形架构，使用 DirectX 12 的游戏应用即使在加载任何游戏资源之前通常也会消耗至少 300 MB 内存。引擎本身在 Windows 2000 上仅消耗 8 MB。

### JIT 流水线

NoctLang 使用双 IR 架构，其中 HIR 负责分析，LIR 统一了解释器、JIT 和 AOT 后端的执行：

- **HIR（高级中间表示）**
    - 用于程序分析的结构化控制流图（CFG）。
    - 用于代数化简的表达式 DAG。
    - 未来高级优化的基础。

```
CFG for "func foo(a) { if (a > 0) { return a; } else { return -a; } }"

  +---------------+
  | 0: Func Block |         -- pred: none, succ: 1
  +---------------+
     +-------------+
     | 1: IF Block |        -- pred: 0, succ: 2 (true), 3 (false)
     +-------------+
        +----------------+
        | 2: Basic Block |  -- pred 1, succ 5
        +----------------+
     +---------------+
     | 3: Else Block |      -- pred 1, succ 4
     +---------------+
        +----------------+
        | 4: Basic Block |  -- pred 3, succ 5
        +----------------+
  +--------------+
  | 5: End Block |          -- pred 2, 4
  +--------------+
                                 (pred = predecessor, succ = successor)
     
```

- **LIR（低级中间表示）**
    - 虚拟机字节码，作为解释和 JIT 代码生成输入的主要格式。
    - 高抽象层次，实现快速、可移植的解释。
    - 足够紧凑，可在 JIT 中高效降低为机器码。

```
  LIR for "a = 1 + 2"

    ICONST       %0, 1               ; 加载常量 1
    ICONST       %1, 2               ; 加载常量 2
    ADD          %2, %0, %1          ; 计算总和
    STORESYMBOL  "a", %2             ; 将结果存入全局变量 "a"
```

编译阶段如下所示：

```
 +-----+     +-----+     +-----+     +-----+
 | SRC | --> | AST | --> | HIR | --> | LIR | -----> [解释器后端]
 +-----+     +-----+     +-----+     +-----+   |
                                               +--> [JIT 后端]
                                               |
                                               +--> [C 后端]
```

HIR 和 LIR 的分离实现了：

- **轻量 JIT 流水线**：从分析到代码生成的最小开销。
- **架构清晰**：每个阶段都有明确定义的职责，简化维护。
- **可移植性**：相同的 LIR 可以直接解释或降低为优化的机器码。

如上所示，HIR 表达结构，而 LIR 表达执行。这种分离使 NoctLang 在不牺牲优化机会的情况下保持 JIT 流水线轻量。

由于所有 JIT 后端都从相同的 LIR 进行转换，跨架构的可移植性自然而然地实现了。这种统一方法使 NoctLang 既具有可移植性又易于维护。

### 统一执行模型

NoctLang 在其 JIT、AOT 和解释器执行模型中保持严格的字节码语义。每条 NoctLang 字节码指令直接映射到相应的运行时 C 函数。在 NoctLang JIT（方法级基准 JIT）中，每条字节码指令都被翻译为运行时函数调用。同样的机制适用于 AOT 和解释器执行。因此，所有三种执行模型都利用统一的基础设施，确保完全的语义等价。

这种简洁、统一的执行模型代表了 NoctLang 的核心创新。据我们所知，NoctLang 是第一个在所有执行模式中统一 JIT、AOT 和解释器执行同时保持严格语义一致性的实用语言。

---

## 垃圾回收

`Ray` 具有高性能的分代垃圾回收器，灵感来源于 Java HotSpot VM 的架构。这种设计确保开发者可以专注于创作，而不会被令人头疼的"GC 卡顿"或帧率下降所打断。

脚本中的对象（字符串、字典）由 GC 管理，而纹理等大型资源由原生代码管理。

### 核心机制：分代 GC

系统将对象分为两组以优化内存管理：

* 新生代：大多数对象生命周期短暂。Suika3 使用高速复制算法（半空间复制 GC）处理这些对象，可以瞬间清除临时数据。（通常 < 0.1ms）

* 老生代：长期存活的对象被移到这里。该区域使用标记-清除-压缩 GC 算法，定期重组内存以防止碎片化。（通常 10-300ms）

如需了解更详细的实现，请查看 [gc.h](external/PlayfieldEngine/external/NoctLang/src/core/gc.h) 和 [gc.c](external/PlayfieldEngine/external/NoctLang/src/core/gc.c)。

### 帧同步延迟隐藏

Ray 真正的"魔法"在于其时序。通过在每一帧执行新生代复制 GC，系统有效地将 GC 处理时间隐藏在自然帧间隔中。

得益于这种分代策略，更重的老生代标记清除很少被触发，为玩家保持恒定的 60 fps 体验。

---

## 兼容性列表

### 平台可用性概览

`Supported（已支持）`表示上游（`Playfield Engine`）完全支持它。

| 类别    | 操作系统/环境   | 状态       | 最后检查时间 | 检查环境                       |
|-------------|--------------------|--------------|--------------|----------------------------------|
| **桌面端** | Windows            | ✅ 已支持 | 2026年4月3日 | Windows 11 (x64/Arm64)           |
|             | macOS              | ✅ 已支持 | 2026年4月3日 | macOS 26 Tahoe (Apple Silicon)   |
|             | Linux              | ✅ 已支持 | 2026年4月3日 | Ubuntu 24.04 LTS (x86_64)        |
| **移动端**  | iOS                | ✅ 已支持 | 2026年4月3日 | iOS 18                           |
|             | Android            | ✅ 已支持 | 2026年4月3日 | Android 15                       |
|             | HarmonyOS NEXT     | ✅ 已支持 | -            | API 10+                          |
| **BSD**     | FreeBSD            | ✅ 已支持 | 2026年4月5日 | 15.0-RELEASE amd64               |
|             | NetBSD             | ✅ 已支持 | 2026年4月5日 | 10.0 amd64, aarch64, armv7       |
|             | OpenBSD            | ✅ 已支持 | 2026年4月5日 | 7.8 amd64, aarch64, armv7        |
| **Web**     | WebAssembly (Wasm) | ✅ 已支持 | 2026年4月3日 | Chrome, Edge, Safari             |
|             | Chromebook         | ✅ 已支持 | -            | Chrome Browser / Linux Container |
| **其他**   | Unity 集成  | ✅ 已支持 | -            | Unity 6.2 (Windows x86_64)       |

### 64 位 Windows 二进制兼容性列表

官方推荐二进制为 64 位版本。

| 操作系统      | 版本                     | 补丁 | CPU    | 运行时                              | 64位二进制 | Direct3D |
|---------|-----------------------------|-------|--------|---------------------------------------|---------------|----------|
| Windows | 11                          |       | x64    | （无需）                       | ✅            | 12.0     |
| Windows | 11                          |       | arm64  | （无需）                       | ✅            | 12.0     |
| Windows | 10                          |       | x64    | （无需）                       | ✅            | 12.0     |
| Windows | 10                          |       | arm64  | （无需）                       | ✅            | 12.0     |
| Windows | 8.1                         |       | x64    | （无需）                       | ✅            | 11.0     |
| Windows | 8                           |       | x64    | （无需）                       | ✅            | 11.0     |
| Windows | 7                           | SP1   | x64    | （无需）                       | ✅            | 11.0     |
| Windows | 7                           |       | x64    | UCRT Update (KB2999226)               | ✅            | 11.0     |
| Windows | Vista                       | SP2   | x64    | Platform Update                       | ✅            | 11.0     |
| Windows | Vista                       | SP1   | x64    | DirectX End-User Runtimes (June 2010) | ✅            | 9.0      |
| Windows | Vista                       |       | x64    | DirectX End-User Runtimes (June 2010) | ✅            | 9.0      |
| Windows | XP Professional x64 Edition | SP2   | x64    | DirectX End-User Runtimes (June 2010) | ✅            | 9.0      |
| Windows | XP Professional x64 Edition | SP1   | x64    | DirectX End-User Runtimes (June 2010) | ✅            | 9.0      |
| Windows | XP Professional x64 Edition |       | x64    | DirectX End-User Runtimes (June 2010) | ✅            | 9.0      |

### 32 位 Windows 兼容性列表

Suika3 提供 32 位二进制 `suika3-32.exe` 以实现向后兼容，通过旧版运行时支持遗留系统。

| 操作系统      | 版本                     | 补丁 | CPU    | 运行时                               | 32位二进制 | Direct3D               |
|---------|-----------------------------|-------|--------|----------------------------------------|---------------|------------------------|
| Windows | 11                          |       | x64    | （无需）                        | ✅            | 12.0                   |
| Windows | 11                          |       | arm64  | （无需）                        | ✅            | 12.0                   |
| Windows | 10                          |       | x86    | （无需）                        | ✅            | 12.0                   |
| Windows | 10                          |       | x64    | （无需）                        | ✅            | 12.0                   |
| Windows | 10                          |       | arm64  | （无需）                        | ✅            | 12.0                   |
| Windows | 8.1                         |       | x86    | （无需）                        | ✅            | 11.0                   |
| Windows | 8.1                         |       | x64    | （无需）                        | ✅            | 11.0                   |
| Windows | 8                           |       | x86    | （无需）                        | ✅            | 11.0                   |
| Windows | 8                           |       | x64    | （无需）                        | ✅            | 11.0                   |
| Windows | 7                           | SP1   | x86    | （无需）                        | ✅            | 11.0                   |
| Windows | 7                           |       | x86    | （无需）                        | ✅            | 11.0                   |
| Windows | 7                           | SP1   | x64    | （无需）                        | ✅            | 11.0                   |
| Windows | 7                           |       | x64    | （无需）                        | ✅            | 11.0                   |
| Windows | Vista                       | SP2   | x86    | DirectX 11 Platform Update             | ✅            | 11.0                   |
| Windows | Vista                       | SP1   | x86    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | Vista                       |       | x86    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | Vista                       | SP2   | x64    | DirectX 11 Platform Update             | ✅            | 11.0                   |
| Windows | Vista                       | SP1   | x64    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | Vista                       |       | x64    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | XP                          | SP3   | x86    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | XP                          | SP2   | x86    |                                        | -->           | 需要 VS2008            |
| Windows | XP                          | SP1   | x86    |                                        | -->           | 需要 VS2008            |
| Windows | XP                          |       | x86    | DirectX 9.0b Runtime                   | ✅            | 9.0                    |
| Windows | XP Professional x64 Edition | SP2   | x64    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | XP Professional x64 Edition | SP1   | x64    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | XP Professional x64 Edition |       | x64    | DirectX End-User Runtimes (June 2010)  | ✅            | 9.0                    |
| Windows | 2000                        | SP4   | x86    | DirectX End-User Runtimes (June 2010)  | -->           | 需要 VS2008            |
| Windows | 2000                        | SP3   | x86    | DirectX End-User Runtimes (June 2010)  | -->           | 需要 VS2008            |
| Windows | 2000                        | SP2   | x86    | DirectX End-User Runtimes (June 2010)  | -->           | 需要 VS2008            |
| Windows | 2000                        | SP1   | x86    | DirectX End-User Runtimes (June 2010)  | -->           | 需要 VS2008            |
| Windows | 2000                        |       | x86    | DirectX End-User Runtimes (June 2010)  | -->           | 需要 VS2008            |
| Windows | Me                          |       | x86    |                                        | -->           | 需要 VC++ 6.0          |
| Windows | 98                          |       | x86    |                                        | -->           | 需要 VC++ 6.0          |
| Windows | 95                          |       | x86    |                                        | -->           | 需要 VC++ 6.0          |
| Windows | NT 4.0                      |       | x86    |                                        | -->           | 需要 VC++ 6.0          |
| Windows | NT 3.51                     |       | x86    |                                        | ❌            | Win32 API 不足 |

### macOS 兼容性列表

| 操作系统                     | 版本 | Mac CPU              | 状态                       |
|------------------------|---------|----------------------|------------------------------|
| macOS Tahoe            | 26.0    | arm64 / x86_64       | ✅ 正常                        |
| macOS Sequoia          | 15.0    | arm64 / x86_64       | ✅ 正常                        |
| macOS Sonoma           | 14.0    | arm64 / x86_64       | ✅ 正常                        |
| macOS Ventura          | 13.0    | arm64 / x86_64       | ✅ 正常                        |
| macOS Monterey         | 12.0    | arm64 / x86_64       | ✅ 正常                        |
| macOS Big Sur          | 11.0    | arm64 / x86_64       | ✅ 正常                        |
| macOS Catalina         | 10.15   | x86_64               | ✅ 正常                        |
| macOS Mojave           | 10.14   | x86_64               | ✅ 正常                        |
| macOS High Sierra      | 10.13   | x86_64               | ✅ 正常                        |
| macOS Sierra           | 10.12   | x86_64               | ✅ 正常                        |
| OS X El Capitan        | 10.11   | x86_64               | ✅ 正常                        |
| OS X Yosemite          | 10.10   | x86_64               | ❌ 无 Metal                  |
| OS X Mavericks         | 10.9    | x86_64               | ❌ 无 Metal                  |
| Mac OS X Puma          | 10.1    | ppc                  | ❌ 无 Metal，无 AVFoundation |
| Mac OS X Cheetah       | 10.0    | ppc                  | ❌ 无 Metal，无 AVFoundation |

### Linux 兼容性列表

| 发行版      | 版本               | CPU             | 状态 | 图形                                |
|-------------------|-----------------------|-----------------|--------|-----------------------------------------|
| Debian            | 13 / 12               | x86_64, arm64   | ✅     | X11 + OpenGL 3 或 Wayland + OpenGL ES 3 |
| Raspberry Pi OS   | Debian 13             | arm64, armv7    | ✅     | X11 + OpenGL ES                         |
| Ubuntu            | 24.04 / 22.04 / 20.04 | x86_64, arm64   | ✅     | X11 + OpenGL 3 或 Wayland + OpenGL ES 3 |
| Kubuntu           | 25.04                 | x86_64, arm64   | ✅     | X11 + OpenGL 3 或 Wayland + OpenGL ES 3 |
| Linux Mint        | 22.3                  | x86_64          | ✅     | X11 + OpenGL 3 或 Wayland + OpenGL ES 3 |
| Fedora            | 43                    | x86_64          | ✅     | X11 + OpenGL 3 或 Wayland + OpenGL ES 3 |
| Odroid Variants   |                       | arm64           | ✅     | GBM + DRM + EGL + OpenGL ES             |

### iOS 兼容性列表

| 操作系统     | 状态   |
|--------|----------|
| iOS 26 | ✅       |
| iOS 18 | ✅       |
| iOS 17 | ✅       |
| iOS 16 | ✅       |
| iOS 15 | ✅       |
| iOS 14 | ✅       |
| iOS 13 | ✅       |
| iOS 12 | ✅       |
| iOS 11 | ✅       |
| iOS 10 | ✅       |
| iOS 9  | ✅       |
| iOS 8  | ✅       |
| iOS 7  | 无 Metal |

### Android 兼容性列表

| 操作系统          | 状态 |
|-------------|--------|
| Android 16  | ✅     |
| Android 15  | ✅     |
| Android 14  | ✅     |
| Android 13  | ✅     |
| Android 12  | ✅     |
| Android 11  | ✅     |
| Android 10  | ✅     |
| Android 9   | ✅     |
| Android 8   | ✅     |
| Android 7   | ✅     |
| Android 6   | ✅     |
| Android 5   | ✅     |
| Android 4.4 | ✅     |

### HarmonyOS / OpenHarmony 兼容性列表

| 操作系统         | 状态 |
|------------|--------|
| API 20     | ✅     |
| API 12     | ✅     |

### FreeBSD

| 操作系统         | 状态      |
|------------|-------------|
| FreeBSD 15 | ✅          |
| FreeBSD 14 | ✅          |

### NetBSD

| 操作系统         | 状态      |
|------------|-------------|
| NetBSD 10  | ✅          |
| NetBSD 9   | ✅          |
| NetBSD 8   | ✅          |

### OpenBSD

| 操作系统           | 状态      |
|--------------|-------------|
| OpenBSD 7.8  | ✅          |

### Solaris

| 操作系统         | 状态      |
|------------|-------------|
| Solaris 11 | ✅          |
| Solaris 10 | ✅          |
| Solaris 9  | 未检查 |
| Solaris 8  | 未检查 |
| Solaris 7  | 未检查 |

---

## 文档

文档可在官网查阅：
- [English](https://suika3.vn/en/docs/)
- [Spanish](https://suika3.vn/es/docs/)
- [French](https://suika3.vn/fr/docs/)
- [German](https://suika3.vn/de/docs/)
- Italian（翻译中）
- [Russian](https://suika3.vn/ru/docs/)
- Greek（翻译中）
- [简体中文](https://suika3.vn/zh-Hans/docs/)
- [繁体中文](https://suika3.vn/zh-Hant/docs/)
- [日本語](https://suika3.vn/ja/docs/)

---

## 国际化

Suika3 支持以下语言。

| 语言               | 语言代码    | 翻译类型         | 翻译范围                             | 进度      |
|------------------------|-------------|--------------------------|----------------------------------|---------------|
| English（默认）     | `en`        | 原始版本                 | UI / 文档 / 示例              | 基准      |
| English（美式）      | `en-us`     | 无                     | UI                               | -             |
| English（英式）      | `en-gb`     | 无                     | UI                               | -             |
| Spanish（默认）     | `es`        | 机器翻译      | UI                               | 完成          |
| Spanish（西班牙）        | `es-es`     | 无                     | UI                               | -             |
| Spanish（拉丁美洲）| `es-la`     | 无                     | UI                               | -             |
| French（默认）      | `fr`        | 机器翻译      | UI                               | 完成          |
| French（法国）        | `fr-fr`     | 无                     | UI                               | -             |
| French（加拿大）        | `fr-ca`     | 无                     | UI                               | -             |
| Italian                | `it`        | 机器翻译      | UI                               | -             |
| German                 | `de`        | 机器翻译      | UI                               | 完成          |
| Greek                  | `el`        | 机器翻译      | UI                               | 完成          |
| Russian                | `ru`        | 机器翻译      | UI                               | 完成          |
| 简体中文     | `zh-cn`     | 机器翻译      | UI                               | 完成          |
| 繁体中文    | `zh-tw`     | 机器翻译      | UI                               | 完成          |
| 日本語               | `ja`        | 原生翻译       | UI                               | 完成          |

### 如何切换语言

Suika3 使用系统区域设置。要切换语言，请设置您的系统语言。

此外，示例游戏的配置界面中有语言切换按钮。

### 贡献翻译

欢迎社区贡献以改善我们的翻译！
如果您想帮助我们触达更多开发者，以下是贡献方式：

0.  执行 `grep -r _TR() .` 以查找原始消息。
1.  **定位文件**：翻译资源分布在三个核心目录中：
    - `resources/i18n/message.txt`（Suika3 部分，`S3_TR()`）
    - `external/PlayfieldEngine/resources/i18n/message.txt`（Playfield Engine 部分，`PF_TR()`）
    - `external/PlayfieldEngine/external/NoctLang/i18n/message.txt`（NoctLang 部分，`N_TR()`）
    - `external/PlayfieldEngine/external/StratoHAL/i18n/message.txt`（StratoHAL 部分，`HAL_TR()`）
2.  **提交更改**：
    - 发现错别字或奇怪的机器翻译？欢迎提交 **Pull Request**。
    - 想添加新语言？请先开一个 **Issue** 以便协调！

> [!TIP]
> 人工/专业翻译优先于机器生成内容。您的人工润色大有裨益！

---

## 第三方库

我们的引擎建立在多个自由/开源软件库之上。为确保构建可重复性和长期可维护性，所有必要的源代码压缩包和补丁都捆绑在本仓库中，位于 `external/PlayfieldEngine/external/StratoHAL/lib/` 目录下。

### 核心库

| 库          | 用途             | 主要特性                                            |
|------------------|---------------------|--------------------------------------------------------|
| Playfield Engine | 2D 游戏引擎      | 我们的基础游戏引擎（自研）                       |
| NoctLang         | 脚本语言  | 我们的脚本语言（自研）                     |
| zlib             | 压缩         | 通用数据压缩的 Deflate 算法        |
| libpng           | 图像               | 支持 PNG 图像的参考库           |
| JPEG9            | 图像               | 工业标准 JPEG 图像解压缩          |
| libwebp          | 图像               | 现代高效图像格式支持          |
| FreeType2        | 字体                | 高质量字体渲染和字形处理      |
| libogg           | 音频容器     | Ogg 多媒体文件的比特流处理           |
| libvorbis        | 音频编解码器         | 用于 BGM 和 SE 的有损音频压缩           |
| brotli           | 压缩         | 用于 Web 和数据资产的高压缩比压缩（WOFF） |
| bzip2            | 压缩         | 用于归档的高质量数据压缩器             |

### 许可证合规

每个库均按其各自的自由/开源软件许可证使用。请参阅本仓库中的 `NOTICE` 文件，了解每个许可证和版权声明的完整文本。

---

## CMake 预设

Suika3 附带涵盖各种平台和构建配置的 CMake 预设。

|预设                              |平台              |编译器   |目录                              |目标        |类型           |
|------------------------------------|----------------------|-----------|---------------------------------------|--------------|---------------|
|windows-vs2022-x86-debug            |Windows               |MSVC       |out/build/windows-vs2022-x86-debug     |suika3.exe    |可执行文件     |
|windows-vs2022-x86-release          |Windows               |MSVC       |out/build/windows-vs2022-x86-release   |suika3.exe    |可执行文件     |
|windows-vs2022-x64-debug            |Windows               |MSVC       |out/build/windows-vs2022-x64-debug     |suika3.exe    |可执行文件     |
|windows-vs2022-x64-release          |Windows               |MSVC       |out/build/windows-vs2022-x64-release   |suika3.exe    |可执行文件     |
|windows-vs2022-arm64-debug          |Windows               |MSVC       |out/build/windows-vs2022-arm64-debug   |suika3.exe    |可执行文件     |
|windows-vs2022-arm64-release        |Windows               |MSVC       |out/build/windows-vs2022-arm64-release |suika3.exe    |可执行文件     |
|windows-vs2022-gdk-desktop          |Windows               |MSVC       |out/build/windows-vs2022-gdk-desktop   |suika3.exe    |可执行文件     |
|windows-vs2022-gdk-xbox-xs          |Windows               |MSVC       |out/build/windows-vs2022-gdk-xbox-xs   |suika3.exe    |可执行文件     |
|windows-vs2026-x86-debug            |Windows               |MSVC       |out/build/windows-vs2026-x86-debug     |suika3.exe    |可执行文件     |
|windows-vs2026-x86-release          |Windows               |MSVC       |out/build/windows-vs2026-x86-release   |suika3.exe    |可执行文件     |
|windows-vs2026-x64-debug            |Windows               |MSVC       |out/build/windows-vs2026-x64-debug     |suika3.exe    |可执行文件     |
|windows-vs2026-x64-release          |Windows               |MSVC       |out/build/windows-vs2026-x64-release   |suika3.exe    |可执行文件     |
|windows-vs2026-x64-console-release  |Windows               |MSVC       |out/build/windows-vs2026-x64-release   |suika3.exe    |可执行文件     |
|windows-vs2026-arm64-debug          |Windows               |MSVC       |out/build/windows-vs2026-arm64-debug   |suika3.exe    |可执行文件     |
|windows-vs2026-arm64-release        |Windows               |MSVC       |out/build/windows-vs2026-arm64-release |suika3.exe    |可执行文件     |
|windows-vs2026-gdk-desktop          |Windows               |MSVC       |out/build/windows-vs2026-gdk-desktop   |suika3.exe    |可执行文件     |
|windows-vs2026-gdk-xbox-xs          |Windows               |MSVC       |out/build/windows-vs2026-gdk-xbox-xs   |suika3.exe    |可执行文件     |
|windows-mingw-x86                   |Windows               |MinGW-GCC  |build-mingw-x86                        |suika3.exe    |可执行文件     |
|windows-mingw-x86_64                |Windows               |MinGW-GCC  |build-mingw-x86_64                     |suika3.exe    |可执行文件     |
|windows-mingw-arm64                 |Windows               |MinGW-LLVM |build-mingw-arm64                      |suika3.exe    |可执行文件     |
|windows-mingw-win95                 |Windows 9x            |MinGW-GCC  |build-mingw-win95                      |suika3.exe    |可执行文件     |
|macos                               |macOS                 |Clang      |build-macos                            |Suika3.app    |应用包     |
|macos-cli                           |macOS (CLI)           |Clang      |build-macos                            |Suika3.app    |应用包     |
|linux                               |Linux (X11)           |GCC        |build-linux                            |suika3        |可执行文件     |
|linux-wayland                       |Linux (Wayland)       |GCC        |build-linux                            |suika3        |可执行文件     |
|linux-gdm                           |Linux (GBM)           |GCC        |build-linux                            |suika3        |可执行文件     |
|linux-gdm-rot90                     |Linux (GBM)           |GCC        |build-linux                            |suika3        |可执行文件     |
|linux-fbdev                         |Linux (fbdev)         |GCC        |build-linux                            |suika3        |可执行文件     |
|linux-x11soft                       |Linux                 |GCC        |build-linux                            |suika3        |可执行文件     |
|freebsd                             |FreeBSD               |Clang      |build-freebsd                          |suika3        |可执行文件     |
|netbsd                              |NetBSD                |GCC        |build-netbsd                           |suika3        |可执行文件     |
|openbsd                             |OpenBSD               |Clang      |build-openbsd                          |suika3        |可执行文件     |
|solaris11                           |Solaris11             |SunCC      |build-solaris11                        |suika3        |可执行文件     |
|solaris10                           |Solaris10             |SunCC      |build-solaris10                        |suika3        |可执行文件     |
|haiku                               |Haiku OS              |GCC        |build-haiku                            |suika3        |可执行文件     |
|wasm                                |WebAssembly           |Emscripten |build-wasm                             |index.html    |HTML + Wasm    |
|wasm-local                          |Chromebook            |Emscripten |build-wasm-local                       |index.html    |HTML + Wasm    |
|ios-device                          |iOS Device            |Clang      |build-ios-device                       |libsuika3.a   |静态库 |
|ios-simulator                       |iOS Simulator         |Clang      |build-ios-simulator                    |libsuika3.a   |静态库 |
|android-x86                         |Android x86           |Clang      |build-android-x86                      |libsuika3.so  |共享库 |
|android-x86_64                      |Android x86_64        |Clang      |build-android-x86_64                   |libsuika3.so  |共享库 |
|android-armv7                       |Android armv7         |Clang      |build-android-armv7                    |libsuika3.so  |共享库 |
|android-arm64                       |Android arm64         |Clang      |build-android-arm64                    |libsuika3.so  |共享库 |
|android-riscv64                     |Android riscv64       |Clang      |build-android-riscv64                  |libsuika3.so  |共享库 |
|openharmony-arm64                   |HarmonyOS NEXT arm64  |Clang      |build-openharmony-arm64                |libsuika3.a   |静态库 |
|openharmony-armv7                   |HarmonyOS NEXT armv7  |Clang      |build-openharmony-armv7                |libsuika3.a   |静态库 |
|openharmony-x86_64                  |HarmonyOS NEXT x86_64 |Clang      |build-openharmony-x86_64               |libsuika3.a   |静态库 |
|unity-win64                         |Unity Plugin          |Clang-CL   |build-unity-win64                      |libsuika3.dll |DLL 插件     |
|unity-switch                        |Unity Plugin          |Clang      |build-unity-switch                     |libsuika3.a   |静态库 |
|unity-ps5                           |Unity Plugin          |Clang      |build-unity-ps5                        |libsuika3.a   |静态库 |
|unity-xbox                          |Unity Plugin          |Clang      |build-unity-xbox                       |libsuika3.a   |静态库 |

---

## 代码库与成熟度

Suika3 是一款代码量超过 10 万行的健壮视觉小说引擎。这不是一个周末项目，而是历经 25 年以上演进的成熟代码库。

- **已验证的稳定性：** 包含自 2001 年以来精炼的核心模块。

- **现代架构：** 具有 2016 年独立出来的清晰 HAL（硬件抽象层）和 2022 年实现的高性能 GPU 渲染。

- **原生多平台：** 主要以 C 语言和平台原生语言构建，包括 C++（DirectX）、Swift（macOS/iOS）、Objective-C（macOS/iOS）、C#（Unity）和着色器（HLSL/GLSL/Metal）。

---

## 质量保证

在**软件工程**中，可靠性从根本上是时间的函数。由于 Suika3 于 2026 年 4 月新发布，引擎目前在现场测试正常运行时间方面处于早期生命周期阶段。因此，正式质量指标尚不完全适用。然而，架构继承了二十多年的开发经验，为通向首个 LTS（长期支持）的 QA 流程奠定了坚实基础。

### 通往稳定的道路

我们致力于提供生产级引擎。我们的 QA 路线图如下：

1. **Bug 追踪**：我们维护所有已识别问题的全面日志。参见 [BUGS.md](BUGS.md)

2. **数据驱动加固**：我们分析根本原因和解决率，以量化和提升软件稳定性。

3. **商业级标准**：我们的最终目标是达到满足商业应用生产严格要求的健壮性水平。

---

## 采用状态

我们旨在为"移动端视觉小说"开拓一个新市场，目前尚未建立成功案例记录。

如果您有兴趣作为**早期采用者**帮助塑造这个新市场，我们诚挚邀请您加入我们的社区。

如果您更倾向于采用具有成熟记录的工具，您可以等到 Suika3 进一步成熟后再重新考虑。

---

## 仓库结构

```
include/                           # 公共头文件
src/                               # 引擎源代码
resources/                         # 引擎的资源和素材
  projects/                          # iOS、Android 等的官方项目基础
cmake/                             # CMake 配置文件和预设
docs/                              # 文档源文件（MkDocs）
external/                          # 第三方库和依赖
  PlayfieldEngine/                   # 核心 2D 游戏引擎
    external/                          # Playfield Engine 的子依赖
      NoctLang/                          # 引擎使用的脚本语言
        include/                           # NoctLang 的公共头文件
        src/                               # NoctLang 的源代码
          core/                              # NoctLang 的核心实现
      StratoHAL/                         # 跨平台支持的硬件抽象层
        include/                           # StratoHAL 的公共头文件
        src/                               # StratoHAL 的源代码
```

---

## 资源文件格式

- 图像：
    - 支持格式：PNG、JPEG、WebP。
- 音频：
    - 支持格式：Ogg Vorbis，44100Hz，立体声或单声道。
- 字体：
    - 支持格式：TrueType（TTF）、OpenType（OTF）

---

## 游戏打包与发行

| 操作系统                 | 资源处理                                                                                                                         |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Windows            | 资源应存储在名为 `assets.arc` 的文件中。                                                                         |
| macOS              | 资源应存储在应用包内的 `Contents/Resources/assets.arc` 中。                                            |
| Linux              | 资源应存储在名为 `assets.arc` 的文件中。                                                                         |
| iOS                | 资源应存储在应用包内的 `Contents/Resources/assets.arc` 中。                                            |
| Android            | 资源不得打包。请直接将资源作为普通文件添加到 `app/src/main/assets/` 文件夹中。               |
| HarmonyOS NEXT     | 资源不得打包。请直接将资源作为普通文件添加到 `entry/src/main/resources/rawfiles/` 文件夹中。 |
| WebAssembly (Wasm) | 资源应存储在 `assets.arc` 中，并与 `index.html` 放在同一目录下。                                                   |
| Unity              | 资源不得打包。请直接将资源作为普通文件添加到 `Assets/Resources/StreamingAssets/` 文件夹中。  |

要从游戏资源生成 `assets.arc`，请使用 `suika3-pack` 工具。`suika3-pack` 工具会创建一个混淆过的资源压缩包，引擎可以高效加载。（混淆算法是密钥轮换 XOR，不用于强安全性。它有助于防止随意篡改。混淆密钥可在"key.h"中更改。）

在 Windows、macOS 和 Linux 上，您可以使用 Visual Studio Code 中的预定义任务。

- 点击搜索栏
- 点击 `Run Task`
- 点击 `Suika3: Create a package file`

---

## 引擎功能列表

**2D 游戏支持：**
- 纹理来源：
    - 颜色
    - 图像
    - 字体
- 渲染：
    - 逐像素
    - 缩放
    - 3D 变换
- 音频播放（Vorbis）
- 资源文件访问
- 存档数据访问

**视觉小说开箱即用支持：**
- 消息显示
- 选项选择
- 背景和角色显示/切换
- 声音播放
- 视频播放
- 分层光栅图像动画（移位、缩放、旋转）
- UI/UX 构建
- 存档/读取
- 跳过模式
- 自动模式
- 跳过已读消息
- 消息历史显示和语音重放
- CG 图库
- 本地化
- 模拟参数显示

**未来工作：**
- 2D RPG 地图行走
- 3D 角色模型
- 网络对战

---

## 路线图

- 视觉小说（已完成）
- 其他含剧情部分的 2D 游戏

---

## 截图

<div align="center">
  <img src="https://raw.githubusercontent.com/awemorris/suika3/refs/heads/main/docs/img/screenshot-win11.webp" alt="Suika3 on Windows 11" width="320" hspace="20">
  <p>Windows 11</p><br>
  <img src="https://raw.githubusercontent.com/awemorris/suika3/refs/heads/main/docs/img/screenshot-ios.webp" alt="Suika3 on iOS" width="320" hspace="20">
  <p>iOS</p><br>
  <img src="https://raw.githubusercontent.com/awemorris/suika3/refs/heads/main/docs/img/screenshot-android.webp" alt="Suika3 on Android" width="320" hspace="20">
  <p>Android</p><br>
</div>

---

## 版本策略

`年.月.补丁级别`

| 版本  | 级别                              | 发布日期        | 支持周期     |
|----------|------------------------------------|---------------------|--------------------|
| 26.04    | 功能汇总 / LTS RC1           | 2026 年 4 月          | - 代号"北辰天歸" |
| 26.05    | 功能汇总 / LTS RC2           | 2026 年 5 月            | -                  |
| 26.06    | 功能汇总 / LTS RC3           | 2026 年 6 月           | -                  |
| 26.07    | 长期支持                  | 2026 年 7 月           | 10 年（最低） |
| 26.08    | 功能汇总                     | 2026 年 8 月         | -                  |
| 26.09    | 功能汇总                     | 2026 年 9 月      | -                  |
| 26.10    | 功能汇总                     | 2026 年 10 月      | -                  |
| 26.11    | 功能汇总                     | 2026 年 11 月      | -                  |
| 26.12    | 功能汇总                     | 2026 年 12 月      | -                  |
| 27.01    | 功能汇总                     | 2027 年 1 月        | -                  |
| 27.02    | 功能汇总                     | 2027 年 2 月       | -                  |
| 27.03    | 功能汇总                     | 2027 年 3 月          | -                  |
| 27.04    | 功能汇总 / LTS RC1           | 2027 年 4 月          | -                  |
| 27.05    | 功能汇总 / LTS RC2           | 2027 年 5 月            | -                  |
| 27.06    | 功能汇总 / LTS RC3           | 2027 年 6 月           | -                  |
| 27.07    | 长期支持                  | 2027 年 7 月           | 10 年（最低） |
| 27.08    | 功能汇总                     | 2027 年 8 月         | -                  |
| 27.09    | 功能汇总                     | 2027 年 9 月      | -                  |
| 27.10    | 功能汇总                     | 2027 年 10 月      | -                  |
| 27.11    | 功能汇总                     | 2027 年 11 月      | -                  |
| 27.12    | 功能汇总                     | 2027 年 12 月      | -                  |
| 28.01    | 功能汇总                     | 2028 年 1 月        | -                  |
| 28.02    | 功能汇总                     | 2028 年 2 月       | -                  |
| 28.03    | 功能汇总                     | 2028 年 3 月          | -                  |
| 28.04    | 功能汇总 / LTS RC1           | 2028 年 4 月          | -                  |
| 28.05    | 功能汇总 / LTS RC2           | 2028 年 5 月            | -                  |
| 28.06    | 功能汇总 / LTS RC3           | 2028 年 6 月           | -                  |
| 28.07    | 长期支持                  | 2028 年 7 月           | 10 年（最低） |

---

## 许可证

Suika3 是一款宽松许可的[自由/开源软件](https://www.gnu.org/philosophy/free-sw.en.html)，基于宽松的 `ZLib License` 发布。

* 您可以将 Suika3 用于商业游戏。
* 您无需开源您的游戏代码。
* 您可以修改和重新分发引擎。
* 署名表示感谢，但非必须。

```
Suika3
Copyright (c) 2026 Awe Morris / SCHOLA SUIKAE
```

完整许可证见 [LICENSE](LICENSE) 和 [NOTICE](NOTICE)。

---

## 支持与联系

如有一般咨询、Bug 报告和技术协助：

- **GitHub Issues**：正式 Bug 追踪和功能请求的首选方式。

- **[Discord 服务器](https://discord.gg/YZsq9u9Mgr)**：实时讨论和快速提问的最佳场所。

我们努力提供及时支持，帮助创作者将他们的故事变为现实。

### 专业与企业支持

虽然**社区**通过 GitHub 和 Discord 提供积极支持，但我们理解商业项目通常需要专门支持或有保障的响应时间。

对于需要**正式维护合同、优先 Bug 修复或私人咨询**的工作室和开发者，请直接通过电子邮件联系我们。我们致力于帮助确保您的项目在高风险生产环境中获得成功。

- **联系方式**：Awe Morris <awe@suika3.vn>

**不想签正式合同？没问题。** 如果您是独立开发者或爱好者，更喜欢非正式的方式，只需在 GitHub Issue 或 Discord 上 ping 我们提问。我们总是很乐意交流，并会尽快回复或推送修复！;-)

---

## 社区

### Discord

[Discord 服务器](https://discord.gg/YZsq9u9Mgr)

我们的服务器不容忍任何形式的歧视。这是一个包容的空间，拥抱所有人类差异，包括但不限于种族、性别、技能水平和神经多样性。

### 招募

我们目前正在招募以下领域的贡献者：

* 文档编辑
* 测试软件工程师
* HarmonyOS NEXT 测试者

### 我们对包容性的承诺

我们致力于为每个人提供一个温馨、安全的环境。任何形式的歧视都被严格禁止。

我们的社区热烈欢迎来自各种背景的开发者，包括但不限于：

- **身份与表达：** 种族、民族、国籍、语言、性别认同与表达、性取向和性别特征。

- **个人属性：** 年龄、体型、个人外貌、疾病和神经多样性。

- **生活背景：** 信仰、残障（例如可见度，但不限于此）、经验水平、教育程度和社会经济状况。

- **正义与包容：** 我们明确欢迎有前科的个人，坚信改过自新的力量以及每一位参与者的内在价值。

### 治理

Suika3 提供一个干净的上游代码库，旨在作为下游定制的可靠基础。鼓励用户维护针对自身需求定制的私有分叉。创建您自己的品牌重塑版本是该项目的自然且完全支持的使用方式。

基于这种理念，Suika3 不采用正式的治理结构。相反，项目由其首席维护者与社区用户密切协作来指导。

---

## 贡献

我们欢迎每个人的贡献！无论您是修复 Bug、改进文档还是提出新功能，您的帮助都是推动 **Suika3** 前进的动力。

---

## 传承：伟大的旅程

Suika3 代表了二十余年不懈创新与开发的结晶：

- **Suika Studio（2001–2004）**：我们代码库的起源，以我们第一批基于 GUI 的编辑器为特色。[存档](https://github.com/awemorris/suika-studio-2002)

- **Unfruitiful（2005–2015）**：十年研发专注于为跨平台支持建立健壮的可移植层。

- **Suika2（2016–2024）**：我们当前架构的基石，十年专注研发的成果。提供具有广泛平台兼容性的完整视觉小说体验。多款使用 Suika3 制作的游戏在 App Store 上有售。[存档](https://github.com/awemorris/suika2)

- **Playfield Engine（2025–）**：从 Suika 系列核心可移植层衍生出的多功能 2D 引擎。[仓库](https://github.com/awemorris/PlayfieldEngine)

- **Suika3（2026–）**：通过综合这些传承并引入 `NovelML` 和 `Ray`，Suika3 在提供现代技术灵活性的同时，保留了其前辈的稳定性。

---

## 为何选择 Suika3？：我们的理念

我们不着眼于现有的视觉小说市场。我们的目标是开拓一个尚不存在的移动端视觉小说市场。

有不同目标的创作者也可以在 Ren'Py、Unity 或 Godot 等其他引擎中找到出色的资源。

### 使命：构建可持续生态系统

我们对视觉小说商业成功的专注，是对媒介长期健康的战略回应。我们相信，为了让视觉小说在 2030 年代蓬勃发展，它们必须超越爱好者的边界，重新建立自己作为蓬勃发展的创意产业的地位。

自 2010 年代以来，视觉小说市场面临重大增长挑战。一个关键瓶颈是**缺乏能够在 iOS 和 Android 上提供无缝原生体验的高性能软件引擎**。虽然开发者通常在 PC 上工作，但对大多数人来说，如今主要的个人计算机是智能手机。

没有适用于现代移动平台的可访问、专业级工具，许多创作者被限制在有限的发行渠道中。结果，这一媒介难以触达全球移动端优先的受众，减缓了其整体扩张。

虽然免费和爱好者项目在文化上具有价值且不可或缺，但它们本身可能并不总能维持一个大型创意产业。一个真正健康的生态系统可能需要：

- **商业可行的游戏** — 能够在玩家主要设备上触达他们并产生必要经济活动的作品，让创作者能够建立长期职业生涯。

- **经济独立** — 赋能人才，尤其是亚洲和全球南方的人才，通过讲故事克服经济障碍。

- **活跃的产业** — 将这一媒介从小众兴趣转变为可持续市场，让创造力能够带来自我依存。

在我们看来，商业成功是一种自然的专业期望。

请注意，这一理念并不排斥爱好者或实验性项目。我们只是专注于不同的问题空间：规模上的可持续性。

### 我们的愿景：增长的催化剂

我们的目标不只是提供又一个工具。我们的目标是提供一个**增长的催化剂**。

通过提供一个"随处移植"的引擎，在不增加沉重框架开销的情况下提供原生性能，我们使开发者能够专注于最重要的事情：**讲述经久不衰的故事。**

因为我们热爱视觉小说，我们致力于推动这一媒介向前发展，确保它在未来数十年内仍是一种充满活力且经济上可行的艺术形式。

### 我们的价值观：赋能人才，实现可持续职业

我们的价值在于赋能人才——尤其是亚洲和全球南方的人才——通过讲故事建立可持续的职业生涯。我们相信，有了正确的工具，创造力可以克服经济障碍。

我们对宽松许可证的承诺，是为了那些在 App Store 和 Google Play 上发布和销售原创视觉小说的人们，无论他们的软件、硬件和预算限制如何。

---

## 常见问题

- [这是什么？](#whats-this)
- [这是与 Ren'Py、Unity 或 Godot 等现有引擎的竞争对手吗？](#is-this-a-competitor-to-existing-engines-such-as-renpy-unity-or-godot)
- [现在可以使用吗？](#is-this-okay-to-use-for-now)
- ["超过 25 年的成熟度"与"零运营使用"矛盾吗？](#doesnt-over-25-years-of-maturity-contradict-zero-operational-use)
- [这是单人维护（bus factor 1）吗？](#oh-its-bus-factor-1-isnt-it)
- [公司可以维护自己的分叉吗？](#can-companies-maintain-their-own-forks)
- [谁来做决策？](#who-makes-the-decisions)
- [Suika3 是开源软件吗？可以商用吗？](#is-suika3-open-source-software-can-it-be-used-commercially)
- [第三方库的许可证如何？](#what-about-the-license-for-third-party-libraries)
- [iOS/主机上 JIT 被禁用，该怎么办？](#jit-is-disabled-on-iosconsole-so-what-should-i-do)
- [脚本安全吗？它们可以访问文件或网络吗？](#are-scripts-safe-can-they-access-files-or-the-network)
- [通过商店审核容易吗？](#is-it-easy-to-pass-the-store-review)
- ["支持所有现代平台"是真的吗？](#is-supports-all-modern-platforms-really-true)
- ["通过 Unity"实现主机支持是什么意思？](#what-does-via-unity-mean-for-console-support)
- [HarmonyOS NEXT 的支持程度如何？](#to-what-extent-is-harmonyos-next-supported)
- [能重现"快 2.5-4.5 倍"吗？测量条件是什么？](#can-you-reproduce-25-45x-times-faster-what-are-the-measurement-conditions)
- [旧 GC 需要 10 到 300ms，会导致帧率下降吗？](#old-gc-takes-10-to-300ms-but-does-it-cause-frame-drops)
- [如何开始制作游戏？有示例吗？](#how-do-i-start-making-games-any-samples)
- [如何进行插件开发？](#how-do-i-go-about-developing-plugins)
- [可以从现有资源（如 Ren'Py 或 Unity）迁移吗？](#can-i-migrate-from-existing-assets-like-renpy-or-unity)
- [文档在哪里？是最新版本吗？](#wheres-the-document-is-it-the-latest-version)
- [支持日语/中文/...吗？](#is-japanesechinese-supported)
- [遇到问题该去哪里？](#where-should-i-go-if-im-in-trouble)
- [企业的 SLA 和维护合同如何？](#what-about-slas-and-maintenance-contracts-for-businesses)
- [最低配置要求是什么？](#what-are-the-minimum-requirements)
- ["Supported（已支持）"是什么意思？](#what-does-supported-mean)
- [会有重大变更吗？兼容性策略是什么？](#will-there-be-breaking-changes-what-is-the-compatibility-policy)
- [支持 DLC 或内购吗？](#does-it-support-dlc-or-in-app-purchases)
- [为何如此专注于 Apple 和 iPhone？](#why-the-deep-devotion-to-apple-and-iphone)
- [为何在 iOS 上使用 Python 很有挑战性？](#why-using-python-on-ios-is-challenging)

### 这是什么？

Suika3 是一款面向专业工作室和商业应用开发设计的下一代视觉小说引擎。它以高性能、长期可维护性和通过原生实现（主要以 C 语言）的广泛平台支持为目标。

### 这是与 Ren'Py、Unity 或 Godot 等现有引擎的竞争对手吗？

与其说是竞争对手，不如说我们针对不同的问题领域。Suika3 明确声明其方向为"创建能够经受商业使用考验的以移动端为中心的视觉小说市场"，并将现有引擎视为可行的选择加以尊重。

### 现在可以使用吗？

首个 LTS 版本的稳定化工作进展顺利，质量指标稳步提升。26.05 系列已经足够稳定，可以普遍使用。

虽然当前用户群体较小，给您提供了早期采用或等待进一步成熟的选择，但 GitHub 上的问题通常在一天内得到解决。这确保了所有用户都能获得高水平的社区支持。

### "超过 25 年的成熟度"与"零运营使用"矛盾吗？

Suika3 本身是一个新的集成，但它建立在包括 Suika2 和 StratoHAL 在内的悠久传承之上。换句话说，这是一个"全新包装，古老基础"。

### 这是单人维护（bus factor 1）吗？

策略明确规定"鼓励分叉和品牌重塑"，以及"维护一个没有正式治理的干净上游"，培养一种使下游维护更容易的方法。

### 公司可以维护自己的分叉吗？

同时提供"软件需求规范"（SRS）和"软件设计规范"（SDS），非常适合企业维护。此外，还提供"专业/企业支持"，使必要的知识能够转移给采用方组织。

### 谁来做决策？

首席开发者做决策。我们不为社区维护正式的治理结构。

### Suika3 是开源软件吗？可以商用吗？

Suika3 基于 zlib 许可证发布，按照 FOSS 定义属于开源软件（OSS）。可在商业项目中自由使用。

但是，其定位与 GitHub 上常见的许多项目略有不同。虽然许多 OSS 项目通过构建在大型现有生态系统之上蓬勃发展，但 Suika3 围绕几乎完全从零开始开发的核心组件设计，外部依赖保持在绝对最低限度。

虽然我们对 GNU/Linux 哲学和更广泛的开源社区深怀敬意，但我们的目标始终是提供符合我们自身严格标准的"商业级质量"。由于这种强烈的独立性，Suika3 可能感觉更接近于"作为 OSS 提供的商业软件"，而非典型的社区驱动 OSS 项目。

因此，我们积极欢迎基于本项目构建的闭源分叉和下游商业产品。

### 第三方库的许可证如何？

请参阅 [NOTICE](NOTICE) 了解 Suika3 中使用的第三方库的每个许可证和版权声明的完整文本。

### iOS/主机上 JIT 被禁用，该怎么办？

官方二进制文件在这些环境中使用解释器。虽然我们认为我们的解释器足够快，但如果您需要速度，或者即使解释器对商店审核也有问题，请使用 [AOT](docs/mkdocs-en/aot.md)。这是一个完美的解决方案，速度比解释器快 2.5-4.5 倍。

### 脚本安全吗？它们可以访问文件或网络吗？

不，脚本在沙箱环境中运行，无法访问资源包外部的文件或网络。它只能访问引擎公开的 API，这些 API 被设计为对游戏逻辑安全。

### 通过商店审核容易吗？

我们认为使用 AOT 编译大幅降低了商店审核的门槛，因为它本质上成为一个简单执行标签的原生应用，而不是运行通用脚本。但我们无法保证商店审核的结果，因为审核可能取决于游戏质量，包括图形设计、用户体验和内容。

### "支持所有现代平台"是真的吗？

可以理解您觉得难以置信，但根据我们的检查，一切都正常运行。但是，当您作为产品发布时，请自行负责进行 QA/QC。

### "通过 Unity"实现主机支持是什么意思？

即使我们将 Suika3 移植到主机，由于 NDA，我们也无法公开其源代码。但是，专用版本的 Unity 可用于主机。因此，我们将 Suika3 移植为 Unity 插件。使用此插件可以在 Unity 中运行 Suika3。换句话说，如果您拥有主机版本的 Unity 和"开发套件"机器，您也可以在主机上运行 Suika3。

请理解主机有 UI/UX 要求，因此您需要额外实现它们。

### HarmonyOS NEXT 的支持程度如何？

所有核心开发者都在中国境外，没有在中国销售的实际硬件。因此，功能仅通过模拟器进行了验证。

### 能重现"快 2.5-4.5 倍"吗？测量条件是什么？

这是一个旨在测量性能差异的综合基准测试。

测量代码：
```
func main() {
    var sum = 0;
    for(i in 0..10000) {
        for(j in 0..100000) {
            sum = sum + 1;
        }
    }
}
```

| 机器                 | JIT (s)      | 解释器 (s)       | 倍率（JIT 对比解释器） |
|-------------------------|--------------|-----------------------|------------------------------|
| Intel Core i9 12900H    | 3.32         | 13.2s                 | 4.0x                         |
| Intel Core Ultra 5 228V | 5.78s        | 15.6                  | 2.7x                         |
| Intel Xeon Silver 4114  | 8.08         | 36.4s                 | 4.5x                         |
| Apple M5                | 2.77         | 10.6s                 | 3.8x                         |
| IBM POWER8              | 43.719       | 117.8s                | 2.7x                         |

在真实游戏应用中，性能差异可能因您的逻辑和脚本执行量而有所不同。但是，我们观察到在典型视觉小说场景中，使用 AOT 时性能提升可以非常显著，通常比解释器快约 5 倍。

### 旧 GC 需要 10 到 300ms，会导致帧率下降吗？

旧 GC 很少被调用。图像等大型缓冲区由 C 管理，并得到适当的手动释放。GC 的目标是脚本中的字符串和字典对象，除非发生异常情况，否则不会调用旧 GC。

### 如何开始制作游戏？有示例吗？

请参阅[快速入门指南](docs/mkdocs-en/docs/getting-started.md)，了解使用 Suika3 创建第一个游戏的逐步指导。我们还在本仓库的 `game/` 目录中提供示例游戏，您可以将其用作参考或自己项目的起点。

### 如何进行插件开发？

请参阅[插件开发指南](docs/mkdocs-en/docs/plugin.md)，了解如何为 Suika3 创建插件的详细说明。

### 可以从现有资源（如 Ren'Py 或 Unity）迁移吗？

仅在需要面向移动端且现有引擎使其困难时才考虑迁移。否则，迁移可能不值得付出努力。

图像和音频可以通过批量转换格式进行迁移，但 UI 需要手动移植。场景也需要手动移植，尽管 AI 可能能够实现某种程度的自动化转换。

### 文档在哪里？是最新版本吗？

请参阅[文档](docs/mkdocs-en/docs/index.md)获取最新文档。

### 支持日语/中文/...吗？

游戏符合 Unicode 标准，因此您可以在游戏内容中使用任何不使用 Unicode 合成的语言。引擎本身已国际化，错误消息以本地语言显示。

对于日语和 CJK 游戏，Suika3 支持：
* 禁则字符，包括换行规则
* 注音标注
* 竖排文字

请注意，由于开发团队缺乏相关语言使用者，目前尚未实现从右到左的书写系统。如果您能帮助实现，请联系开发者。

### 遇到问题该去哪里？

请在 GitHub 或 Discord 上提问。如果您不熟悉 GitHub 且不喜欢 Discord，电子邮件也可以 ;-)

### 企业的 SLA 和维护合同如何？

请申请您所需的服务级别。对于仅涵盖 Bug 修复的合同，费用通常约为每月 100 美元。对于包含功能添加的综合合同，每个游戏标题约为 5000 美元。如果您来自新兴国家且无法承担这些费用，请联系我们讨论选择方案。

### 最低配置要求是什么？

请参阅[兼容性列表](#compatibility-list)了解支持平台及其要求的详细信息。

- 官方推荐配置
    - 显示：640x480 24bpp
    - CPU：1GHz
    - RAM：512MB
    - GPU：DirectX 9 / OpenGL 3.0 / OpenGL ES 2.0 / Metal 1.0
    - 磁盘：2MB + 资源文件

- 嵌入式设备最低配置
    - 显示：任意尺寸，需要 24bpp
    - CPU：200MHz
    - RAM：32MB
    - GPU：不需要
    - 磁盘：2MB + 资源文件

### "Supported（已支持）"是什么意思？

这表示示例游戏已通过验证流程，确保其在实际硬件或模拟器上运行。

这仅意味着我们拥有该平台的可用代码库，您需要为自己的游戏进行最终 QA。

### 会有重大变更吗？兼容性策略是什么？

对过去版本的 API 规范不会进行向后破坏性变更。现有 API 函数不会被更改，而是会添加新 API。如果必须更改行为，将提供一个标志来配置行为模式。请注意，存档数据规范在不同版本之间可能不兼容。对于单个产品，请固定并锁定要使用的主要版本号。

### 支持 DLC 或内购吗？

不，不支持，也没有支持计划。

作为替代，请采用基于订阅的发行模式，如 Apple Arcade。在这种模式下，视觉小说成为一部可以长时间阅读的作品——很像一本书——通过持续观看和游玩时间来货币化，类似于 YouTube 视频。

移动端视觉小说市场必须适应这种长尾发行，否则将无法生存。

即使项目得到少数核心粉丝的支持，我建议销售周边商品而不是依赖 DLC。额外内容应作为免费应用更新提供，而不是分割为付费部分；作品应始终保持为一个单一、统一的体验。

目前，这仍是一个前瞻性观点。然而，应用内货币化模式——尤其是类似赌博机制的模式——可能会面临越来越多的监管限制，这取决于地区政策。此类法规可能会扩展并成为更广泛的全球标准。

因此，建立不依赖内购的商业模式不仅是风险缓解策略，也是实现更可持续收入的道路。更重要的是，它使每部作品能够长期保持可用性、可发现性并持续被游玩——使其能够被欣赏和喜爱。

此外，平台持有者是发行的核心，是不可或缺的商业伙伴。在移动端和主机上，有必要不仅基于"您想创造什么"，还要基于"平台方期望什么样的体验"来设计项目。这可能看起来与纯粹的艺术创作不同。然而，作为专业创作者，这是以可持续方式传递您的作品不可或缺的过程。

游戏订阅服务仍是一个新兴和发展中的市场。在这个阶段为其增长做出贡献，创作者将处于与平台持有者建立牢固关系并从增加的曝光度和支持中受益的有利位置。在市场成熟时，早期参与塑造生态系统很可能会得到回报。

这是 Suika3 项目的核心策略。

### 为何如此专注于 Apple 和 iPhone？

Apple 产品可能并非总是最实惠或最普遍可及的。然而，四十余年来，Apple 一直在不断重新定义计算的格局。

我们为支持他们的平台感到自豪，我们的承诺坚定不移——从 iPhone 到 Vision Pro。

### 为何在 iOS 上使用 Python 很有挑战性？

在 App Store 上，Apple 对涉及动态代码执行的"兼容性虚拟机（VM）"实施了事实上的严格限制。这并未在书面指南中明确详述，而是被开发者广泛认可为审核流程的"隐性规则"。一个典型例子是几乎完全没有捆绑 Java 运行时的通用应用。

相比之下，游戏开发中常用的 `Lua` 等语言相对被广泛接受。这是因为 Lua 易于"沙箱化"，使其适合与应用核心功能隔离的受限脚本环境。换句话说，它允许在审核流程后无法任意更改核心操作系统功能和应用基本行为的结构。

然而，`Python` 则是另一回事。它默认缺乏强大的内置沙箱机制，根据设计，脚本可以获得对 iOS 功能的广泛访问权限。从 Apple 的角度来看，这通常被视为允许在审核后进行重大行为更改的"难以控制的 VM"，使其成为经常被拒绝的目标。

您可能会想，"那为什么 App Store 上有 Ren'Py 游戏？"这正是问题的核心。实际上，Apple 的审核流程涉及一定程度的自由裁量。如果一个项目来自主要发行商，或者是 Apple 认为"为整体商店生态系统增加价值"的高质量作品，即使是基于 Python 的也可能通过。

本质上，如果您使用 Ren'Py 挑战商店，您需要达到令人信服的极高质量才能说服审核员。然而，视觉小说是一种高度依赖艺术敏感性的类型；对于一个主要关注技术合规性的审核员来说，要立即传达这种价值并非易事。

这正是 Suika3 的用武之地。

Suika3 采用的设计要么通过 AOT（提前编译）预先将脚本转换为原生代码，要么在严格管理的沙箱 VM 中执行它们。这种方法显著降低了与 App Store 审核流程相关的技术风险。

通过预先消除这些技术障碍，Suika3 使开发者能够仅凭"作品质量"来竞争。
