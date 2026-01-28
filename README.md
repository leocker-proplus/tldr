<!-- markdownlint-disable MD041 -->

<div align="center">
  <h1><a href="https://tldr.sh/"><img alt="tldr-pages" src="images/banner.png" width=600/></a></h1>

[![Build status][github-actions-image]][github-actions-url]
[![Matrix chat][matrix-image]][matrix-url]
[![Merged PRs][prs-merged-image]][prs-merged-url]
[![GitHub contributors][contributors-image]][contributors-url]
[![license][license-image]][license-url]
[![Mastodon][mastodon-image]][mastodon-url]

[github-actions-url]: https://github.com/tldr-pages/tldr/actions
[github-actions-image]: https://img.shields.io/github/actions/workflow/status/tldr-pages/tldr/ci.yml?branch=main&label=Build
[matrix-url]: https://matrix.to/#/#tldr-pages:matrix.org
[matrix-image]: https://img.shields.io/matrix/tldr-pages:matrix.org?label=Chat+on+Matrix
[prs-merged-url]: https://github.com/tldr-pages/tldr/pulls?q=is:pr+is:merged
[prs-merged-image]: https://img.shields.io/github/issues-pr-closed-raw/tldr-pages/tldr.svg?label=Merged+PRs&color=green
[contributors-url]: https://github.com/tldr-pages/tldr/graphs/contributors
[contributors-image]: https://img.shields.io/github/contributors-anon/tldr-pages/tldr.svg?label=Contributors
[license-url]: https://github.com/tldr-pages/tldr/blob/main/LICENSE.md
[license-image]: https://img.shields.io/badge/license-CC_BY_4.0-blue.svg?label=License
[mastodon-url]: https://fosstodon.org/@tldr_pages
[mastodon-image]: https://img.shields.io/badge/Mastodon-6364FF?logo=mastodon&logoColor=fff
</div>

## 什么是 tldr-pages？

**tldr-pages** 项目是一个由社区维护的命令行工具帮助文档合集，旨在成为传统[手册页](https://en.wikipedia.org/wiki/Man_page)更简洁、更易上手的补充资料。

你或许是命令行新手，或许只是有些生疏，总是记不住 `lsof`、`tar` 这类命令的参数？

过去，`man tar` 里第一个解释的参数更是让人摸不着头脑：

$ man tar
...
-b blocksize

指定块大小，单位为512字节的记录，用于磁带驱动器的输入输出。
一般情况下，只有读写磁带驱动器时才需要该参数，即便如此也很少用到，因为默认的20个记录块大小（10240字节）已经非常通用。
...
显然，我们需要更简洁、聚焦实际使用场景的帮助文档。比如这样：

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/tldr-pages/tldr/blob/main/images/tldr-dark.png">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/tldr-pages/tldr/blob/main/images/tldr-light.png">
    <img alt="tldr 客户端展示 tar 命令的截图" src="https://github.com/tldr-pages/tldr/blob/main/images/tldr-dark.png">
</picture>

本仓库正是为此而生：这是一个持续更新的合集，收录了 UNIX、Linux、macOS、FreeBSD、NetBSD、OpenBSD、SunOS、Android、Windows、Cisco IOS 和 DOS 系统中，最常用命令行工具的使用示例。

如何使用？
[!TIP]
无需在电脑上安装客户端，也可通过网页版查看：https://tldr.inbrowser.app（支持 PWA 离线使用）。
在本地使用最便捷的方式，是安装官方的Python 客户端，可通过 pipx 从 PyPI 安装（也可使用其他包管理器）：
pipx install tldr
Linux 和 Mac 用户也可通过 Homebrew 安装官方Rust 客户端（其他系统可使用对应包管理器）：
brew install tlrc
Windows 用户可通过 Winget 安装官方Rust 客户端（其他系统可使用对应包管理器）：
winget install tldr-pages.tlrc
你也可以使用官方的Node.js 客户端（注：该客户端更新进度相对滞后）：
npm install -g tldr
安装完成后，你就可以直接查看简洁易懂的命令帮助，例如查看 tar 命令，只需输入 tldr tar，替代传统的 man tar。

如果不想安装任何软件，可直接查看PDF 版本。
[!NOTE]
大多数语言的翻译版 PDF 均可在最新发布的附件中找到。
社区还提供了多款第三方客户端，支持命令行和其他平台，完整的客户端列表可查看项目维基百科。

如何参与贡献？

我们欢迎任何形式的贡献！

贡献方式包括：

• 补充尚未收录的常用命令文档

• 为现有文档新增示例或优化内容

• 完成标注需要帮助标签的待办任务

• 将文档翻译为其他语言

所有 tldr 文档均采用 Markdown 编写，可轻松编辑，你可以通过 Git 命令行或 GitHub 网页界面提交 PR。

我们致力于打造友好协作的社区氛围。如果是首次贡献，建议先阅读贡献指南，放心提交你的修改即可！

如果想参与翻译工作，可访问 https://lukwebsforge.github.io/tldri18n/ 查看各语言翻译进度，以及待翻译/需更新的内容。

也欢迎加入我们的Matrix 交流群！

同类项目

• cheat.sh
整合多个来源的速查手册（包括 tldr-pages），提供统一的查询界面。

• devhints
不仅涵盖命令行，还包含大量编程相关的速查手册，内容十分丰富。

• eg
在命令行展示带详细解释的使用示例，支持自定义示例与默认示例一同展示。

• kb
极简的命令行知识库管理工具，可简洁有序地管理笔记和速查手册，支持非文本文件。

• navi
交互式速查工具，可实时浏览示例或快速补全命令。

• Cheat
支持在命令行创建和查看交互式速查手册，专为那些常用但又记不清参数的命令设计。

• Command Line Interface Pages
可编写标准化的 CLI、目录和配置文件帮助文档。

• bropages (已废弃)
手册页的优质补充工具，展示简洁的命令通用示例，示例由社区提交并支持投票，优质内容会优先展示。

"tldr" 是什么意思？

TL;DR 是 Too Long; Didn't Read 的缩写，起源于网络俚语，用于表示因文本过长而跳过未读。
更多介绍可查看 How-To Geek 的文章。

项目声明

1. 本文档为 tldr-pages/tldr 简体中文翻译版，遵循原项目 CC BY 4.0 开源协议。

2. 翻译严格保留原文档格式、代码块及链接，仅对文字内容进行本地化处理。

3. 原项目地址：https://github.com/tldr-pages/tldr

4. 开源协议：https://github.com/tldr-pages/tldr/blob/main/LICENSE.md
