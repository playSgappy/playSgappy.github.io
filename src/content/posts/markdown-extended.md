---
title: Markdown 扩展功能
published: 2024-05-01
updated: 2024-11-29
description: 了解有关 Fuwari 中 Markdown 功能的更多信息
image: ""
tags:
  - Example
category: Examples
draft: false
---

## GitHub 仓库卡片
您可以添加链接到 GitHub 存储库的动态卡片，在页面加载时，存储库信息将从 GitHub API 中提取。

::github{repo="Fabrizz/MMM-OnSpotify"}

使用代码创建 GitHub 存储库卡 `::github{repo="<owner>/<repo>"}`.

```markdown
::github{repo="saicaca/fuwari"}
```

## 警告

支持以下类型的警告：`note` `tip` `important` `warning` `caution`

:::note
突出显示用户应该考虑的信息，即使浏览时也是如此。
:::

:::tip
帮助用户取得更大成功的可选信息。
:::

:::important
用户成功所必需的关键信息。
:::

:::warning
由于存在潜在风险，需要用户立即关注的关键内容。
:::

:::caution
某个行为可能造成的负面后果。
:::

### 基本语法

```markdown
:::note
Highlights information that users should take into account, even when skimming.
:::

:::tip
Optional information to help a user be more successful.
:::
```

### 自定义标题

警告的标题可以自定义。

:::note[我的自定义标题]
这是一条带有自定义标题的注释。
:::

```markdown
:::note[MY CUSTOM TITLE]
This is a note with a custom title.
:::
```

### GitHub 语法

> [!TIP]
> [The GitHub syntax](https://github.com/orgs/community/discussions/16925) 也受支持。

```
> [!NOTE]
> The GitHub syntax is also supported.

> [!TIP]
> The GitHub syntax is also supported.
```