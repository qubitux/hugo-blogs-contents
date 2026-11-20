# 项目简介
这是一个基于Hugo构建的静态博客内容目录
# 文件写入规范
- 除了内容目录和文件，其他配置文件都需要为每个配置项写详情的注释，解释这个字段是做什么的、有什么作用、设置和不设置有什么效果
# 内容组织
- 内容按「语言 → 领域 → 知识点」三级存放：`content/<语言>/<领域>/<知识点>.md`（语言目录为 `zh-cn`、`en`），与笔记仓库（voidHalcon-notes）的 `<语言>/<领域>/` 目录一一对应；org 里的 `#+hugo_section: <语言>/<领域>` 导出后即落在这里。
- 领域目录是 Hugo 的一级 section，需要一个 `_index.md`（标题与简介）；`/domains/` 知识库页由主题的 `layouts/section/domains.html` 自动列出所有有文章的领域，新增领域不用改配置。
- `posts`、`notes`、`logs`、`about`、`domains` 是站点功能栏目，不算领域（见 `hugo.yaml` 的 `params.domains.exclude`）。
