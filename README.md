# Daily Insight

> 朝朝如是，且谙今日。

Stout 的个人博客源码。基于 [Astro](https://astro.build/) 构建，主题改造自 [Retypeset](https://github.com/radishzz/Retypeset)（原 fork 自 [CassiopeiaCode/blog](https://github.com/CassiopeiaCode/blog)）。

线上地址：<https://stout-xiao.github.io>

## 本地开发

需要 Node 20+ 和 [pnpm](https://pnpm.io/) 10.x。

```bash
pnpm install
pnpm dev          # 本地开发，默认 http://localhost:4321
pnpm build        # 生产构建到 ./dist
pnpm preview      # 本地预览构建产物
pnpm new-post     # 交互式创建新文章
```

## 写文章

文章放在 `src/content/posts/`，frontmatter 见 `src/content.config.ts`：

```yaml
---
title: 文章标题
published: 2026-05-11
description: 简介，可选
tags: [tag1, tag2]
draft: false
---
```

英文版本放 `src/content/posts/en/` 下，文件名与中文版相同。

## 部署

推到 `main` 分支后，GitHub Actions 会自动构建并发布到 GitHub Pages。
首次部署前需要在仓库 **Settings → Pages → Source** 选择 `GitHub Actions`。

## 主要配置

`src/config.ts` 集中管理站点信息、配色、评论、SEO 等。改完会热重载。

## 致谢

主题来自 [Retypeset](https://github.com/radishzz/Retypeset)，作者 radishzz。
