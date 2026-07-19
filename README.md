# 🎯 简历项目面试官 - Resume Project Interviewer

[![Stars](https://img.shields.io/github/stars/Mrmr888/interviewing-resume-projects?style=flat-square)](https://github.com/Mrmr888/interviewing-resume-projects/stargazers)
[![Forks](https://img.shields.io/github/forks/Mrmr888/interviewing-resume-projects?style=flat-square)](https://github.com/Mrmr888/interviewing-resume-projects/forks)
[![Last Commit](https://img.shields.io/github/last-commit/Mrmr888/interviewing-resume-projects?style=flat-square)](https://github.com/Mrmr888/interviewing-resume-projects/commits/main)
[![Issues](https://img.shields.io/github/issues/Mrmr888/interviewing-resume-projects?style=flat-square)](https://github.com/Mrmr888/interviewing-resume-projects/issues)
[![License](https://img.shields.io/github/license/Mrmr888/interviewing-resume-projects?style=flat-square)](LICENSE)

一个专门“拷打”实习生项目经历的 Codex Skill。读取候选人的真实简历，围绕后端、Agent、RAG、LLM 与 AI 应用项目连续追问，判断项目是否真正做过、技术是否理解、问题是否能定位、方案是否经得住变化。

> 核心原则：优先判断“做过”，而不是“背过”；所有问题和评分都必须能追溯到简历或候选人的回答。

## ✨ 核心特性

### 📄 基于简历取证

- 支持 PDF、DOCX 附件与粘贴文本
- 区分“简历明示”“待确认”“回答新增”三类证据
- 不自行补全项目规模、个人职责、性能数据或技术实现
- 发现简历与回答不一致时要求澄清，不直接断言造假

### 🔍 像真实面试官一样追问

- 一次只问一个主问题，根据回答动态选择下一题
- 对“优化了”“提高了”“用了 Agent”等模糊表述持续追问
- 从个人贡献一路深入到原理、取舍、故障和扩容场景
- 支持随时结束、切换项目、切换模式或立即复盘

### 🧠 聚焦三类技术项目

| 方向 | 重点考察 |
| --- | --- |
| 后端开发 | 数据库、索引、缓存、并发、事务、接口、可靠性、容量与部署 |
| Agent 开发 | 工具调用、规划与停止、上下文、记忆、状态、失败恢复、评测与权限 |
| AI 应用 | 模型选型、Prompt、结构化输出、RAG、幻觉、评测、延迟、成本与隐私 |

### 📊 证据化评分与复盘

- 真实性与个人贡献：25 分
- 技术理解深度：25 分
- 问题定位与解决能力：20 分
- 工程化与可靠性意识：15 分
- 取舍与反思能力：10 分
- 表达清晰度：5 分

每个维度都会标记为“已证明”“部分证明”“未证明”或“未考察”，并给出证据、扣分原因、风险点和后续练习问题。

## ⚙️ 面试模式

| 配置 | 可选项 | 默认值 |
| --- | --- | --- |
| 面试模式 | 动态面试 / 问题清单 | 动态面试 |
| 压力等级 | 温和 / 标准 / 高压 | 标准 |
| 反馈方式 | 统一复盘 / 逐题教练 | 统一复盘 |

- **动态面试**：最多 12 个主问题或约 30 分钟，一次一问并持续追问。
- **问题清单**：按简历中的每个项目分别生成真实性、技术深挖、故障场景与复盘问题。
- **高压模式**：提高追问密度和证据要求，但始终保持专业，不进行羞辱或人身攻击。

## 🚀 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/Mrmr888/interviewing-resume-projects.git
cd interviewing-resume-projects
```

### 2. 安装 Skill

Windows PowerShell：

```powershell
Copy-Item -Recurse .\skills\interviewing-resume-projects "$HOME\.codex\skills\interviewing-resume-projects"
```

macOS / Linux：

```bash
cp -R ./skills/interviewing-resume-projects ~/.codex/skills/interviewing-resume-projects
```

重新打开 Codex，使 Skill 被重新发现。

### 3. 开始面试

附加简历后输入：

```text
使用 $interviewing-resume-projects 读取我附加的简历。
采用动态面试、标准压力、统一复盘，重点深挖后端和 Agent 项目。
```

生成完整问题清单：

```text
使用 $interviewing-resume-projects，根据下面的项目经历生成高压问题清单。
每个项目分别出题，并说明每题的考察点。
```

逐题训练：

```text
使用 $interviewing-resume-projects 开始温和模式的动态面试，采用逐题教练反馈。
```

## 🧪 一次面试如何进行

1. 读取简历并建立项目证据表
2. 确认面试模式、压力等级与反馈方式
3. 从项目目标、职责和结果开始核验真实性
4. 根据回答进入技术原理、工程细节与故障场景
5. 检查取舍、失败经历和重新设计思路
6. 输出 100 分评价、证据、风险与练习建议

## 📁 仓库结构

```text
skills/interviewing-resume-projects/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── backend.md
    ├── agent.md
    └── ai-app.md
```

## 🔐 隐私提示

简历通常包含姓名、电话、邮箱、公司名称和内部项目信息。提交 Issue、测试样例或面试记录前，请先删除个人信息、凭据、业务数据和其他敏感内容。

本 Skill 不需要额外的网络请求、分析服务或遥测。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request：

- 补充更有区分度的后端、Agent 或 AI 应用追问维度
- 提供已经脱敏的失败案例与边界场景
- 改进面试流程、评分标准或安装说明

贡献内容不得包含真实候选人的个人信息、公司秘密或未经授权的简历内容。

## 📜 许可证

本项目采用 [MIT License](LICENSE)。

## 🙏 致谢

README 的信息组织与徽章展示风格参考了 [anbeime/skill](https://github.com/anbeime/skill)，项目内容与实现均为独立设计。
