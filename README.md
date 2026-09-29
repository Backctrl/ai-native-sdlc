# AI-native SDLC：AI 原生团队开发流程

帮助团队把需求意图、设计规格、实现计划、协作交接和验证证据连起来的中文 Skill。适用于接入团队规范、推进功能或缺陷、协调多角色交付，以及审查验收证据。

当前 Skill 版本：**1.0.0**。流程覆盖 **Plan → Design → Build → Test → Deploy → Maintain**，按任务规模选择轻量、标准或增强记录深度。

## 安装

本仓库的 [`ai-native-sdlc/`](ai-native-sdlc/) 是完整 Skill，安装时保留其目录结构。

**Codex 团队项目：**下载仓库后，将 `ai-native-sdlc/` 整体复制到目标项目的 `.agents/skills/ai-native-sdlc/`，并随项目纳入版本管理。也可以将本仓库链接交给支持 GitHub Skill 安装的 Codex，明确要求只安装 `ai-native-sdlc` 子目录。

**Claude Code：**可将同一份目录接入项目的 `.claude/skills/ai-native-sdlc/`。该环境的自动发现尚未在本项目验证，实际行为以目标工具版本为准。

如果选择器暂未发现新 Skill，可让当前 Agent 直接读取目标项目中 `ai-native-sdlc/SKILL.md` 的实际路径。完整接入步骤见 [团队接入](ai-native-sdlc/references/团队接入.md)。

## 开始使用

首次在团队项目中接入：

```text
请使用 $ai-native-sdlc，检查当前仓库并接入团队开发规范。
先交付基于现有事实的团队契约草案与规则差异。
```

推进具体工作：

```text
请使用 $ai-native-sdlc，实现工单 PROJ-123。
复用工单与现有设计作为真源，按任务规模推进，完成本地验证后交付。
```

审查交付证据：

```text
请使用 $ai-native-sdlc，只读审查这个 PR 的验收证据，
指出它现在处于哪个交付阶段，以及还缺什么。
```

## 包含的内容

| 内容 | 用途 |
| --- | --- |
| [SKILL.md](ai-native-sdlc/SKILL.md) | 核心流程、使用范围、协作与完成规则 |
| [阶段规范](ai-native-sdlc/references/阶段规范.md) | 六个阶段的输入、输出及进入下一步的证据 |
| [协作与交接](ai-native-sdlc/references/协作与交接.md) | 责任人、输入版本、文件所有权、任务交接 |
| [验证与持续改进](ai-native-sdlc/references/验证与持续改进.md) | 实际验证、自测与独立核验、反馈循环 |
| [模板目录](ai-native-sdlc/assets/templates/) | 团队契约、意图、规格、计划、交接、验证、评审、发布和事故记录 |
| [展示元数据](ai-native-sdlc/agents/openai.yaml) | Skill 的名称、简介与默认提示词 |

## 使用范围

Skill 提供方法、模板和协作指引。任务台账执行器、多 Agent 调度服务、CI/CD、分支保护、发布工具和监控需要结合团队的真实环境另行接入。`agents/openai.yaml` 是 Skill 展示元数据。

团队已有工单、设计平台、Git/PR 或知识系统时，继续引用已有真源。按本次工作取用模板，不批量创建空文档。安装 Skill 本身不代表采纳新的审批政策或授权外部操作。

团队共用一个版本；先用一个小工作项确认交接和验证方式，再根据实际问题调整规范。

## 来源

方法参考 [Anthropic Claude Academy — The AI-native SDLC playbook](https://academy.claude.com/zh-CN/courses/ai-native-sdlc-playbook)。这是中文团队化改编，包含记录深度、验收编号和交接模板等本包约定，不是官方课程全文或认证产品。详细对应关系见 [课程映射](ai-native-sdlc/references/课程映射.md)。
