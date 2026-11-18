# 工具与用途

本表依据实际工作记录和交付产物整理。「工作记录」列说明工具完成了哪一步。工具按任务和环境选用，可用等效工具完成同一核对。

| 阶段 | 实际使用 | 工作记录与产物 | 等效做法 |
| --- | --- | --- | --- |
| 命中文献与官方资料 | Codex 网页检索、Google Patents、国家知识产权局公开页面 | 检索得到候选，打开文献核读公开说明书与权利要求，回查官方公开资料和出处。 | 用可访问的公开专利数据库取得正文，所需原版图文、日期及状态回查官方来源。 |
| 全文离线整理 | Python、Requests、Beautiful Soup | 保存原网页快照，分别提取摘要、说明书和权利要求，制作 HTML 与 Markdown 阅读版，标明图像缺失。 | 少量材料可用浏览器另存网页或原版 PDF，手工摘取并保留定位信息。 |
| 方案和发明点组织 | Codex、`patent-disclosure` 相关方法 | 读取交底和专利点挖掘指引，用于梳理方案主线、技术手段差异与发明点，并产出章节稿。 | 用本 Skill 的证据链和章节模板独立完成。 |
| 术语及自然化润色 | `humanizer-zh` | 用于现有技术介绍、实施流程核对后润色和指定段落压缩。 | 直接使用本 Skill 的 [Prompt 4–6](prompts.md)。 |
| Word 编辑和变更比对 | `documents` 的处理流程、Python、`python-docx`、OpenXML、`lxml` | 保留模板和公式，写入或替换指定段落，标红相关文字，在副本中核对正文与图件变更。 | 用 Word 的样式与比较功能，必要时检查 DOCX 的正文、数学结构和图件。 |
| 附图和实施例核对 | Python、SVG、PNG，原生矢量与脚本 | 绘制或修改流程图和系统图，导出可插入稿件的图件。用 Python 复算构造实例中的关键结果。 | 用能保存可编辑图源的工具，逐节点核对。可用小脚本或手算验证关键条件。 |
| Word、PDF 版式检查 | Microsoft Word 只读导出 PDF，Poppler、`pdf2image` 或 PyMuPDF，`pdfplumber` 辅助提取 | 由 Word 导出当前稿，渲染页面，对照分式、图片和分页。独立 PDF 样式稿也曾用 Playwright 浏览器打印。 | 用可实际渲染的 PDF 阅读器或导出工具，打开有代表性的公式、图和跨页处，完整终审逐页看。 |
| 交底与申请稿审阅 | Codex 多视角审阅及子代理 | 并行核读技术、对比材料、版式或跨稿一致性，再汇总定位意见、复核已修订项。 | 同一人按三个视角顺序审阅，或者交给有相应资料权限的同事。 |
| 软件演示和界面 | HTML/CSS/JavaScript、Node.js、Chrome、Playwright、`impeccable` | 实现并打包演示，运行逻辑用例及浏览器操作检查，对界面做精修并核对桌面、移动端。 | 使用项目已有框架，保留可运行包、检查记录和真实操作图。 |
| 在线演示 | Codex Sites | 在获准的工作范围内创建在线演示并更新版本。 | 用离线包交付，或使用获准的托管环境。 |
| 软著材料 | `software-copyright-materials`、OfficeCLI 1.0.151、Playwright | 做源码选材和操作手册草稿，截图来自运行中的页面。OfficeCLI 生成代码和手册先行 DOCX，再核对页数和嵌图。 | 仅在需要此分支时按所用工具的当前版本要求及接收方格式执行。 |
| 检索及工具安装的辅助路由 | `agent-reach` 指引、GitHub CLI | 路由到可用的检索能力，读取所需第三方技能的公开仓库和发布信息。专利的可引用证据来自实际打开的文献。 | 直接访问官方文献和第三方工具上游。 |

工具可以按需组合复用。明示的工具调用、生成记录和可用交付件分别支持不同深度的使用结论。环境探测、安装或单次试跑只能说明这个动作本身。每次交付写清实际核过的范围。

第三方技能可从原渠道取得。 [Humanizer-zh](https://github.com/op7418/Humanizer-zh) · [Impeccable](https://github.com/pbakaus/impeccable) · [SoftwareCopyright-Skill](https://github.com/Fokkyp/SoftwareCopyright-Skill) · [OfficeCLI](https://github.com/iOfficeAI/OfficeCLI)
