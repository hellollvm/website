# HelloLLVM 社区网站（Hugo）

该仓库为 Hugo 静态站点，采用明暗双主题的活泼设计，**中英双语**（默认中文，可切换英文）。

- 中文站：`https://hellollvm.org/`
- English: `https://hellollvm.org/en/`

## 本地预览

```bash
hugo server
```

切换英文：访问 `http://localhost:1313/en/`，或点击右上角 `EN` / `中文` 按钮。

## 目录说明

- `content/zh/`、`content/en/`: 中英两套内容（路径一一对应，Hugo 自动互链翻译）
  - `posts/`: 博客文章
  - `meetups/`: Meetup / 大会详情页
  - `announcements/`: 社区公告
  - `archives.md`: 历史活动存档
- `layouts/`: 页面模板（首页、列表、文章、页头页脚）
- `i18n/zh.yaml`、`i18n/en.yaml`: 界面文案翻译
- `assets/css/main.css`: 站点样式（明暗双主题，含亮色渐变点缀）
- `.github/workflows/hugo-ci.yml` / `hugo-deploy.yml`: Hugo 构建 CI 与 GitHub Pages 部署

## 内容 front matter 约定

活动类文章可在 front matter 中补充信息，首页「近期活动」卡片会展示：

```yaml
city: "深圳"                # 城市
format: "线下 + Zoom"       # 活动形式
venue: "深圳虚拟大学园 A301" # 地点（可选）
time_label: "2023-04-22（周六）14:30–17:30"
links:                      # 相关链接（可选）
  - name: "报名参会"
    url: "https://example.com"
summary: "卡片摘要（可选，缺省取正文开头）"
```

新增内容时请**同时提供中英两个版本**（`content/zh/...` 与 `content/en/...`，文件名保持一致）。
