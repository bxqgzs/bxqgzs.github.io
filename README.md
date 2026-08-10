# 白小谦工作室唯一官网

> 版本：v2.0.0  
> 线上地址：https://qians.netlify.app

白小谦工作室官网，专注于极简设计与用户体验，出品 Qian影视、Qian音乐、Qian云盘、SBTI测试等免费、简洁、实用的互联网工具。

## 技术栈

- 单 HTML 零构建（`index.html`）
- Tailwind CSS（CDN JIT）+ GSAP 动画 + Font Awesome 图标
- 苹果官网设计风格：大留白、大字、细腻 scroll reveal 动效
- 尊重 `prefers-reduced-motion`，无 JS 时内容仍可见

## 本地预览

```bash
python -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 一键部署到 Netlify

点击下方按钮， fork 仓库后即可一键部署：

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/bxqgzs/bxqgzs.github.io)

> 将上方 URL 中的仓库地址替换为你的实际 GitHub 仓库地址。

部署说明：
- 构建命令：无（纯静态）
- 发布目录：`.`（根目录）
- 配置文件：`netlify.toml`（已含安全头与缓存策略）

## 必应（Bing）收录指南

本项目已内置必应收录所需文件：

| 文件 | 作用 |
|------|------|
| `robots.txt` | 允许所有爬虫（含 bingbot），指向 sitemap |
| `sitemap.xml` | 站点地图，提交给必应 |
| `BingSiteAuth.xml` | 必应站点验证占位文件 |
| `index.html` 内 meta | description / keywords / Open Graph / canonical |
| JSON-LD | Organization / WebSite / BreadcrumbList 结构化数据 |

### 验证步骤

1. 部署上线后，访问 [Bing Webmaster Tools](https://www.bing.com/webmasters/)。
2. 添加站点 `https://qians.netlify.app/`。
3. 选择「文件验证」方式，获取专属验证码。
4. 编辑 `BingSiteAuth.xml`，将 `YOUR_BING_CODE` 替换为你的验证码。
5. 重新部署，在 Bing Webmaster Tools 点击验证。
6. 提交 `sitemap.xml`（`https://qians.netlify.app/sitemap.xml`）。

## 项目结构

```
├── index.html              # 主页面
├── 404.html                # 404 页
├── robots.txt              # 爬虫规则
├── sitemap.xml             # 站点地图
├── BingSiteAuth.xml        # 必应验证
├── humans.txt              # 人类信息
├── manifest.webmanifest    # PWA 清单
├── netlify.toml            # Netlify 配置
├── favicon.svg             # 矢量图标
├── apple-touch-icon.png    # iOS 图标
├── og-image.png            # 社交分享图
└── *.png                   # 作品图
```

© 白小谦工作室. 保留所有权利.
