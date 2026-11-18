# 中文发明专利项目工作流

给正在准备中文发明专利材料的研发人员使用。它把相似专利的查找和精读、现有技术的不足、交底书实施方案、术语润色、反馈修订和申请稿复核串在一起。软件演示、使用手册和软著材料是可选分支。

**核心产物是可追溯的交底稿。** 每个重要判断都能回到公开资料、项目事实或发明人确认。既可以从头推进，也可以单独处理一节、一张图或一轮修改。

## 开始使用

将整个 `patent-project-workflow` 文件夹放入项目的 `.agents/skills/`，或个人目录的 `~/.agents/skills/`。然后在 Codex 中指定 `$patent-project-workflow`。文件夹内需保留 `SKILL.md` 及其相对路径引用。 [Codex Skill 文档](https://learn.chatgpt.com/docs/build-skills)

```text
用 $patent-project-workflow，按我提供的模板和当前确认稿推进交底书。
先梳理现有技术的证据和不足，再写技术问题、目的和实施方式。
正文中把尚未确认的配置和未测试的效果保留为待核事项。
```

```text
用 $patent-project-workflow，仅复核这份申请文件初稿与交底书的一致性。
定位到权利要求、段号、步骤或图号，给出修改建议。本轮只读。
```

没有 Agent Skills 客户端时，也可以阅读流程和直接复制 Prompt。Markdown 工作流可独立使用。全文检索需要网页访问，Word 或软件材料按实际交付选用对应工具。

## 研发人员怎样参与

研发人员提供模板、已有方案和对比线索，决定技术主线、适用边界及待实现的细节。检索阶段共同确认哪些对比件值得精读。成文阶段逐轮确认术语、公式、实施条件、发明点和效果依据。收到审阅反馈后，决定哪些意见采纳、改到哪里、如何标记。软件分支由研发人员确认实际演示范围及手册版本。Skill 将每次确认落到证据、段落、图件或验证记录。

## 从哪里读

| 文件 | 内容 |
| --- | --- |
| [SKILL.md](SKILL.md) | 工作入口、阶段顺序和交付口径 |
| [检索与比对](references/prior-art.md) | 检索词组合、公开文本、证据定位、差异及不足 |
| [交底与申请稿](references/disclosure.md) | 大纲、章节、公式附图、修订及跨稿核对 |
| [可复制 Prompt](references/prompts.md) | 查找和证据对照、术语自然化、压缩、标题、审阅与局部修订 |
| [工具与用途](references/tools.md) | 有实际工作记录的工具、承担的任务和等效替代 |
| [软件配套](references/software.md) | 原型、测试、界面优化、截图手册和软著 |
| [项目工作表](assets/workbook.md) | 可复制的证据卡、技术链、术语表和修改表 |
| [虚构示例](examples/worked-example.md) | 从比对、交底编写到审阅的离线走读 |

## 发布自己的版本

1. 把本目录复制到独立的新目录，作为公开仓库的根目录。初次检入时暂存表中源文件、本 README、`agents/openai.yaml` 和选定的许可文件，再用 `git diff --cached --name-only` 核对文件清单。 [GitHub 导入本地项目](https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github)
2. 发布前通读现有文件和示例。公开仓库收录通用流程和虚构示例。真实交底书、原始图件、检索记录、批注、截图、内部应用链接和旧仓库历史保留在私有工作区。新贡献也适用同一原则。
3. 决定他人可以怎样使用、修改与传播这些内容。准备开源时，在仓库根目录添加选定的 `LICENSE`，填入合适的权利人信息。第三方工具使用其自身许可，工具实现和安装包单独从原渠道获取。 [GitHub 许可说明](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)
4. 在干净目录用虚构示例试跑一次，再按需创建首个 Release。发布说明可写明中文发明专利适用范围、安装方法、可独立使用的 Prompt、按需依赖及示例入口。

## 许可证

本仓库的 Skill、提示词、模板和示例采用 [MIT 许可证](LICENSE)。引用的第三方工具各自适用其许可。
