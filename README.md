# ai-learning-materials — 个人学习资料仓库

用 AI 构建的个人版学习资料生成体系：一个可复用的**学习资料生成 Skill** + 用它生成的**结构化概念学习资料**。

## 这是什么

本仓库包含两部分：

1. **项目级 Skill**：`learning-material-generator` —— 一个"概念 → 结构化学习资料"的生成器。
   输入任意概念，按固定流程产出含学习目标、机制原理、应用场景、误区辨析、自测题、参考资料的 HTML 学习页。
2. **学习资料**：首批用该 Skill 生成的四份资料（Agent / 大模型的上下文 / Skill / 三者关系）。

## 目录结构

```
ai-learning-materials/
├── .workbuddy/
│   └── skills/
│       └── learning-material-generator/
│           └── SKILL.md            # 项目级 Skill（YAML frontmatter + 生成流程 + 质检清单）
├── learning-materials/
│   ├── agent.html                  # 概念：Agent（智能体）
│   ├── llm-context.html            # 概念：大模型的上下文
│   ├── skill.html                  # 概念：Skill
│   ├── concept-relationship.html   # 三者关系（网页版）
│   └── concept-relationship.md     # 三者关系（Markdown 版，含 Mermaid 图）
├── README.md
└── .gitignore
```

## 如何使用这个 Skill

1. 用 WorkBuddy 打开本仓库（Skill 位于 `.workbuddy/skills/`，打开后自动可用）；
2. 对 AI 说，例如：
   - 「用 learning-material-generator 为「RAG」生成学习资料」
   - 「我想搞懂「微调」，帮我生成学习笔记」
3. 生成结果会按 Skill 规定的固定结构输出到 `learning-materials/<概念slug>.html`；
4. **完成后请在页面底部的"个人理解"区补写自己的话**——这是本流程的必要环节，不是可选项。

## 学习资料索引

| 资料 | 概念 | 状态 |
|------|------|------|
| [agent.html](learning-materials/agent.html) | Agent（智能体） | ✅ 已生成，个人理解待补写 |
| [llm-context.html](learning-materials/llm-context.html) | 大模型的上下文 | ✅ 已生成，个人理解待补写 |
| [skill.html](learning-materials/skill.html) | Skill | ✅ 已生成，个人理解待补写 |
| [concept-relationship.html](learning-materials/concept-relationship.html) | 三者关系 | ✅ 已生成，个人理解待补写 |

## 人工检查与修改说明

本仓库内容按"AI 生成 + 人工核对"的流程产出，如实记录如下：

- **AI 生成部分**：四份学习资料的初稿、SKILL.md 的流程框架，均由 AI（WorkBuddy）依据学习资料生成 Skill 产出；
- **人工核对部分**：本人逐篇阅读并核对了概念定义与官方口径的一致性、参考链接的真实性、自测题答案的正确性；对表述不通顺、不符合个人学习习惯的地方做了修改（修改后补充在此处）；
- **个人理解区**：所有页面中的"个人理解"区为本人的话，AI 不代写；生成时仅留白或基于本人提供的初稿润色。

## 后续计划

- 持续用该 Skill 沉淀新概念的学习资料（RAG、微调、评测……）
- 为高频自测错题补充"错题回顾"章节
- 把"个人理解"区与复习记录打通，形成长期记忆曲线
