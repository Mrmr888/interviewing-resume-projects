# Resume Project Interviewer Skill

一个面向实习生技术面试的 Codex Skill。它从候选人提供的简历项目经历出发，针对后端、Agent、RAG、LLM 和 AI 应用开发进行真实性核验、技术深挖、故障场景追问与证据化复盘。

## 功能

- 读取 PDF、DOCX 附件或粘贴的简历文本
- 动态面试与问题清单两种模式
- 温和、标准、高压三档强度
- 统一复盘与逐题教练两种反馈方式
- 后端、Agent、AI 应用三类按需深挖参考
- 只依据简历和候选人回答，不编造项目事实或数据
- 100 分证据化评分与实习技术面建议

## 安装

下载或克隆本仓库后，将 Skill 目录复制到 Codex 的全局 Skills 目录。

Windows PowerShell：

```powershell
Copy-Item -Recurse .\skills\interviewing-resume-projects "$HOME\.codex\skills\interviewing-resume-projects"
```

macOS / Linux：

```bash
cp -R ./skills/interviewing-resume-projects ~/.codex/skills/interviewing-resume-projects
```

重新打开 Codex 后即可调用：

```text
$interviewing-resume-projects
```

## 使用示例

```text
使用 $interviewing-resume-projects 读取我附加的简历。
采用动态面试、标准压力、统一复盘，重点深挖后端和 Agent 项目。
```

也可以直接粘贴简历项目内容，并要求生成完整问题清单：

```text
使用 $interviewing-resume-projects，根据下面的项目经历生成标准压力的问题清单。
```

## 仓库结构

```text
skills/interviewing-resume-projects/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── backend.md
    ├── agent.md
    └── ai-app.md
```

## 隐私提示

简历可能包含姓名、电话、邮箱和公司内部信息。公开 Issue、日志或测试样例前，请先删除个人信息和敏感数据。

## License

[MIT](LICENSE)
