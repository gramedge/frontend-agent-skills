# Frontend Agent Skills

面向前端项目的可复用 Agent Skills。仓库中的每个 Skill 都位于 `skills/<skill-name>/` 目录，可单独安装。

## Skills

### `prototype-to-page`

根据 Figma 设计稿、产品原型图或页面截图，在现有 Vue 3 + TypeScript、Element Plus 项目中实现页面。默认优先保证结构、功能和可维护性，不追求像素级复刻。

## 安装

将 `<owner>/<repo>` 替换为上传后的 GitHub 仓库地址。

先查看仓库中可安装的 Skills：

```bash
npx skills add <owner>/<repo> --list
```

安装 `prototype-to-page`：

```bash
npx skills add <owner>/<repo> --skill prototype-to-page
```

只安装到 Codex：

```bash
npx skills add <owner>/<repo> --skill prototype-to-page --agent codex
```

默认安装到当前项目。需要全局安装时增加 `--global`：

```bash
npx skills add <owner>/<repo> --skill prototype-to-page --agent codex --global
```

## 仓库结构

```text
frontend-agent-skills/
├── README.md
└── skills/
    └── prototype-to-page/
        └── SKILL.md
```

新增 Skill 时，创建 `skills/<skill-name>/SKILL.md`，并在文件开头提供合法的 YAML frontmatter：

```yaml
---
name: skill-name
description: 说明该 Skill 的用途及应在什么情况下使用。
---
```
