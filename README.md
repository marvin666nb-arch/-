# 程序员在线工具箱

这是一个纯静态版程序员在线工具箱网站，包含 35 个常用在线工具，适合部署到 GitHub Pages、Netlify、Cloudflare Pages 等静态托管平台。

当前版本已取消登录、付费、会员和次数限制。所有工具打开即可使用，TXT、CSV、Excel、Word、PDF、ZIP 等导出功能可直接点击下载。

## 下载链接

用户在 GitHub README 页面点击下面的蓝色文字，会直接下载当前仓库的完整源码 ZIP 文件，不需要改用户名，不需要改仓库名：

[点击自动下载源码 ZIP](archive/refs/heads/main.zip)

如果已经开启 GitHub Pages，网站访问地址通常是：

[点击访问在线网站](https://你的GitHub用户名.github.io/仓库名/)

## 功能分类

- 文本处理：文本去重、文本分割、文本合并、批量替换、HTML 转纯文本、段落排版、文本脱敏、字数统计等。
- 数据格式转换：JSON 转 CSV/Excel、CSV 清洗、Markdown 转 Word/PDF、JSON 格式化、XML 转 JSON、JsonSchema 生成等。
- 代码开发工具：正则表达式生成、自然语言生成 MySQL、代码删除注释与压缩、接口测试、SQL Insert 生成、爬虫规则生成等。
- 批量文件处理：批量文件名修改、二维码批量生成、TXT 文档分割、ZIP 打包导出等。
- 信息提取工具：手机号、邮箱、网址、身份证、微信号、QQ 号等字段提取。
- 加密换算工具：Base64、URL 编码、MD5/SHA1/SHA256、时间戳、ASCII、颜色换算、金额大写转换等。

## 本地运行

解压本项目后，进入项目目录，推荐使用本地静态服务运行：

```bash
python -m http.server 4173
```

然后在浏览器打开：

```text
http://localhost:4173/
```

也可以直接打开 `index.html` 查看首页，但部分浏览器会限制本地文件路径下的 iframe、下载或资源加载，所以更推荐使用本地静态服务。

## GitHub Pages 部署

1. 新建一个 GitHub 仓库。
2. 把本目录内的所有文件上传到仓库根目录，包括 `index.html`、`core.html`、`tools`、`assets`、`.nojekyll` 等。
3. 打开仓库的 `Settings`。
4. 进入 `Pages`。
5. 在 `Build and deployment` 中选择 `Deploy from a branch`。
6. Branch 选择 `main`，Folder 选择 `/root`。
7. 保存后等待 GitHub 自动部署。

部署完成后，GitHub 会生成访问地址，格式通常是：

```text
https://你的GitHub用户名.github.io/仓库名/
```

## 文件说明

- `index.html`：网站首页，包含 6 大分类和 35 个工具入口。
- `core.html`：万能处理器主页面，内置全部工具处理逻辑。
- `core/index.html`：兼容 `/core/` 路径访问。
- `tools/`：35 个独立 SEO 静态工具页面。
- `assets/`：静态资源文件。
- `member.html`：免费使用说明页面。
- `sitemap.xml`：搜索引擎站点地图。
- `robots.txt`：搜索引擎抓取规则。
- `.nojekyll`：GitHub Pages 静态部署标记文件。
- `404.html`：静态站兜底页面。

## 使用方法

1. 打开首页 `index.html` 或访问部署后的首页地址。
2. 点击任意工具卡片进入对应工具页面。
3. 也可以直接打开 `core.html`，在左侧菜单切换 35 个工具。
4. 在左侧输入框粘贴内容，或拖拽上传文本文件。
5. 点击“执行转换”查看右侧结果。
6. 点击“复制文本”复制结果。
7. 点击“导出 TXT / CSV / Excel / Word / PDF / ZIP”下载结果文件。

## 注意事项

- 本项目是纯静态网页，不需要 Node.js 后端、数据库或 Supabase。
- 大部分处理逻辑都在浏览器本地执行，数据不会上传到服务器。
- 二维码生成和 ZIP 打包使用浏览器端脚本，如果部署环境不能访问 CDN，建议把相关库下载后改成本地引用。
- 接口在线测试工具受浏览器跨域规则影响，目标接口需要允许跨域访问才能正常返回数据。
