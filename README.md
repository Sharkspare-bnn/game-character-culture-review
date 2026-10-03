# 游戏角色设定出海文化预审 Skill
# Game Character Cultural Pre-Review Skill

[中文](#中文) · [English](#english)

---

## 中文

一个 Claude Agent Skill，在游戏角色和皮肤的**概念设计阶段**，针对海外目标市场做文化预审。支持中英文：用中文提问输出中文报告，用英文提问输出英文报告。

### 它做什么

输入角色设定、概念图和目标市场，按四层检查风险：

1. **文化与符号**：宗教、神话、历史、民族服饰、手势、颜色、装饰文字
2. **跨语言命名**：谐音、撞名、名字与原型是否自洽
3. **分级与法规**：暴露程度、暴力细节、特定市场的内容限制
4. **当地受众预期**：刻板印象、社区历史、市场间分化

输出一份七部分报告：按市场分开的结论、风险定位表、概念图标注、受众读法推演、"修改设计"与"坚持原设计的缓冲方案"两套处理方案、回流检查、需人工确认事项。

### 市场覆盖

| 档位 | 市场 |
| --- | --- |
| 核实市场 | 日本、韩国、北美 |
| 初步参考市场 | 欧洲、东南亚、中东 |
| 回流检查 | 中国大陆 |

### 文件结构

```
SKILL.md                  主流程与运行规则
references/               检查清单、原型库、命名方法、缓冲手段、市场文件、案例库
templates/report.md       报告模板（含英文报告用语）
examples/walkthrough.md   完整示例（虚构角色）
```

### 使用方法

下载本仓库（Code → Download ZIP），在 Claude 的 设置 → 功能 → Skills 中上传。之后提供角色设定与目标市场即可触发。

### 重要说明

- 这是设计阶段的初筛工具，**不替代当地文化顾问和法务审核**
- 参考资料为初稿，标注了核实日期；原型库评级只是审查起点
- 涉及高敏感原型时，skill 会要求定稿前由当地顾问复核
- 参考资料目前以中文写成；输出英文报告时，内容会由模型译成英文
- 欢迎通过 Issue 或 Pull Request 补充案例和市场资料，每条请附可查证来源

---

## English

A Claude Agent Skill for cultural pre-review of game characters and skins at the **concept design stage**, before art and voice work are locked. Bilingual: ask in English to get an English report, ask in Chinese to get a Chinese report.

### What it does

Given a character brief, concept art and target markets, it checks four layers of risk:

1. **Culture and symbols**: religion, mythology, history, traditional dress, gestures, colors, decorative text
2. **Cross-language naming**: homophones, name collisions, whether the name fits its source
3. **Ratings and regulation**: exposure, violence, market-specific content limits
4. **Local audience expectations**: stereotypes, community history, divergence between markets

It produces a seven-part report: a verdict per market, a risk map, concept art annotations, local audience reading, two response options ("revise the design" and "keep the design, mitigate the risk"), a home-market spillover check, and items requiring human review.

### Market coverage

| Tier | Markets |
| --- | --- |
| Verified | Japan, South Korea, North America |
| Preliminary | Europe, Southeast Asia, Middle East |
| Spillover check | Mainland China |

### Structure

```
SKILL.md                  Workflow and operating rules
references/               Checklists, archetype table, naming method, mitigation options, market files, case bank
templates/report.md       Report template (with English wording)
examples/walkthrough.md   Full worked example (fictional character)
```

### How to use

Download this repository (Code → Download ZIP) and upload it in Claude under Settings → Capabilities → Skills. Then share a character brief and target markets to trigger it.

### Important notes

- This is a first-pass screening tool for the design stage. It **does not replace local cultural consultants or legal review**
- Reference files are drafts with review dates; archetype ratings are a starting point, not a verdict
- When a design touches highly sensitive references, the skill requires local consultant review before sign-off
- Reference files are currently written in Chinese; English reports are produced by the model translating that content
- Contributions of cases and market notes are welcome via Issues or Pull Requests; please include a verifiable source for each
