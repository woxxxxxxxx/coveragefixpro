# CoverageFixPro

## 基础信息
- 域名：coveragefixpro.com
- 主色：#1d4ed8（蓝）
- GA ID：G-5XX4CE3YBR
- 工具/内容数量：120 保险计算器 + 11篇博客
- 部署方式：**Hostinger FTP**（node deploy-ftp.js）⚠️ 不是GitHub Pages
- Git仓库：github.com/woxxxxxxxx/coveragefixpro（仅做版本控制，不部署）

## 当前进度
- AdSense 状态：准备就绪，可提交审核 [2026-06-21]
- 上次审计完成：2026-06-21
- 通过概率评估：90%+
- 本轮完成事项 [2026-06-21]：
  - 删除"no ads/no tracking"红线文案
  - About页面去模板化
  - 120个工具页添加 How to Use + Use Cases 模块
  - 创建 blog/ 目录 + 11篇保险博客文章
  - 导航添加 Blog 链接
  - 修复模板 meta descriptions（25页补充唯一描述）
  - CSS tool-modules.css 511行专业样式
  - 120个tool-card添加分类emoji图标
  - 修复130+ HTML文件 StructuredData 路径泄露（C:/Users...）
  - sitemap.xml 路径修复
- 下一步：提交 AdSense 审核

## 专属配置
- FTP：212.85.28.149 / u868313694.coveragefixpro.com / Xxh113324~ / public_html
- 部署命令：`node deploy-ftp.js`（必须运行才能更新线上！）
- Git push 仅备份代码，**不会触发线上更新**

## ⚠️ 重要教训
- **CoverageFixPro 用 Hostinger FTP 部署，不是 GitHub Pages**
- 之前误以为是 GitHub Pages，4次 git push 后线上一直不更新，浪费1小时排查 BTT 按钮问题
- 任何代码改动后必须执行 `node deploy-ftp.js` 才能上线
- 排查"线上没生效"问题第一步：用 curl 验证线上实际内容

## 关键修复历史
- [2026-06-20] 首页emoji乱码 → 恢复120个工具卡片图标
- [2026-06-20] deploy-ftp.js 排除列表 → 清理开发文件
- [2026-06-21] "no ads/no tracking" → 删除（AdSense红线）
- [2026-06-21] About页模板化 → 定制化内容
- [2026-06-21] 工具页无教程内容 → 添加 How to Use + Use Cases
- [2026-06-21] 无博客 → 创建11篇文章
- [2026-06-21] 25页缺meta description → 补充唯一描述
- [2026-06-21] StructuredData URL含本地路径 → 修复为正确URL
- [2026-06-21] tool-card无图标 → 添加120个分类emoji
- [2026-06-21] 首页 BTT 按钮点击无反应 → 完全重写为 JS动态创建按钮 + inline style + 直接赋值 scrollTop（旧实现缺 click handler，且依赖CSS .show 类）
- [2026-06-21] **部署方式认知错误** → 之前误以为 GitHub Pages，实际是 Hostinger FTP；必须运行 `node deploy-ftp.js`

## 待办
- [ ] 提交 AdSense 审核
- [ ] 继续扩充博客内容


## 2026-06-28 AdSense ????
- Blog ??/??? 16 ????????????? sitemap.xml?
- ??????????/?????????


## 2026-07-01 search-click acceleration
- Added 3 search-intent guide hub pages based on recent Search Console exposure.
- Updated title/meta descriptions for high-impression, low-CTR pages and added a homepage entry block for the new guides.
- Regenerated sitemap.xml with lastmod=2026-07-01. Goal: improve long-tail relevance, internal link strength, and search-result click clarity.

## 2026-07-11 AdSense low-value remediation
- The earlier content lift still left 16 insurance articles around 210-240 words and several 240-word search guides. Eight core articles were rebuilt to 621-647 words with claim/base scenarios, verification cards, decision records, limitations, and NAIC/HealthCare.gov/FEMA sources.
- Twelve thin articles/guides are noindex, excluded from the sitemap, and contain no AdSense loader. Added editorial-policy.html; the sitemap now contains 139 indexable pages.
- Treat YMYL claims conservatively: calculators are planning aids, not quotes or coverage determinations. Wait for recrawl before resubmitting.
