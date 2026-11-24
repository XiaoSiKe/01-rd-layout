<h1 align="center">📄 零一RD排版</h1>

<p align="center">为 GitHub README 提供一致的首屏排版与交付检查</p>

<p align="center">
  <a href="#安装">安装</a> · <a href="#使用">使用</a> · <a href="#强制调用">强制调用</a>
</p>

> [!IMPORTANT]
> 如果希望每次编写或修改 GitHub 仓库主 README 都先加载本 Skill，请安装后将下方规则加入 Codex 的全局 `AGENTS.md`。仓库级 `AGENTS.md` 可为单个项目设定同样的要求。

## 安装

使用 Node.js 环境中的 `npx` 安装：

```sh
npx -y skills add XiaoSiKe/01-rd-layout -g --all
```

Skill 本身由 Markdown 指令和 Codex 显示配置组成，可以直接交给兼容 Agent Skills 的工具使用。

## 使用

直接说“帮我写这个 GitHub 仓库的 README”，或显式调用 `$01-rd-layout`。新写和整体排版时，应用以下样式：

- 主标题居中，左侧放一个与项目相符的小图标。
- 顶部简介、标语、徽章与导航按需居中排列，正文左对齐。
- 使用前提或必读信息用 GitHub 原生的紫色 Important 提示块。

只读任务和内部目录索引无需调用。局部修改遵守用户指定的修改范围。

## 强制调用

将以下内容加入 `~/.codex/AGENTS.md`。如果使用了 `AGENTS.override.md`，加入实际生效的文件。

```markdown
## GitHub README 排版

每次产出或修改用于 GitHub 展示的仓库主 README.md，必须在起草或改动前加载
零一RD排版（$01-rd-layout），即使用户未点名。若未自动加载，直接读取已安装的
01-rd-layout/SKILL.md。按该 Skill 核对交付结果，局部修改遵守用户指定范围。
```

查看 [Skill 指令](skills/01-rd-layout/SKILL.md)。
