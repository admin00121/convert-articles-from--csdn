================================================================
 CSDN 文章转 Word ——  GitHub 仓库说明文档
================================================================

【使用说明】
1. 把本文件重命名为 README.md，再上传到 GitHub 仓库根目录。
2. 把文中所有 <尖括号> 占位符替换成你自己的信息：
     <你的GitHub用户名>    例如 zhangsan
     <仓库名>              例如 csdn-to-word
     <你的邮箱>            可选，用于接收反馈
3. 上传前请把 G:\csdn 里的 exe 一起放到仓库的 Release 里（见第六节）。

本文件用 Markdown 语法书写，GitHub 会自动渲染。

================================================================


# CSDN 文章转 Word 📄

> 把 CSDN 博客文章一键抓下来，排成**可以直接打印**的 Word 文档（.docx）。
> 单文件绿色程序，100 KB，无需 Python、无需 Office、双击即用。

---

## ⭐ 使用前请先给个 Star

**本项目免费使用，但请你先做一件事：**

> ### 👉 给本仓库点一个 ⭐ Star，再下载使用。

- 点 Star 的位置：页面右上角的 **Star** 按钮
- 仓库地址：https://github.com/<你的GitHub用户名>/<仓库名>
- 一个 Star 不花你任何钱，但能让作者知道这个工具真的有人在用，也是持续维护的动力

**为什么要有这个要求？**
纯个人项目，没有广告、没有会员、没有内购。唯一的"回报"就是知道你用得顺手。
如果你觉得它省了你的时间，请点一下 Star；如果你不打算点，也请至少把这个仓库分享给需要的人。

> 说明：GitHub 无法用技术手段强制验证 Star，这是一条**君子协定**。
> 你可以直接下载使用，但还是希望你能顺手点一下 ⭐。

---

## ✨ 它能做什么

CSDN 的文章直接打印会很难看：侧边栏、广告、推荐位、浮动按钮全都在，正文被挤成窄窄一条。
这个小工具把文章"洗"成一篇干净的 Word 文档，按 A4 纸排版，直接 Ctrl+P 就能打成纸质资料。

**核心能力**

| 功能 | 说明 |
| --- | --- |
| 单篇转换 | 填一个文章网址，点「确认转换」，几秒出结果 |
| 批量转换 | 网址框支持多行，每行一个，连续处理 |
| 整站搬运 | 直接填**博主主页**地址，自动枚举该博主全部文章（可限篇数） |
| 图片嵌入 | 自动下载文中配图并嵌入 Word，按版心等比缩放 |
| 代码块保留 | 等宽字体 + 灰底 + 逐行保留缩进，代码不再糊成一片 |
| 表格还原 | 真实 Word 表格，带边框，表头跨页自动重复 |
| 目录友好 | 标题带大纲级别，Word 里一键生成目录、导航窗格可跳转 |
| 页码 | 页脚居中「第 X 页 / 共 Y 页」 |
| 直接打印 | 界面里有「直接打印」按钮，调系统打印动作 |
| 来源标注 | 可选保留作者、发布时间、原文链接 |

---

## 🖥 运行环境

**最基本的要求：一台 Windows 电脑 + .NET Framework 4.7.2 以上。**

| 项目 | 要求 | 说明 |
| --- | --- | --- |
| 操作系统 | Windows 7 SP1 / 8.1 / 10 / 11 | 32 位、64 位都可以 |
| .NET Framework | **4.7.2 或更高** | Win10 1803 起、Win11 全部自带；Win7 / Win8.1 需装一次 |
| Python / Java / Node | ❌ 不需要 | 已编译成原生 exe |
| Office / WPS | ❌ 不需要 | 程序自己生成 .docx，不调用 Word |
| 管理员权限 | ❌ 不需要 | 不写注册表、不装服务、不设开机启动 |
| VC++ 运行库 | ❌ 不需要 | 纯 .NET 程序 |

**怎么查自己的 .NET 版本**

`Win + R` → 输入 `regedit` → 定位到

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full
```

看 `Release` 的值：

| Release 值 | 版本 | 能否运行 |
| --- | --- | --- |
| ≥ 461808 | 4.7.2 | ✅ |
| ≥ 528040 | 4.8 | ✅ |
| ≥ 533320 | 4.8.1 | ✅ |
| < 461808 | 更低版本 | ❌ 需先安装 |

低于 461808 的话，去微软官网搜索「.NET Framework 4.8 运行时」下载安装即可（免费，约 60 MB）。

---

## 🚀 快速开始

1. 到本仓库的 **Releases** 页面下载 `CSDN文章转Word_v1.2.exe`
2. 把它和同名的 `CSDN文章转Word_v1.2.exe.config` **放在同一个文件夹**（两个文件都要，别只拷 exe）
3. 双击 exe
4. 在「文章网址」框粘贴 CSDN 文章地址，例如：

   ```
   https://blog.csdn.net/qq_44715943/article/details/116714584
   ```

5. 需要的话改一下「保存位置」
6. 点 **「确认转换」**
7. 完成后点「打开刚生成的文档」，或直接点「直接打印」

默认输出目录：exe 同目录下的 `输出文档` 文件夹。

---

## 📖 界面与选项

| 控件 | 作用 |
| --- | --- |
| 文章网址 | 支持多行；可省略 `https://` 自动补全；也可填博主主页 |
| 保存位置 | 输出目录，可点「浏览…」选择 |
| 下载并嵌入文中图片 | 勾选后下载配图嵌入 Word；不勾选只出文字，速度更快 |
| 保留作者 / 时间 / 原文链接 | 在文档顶部生成一行来源信息 |
| 博主主页最多抓 __ 篇 | 对博主主页生效，防止误抓上千篇（默认 20） |
| 确认转换 | 开始任务，处理中自动禁用防重复点击 |
| 打开刚生成的文档 | 用默认程序打开最近生成的 docx |
| 直接打印 | 调系统 print 动作直接送打印机 |
| 打开输出文件夹 | 在资源管理器中定位输出目录 |

### 批量抓某个博主的全部文章

网址框里直接填主页地址：

```
https://blog.csdn.net/qq_44715943
```

程序会翻页枚举该博主的文章列表并逐篇转换，篇数由「博主主页最多抓 __ 篇」控制。

---

## 📑 生成的文档长什么样

按打印需求排版，不是网页截图：

- **A4 纸**，四边 25 mm 页边距
- 正文：宋体 / Times New Roman，五号（10.5 pt），**1.5 倍行距**，首行缩进 2 字符，两端对齐
- 标题：微软雅黑加粗，一级 16 pt、二级 14 pt，带大纲级别
- 代码块：Consolas 等宽字体、浅灰底纹、左侧竖线、逐行保留缩进
- 表格：带边框、表头浅蓝底纹、跨页自动重复表头
- 图片：按版心宽度（160 mm）等比缩放并居中，过高的图自动限高
- 页脚：居中「第 X 页 / 共 Y 页」
- 付费 / 登录受限的文章，文末加一行红色提示

> 建议先打开仓库里的 `效果样张-你的测试文章.docx` 看一眼实际效果。

---

## ⌨️ 命令行用法（可选）

除了图形界面，也支持命令行，方便做批处理或自动化：

```bat
:: 转换单篇
CSDN文章转Word_v1.2.exe --cli "https://blog.csdn.net/xxx/article/details/123" "D:\输出目录"

:: 从本地已保存的 HTML 转换（离线，不联网）
CSDN文章转Word_v1.2.exe --from-html "page.html" "https://blog.csdn.net/xxx/article/details/123" "out.docx"
```

开发自测用的隐藏参数：`--gui-test`、`--screenshot`、`--selftest-image`。

---

## ❓ 常见问题

**Q1. 提示「无法连接到远程服务器 / 基础连接已经关闭」**
网络不通，或被安全软件拦截。先用浏览器确认能正常打开那篇文章。

**Q2. 提示「没有找到正文区域」**
网址不是文章详情页，或被 CSDN 反爬拦截。正确形式：
`blog.csdn.net/用户名/article/details/数字`

**Q3. 提示「疑似付费专栏 / 需登录查看全文」**
该文章要订阅或登录才能看全文，程序只能拿到公开部分，文末会有红色提示。
这是 CSDN 的访问限制，不是程序 bug。

**Q4. 生成的文档里没有图片**
图片需要访问 `i-blog.csdnimg.cn`。若该域名被墙或被公司网络拦截，图片会跳过，
文字部分不受影响。日志里会逐条打印「图片跳过」。

**Q5. 处理到一半卡住 / 没反应**
看界面下方的日志框；如果程序崩溃，exe 同目录会写 `CSDN2Word.log`，
里面有完整堆栈，可以提 Issue 时附上。

**Q6. 提示「Word 无法完成操作」**
如果连别的软件生成的标准 docx 也打不开，那是本机 Office 环境问题
（常见于受限账户或损坏的 Normal.dotm），与本程序产出的文档无关。
可试 Word 的「打开并修复」。

**Q7. 杀毒软件报警**
程序是自行编译的 .NET 程序，未做数字签名。部分杀软会对"新出现的未知 exe"
启发式报警。可加入信任，或用仓库里的源码自行编译。

**Q8. 想改字号 / 行距 / 页边距**
参数集中在 `src/Wml.cs` 顶部（页边距、版心尺寸）与 `src/DocxWriter.cs` 的
`BuiltInStyles()`（正文字号、行距、标题字号），改完重新编译即可。

---

## 🔧 从源码编译

需要 .NET SDK（8.0 及以上均可）：

```bat
dotnet build CSDN2Word.csproj -c Release
```

产物：`bin\Release\net472\CSDN2Word.exe`，同样是**单文件**
（依赖全部来自 .NET Framework 内置程序集，没有第三方 DLL）。

### 源码结构

| 文件 | 职责 |
| --- | --- |
| `src/HtmlParser.cs` | 容错 HTML 解析器（自写，零第三方依赖） |
| `src/ArticleFetcher.cs` | 抓取、编码识别、元信息提取、正文定位、博主文章枚举 |
| `src/ArticleConverter.cs` | DOM → WordprocessingML（标题/列表/表格/代码/引用/图片） |
| `src/DocxWriter.cs` | 手写 OOXML 打包 .docx（样式、编号、页脚、表格） |
| `src/ImageUtil.cs` | 图片尺寸探测与等比缩放 |
| `src/Wml.cs` | WordprocessingML 常量、段落/run 构造器 |
| `src/MainForm.cs` | 图形界面 |
| `src/Program.cs` | 入口 + 命令行 / 自测模式 |
| `tools/validate_docx.py` | 产出的 docx 结构与 OOXML 元素顺序校验脚本 |

**技术要点**：不依赖 python-docx、不依赖 OpenXML SDK、不依赖 Word。
`.docx` 的 ZIP 包与 XML 全部手写生成，因此才能做到 100 KB 单文件、零依赖。

---

## 📌 已知限制

1. **付费 / 专栏文章**只能抓到公开部分（CSDN 服务端就只返回这些）
2. **图片**需要网络能访问 `i-blog.csdnimg.cn`，否则自动跳过
3. **公式**：CSDN 的 LaTeX 公式转成图片，作为普通图片嵌入，不可编辑
4. **频繁抓取**可能触发 CSDN 反爬（返回 521），程序会自动重试，仍失败请隔几分钟再试
5. 仅支持 **Windows**；macOS / Linux 需要另写

---

## 📄 免责声明

- 本工具仅用于**个人学习、资料整理与离线阅读**
- 抓取内容的版权归原作者与 CSDN 所有，**请勿用于商业转载或二次发布**
- 请控制抓取频率，不要对 CSDN 服务器造成压力
- 使用本工具产生的任何后果由使用者自行承担

---

## ⭐ 再次提醒

如果这个工具帮你省下了排版的时间：

**请给本仓库点一个 Star ⭐，这是对作者最直接的支持。**

https://github.com/<你的GitHub用户名>/<仓库名>

---

## 📮 反馈

- 提 Issue：https://github.com/<你的GitHub用户名>/<仓库名>/issues
- 邮箱：<你的邮箱>
- 提 Issue 时请附上：CSDN 文章链接、`CSDN2Word.log` 内容、Windows 版本

---

## 📜 License

MIT License

Copyright (c) 2026 <你的GitHub用户名>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

<div align="center">

**如果觉得有用，点个 ⭐ Star 再走吧**

</div>
