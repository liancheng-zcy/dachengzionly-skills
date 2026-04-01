# dachengzionly-skills

Practical skills for Claude Code - structured workflows for feature modification.

## Installation

### Claude Code

```bash
/plugin marketplace add liancheng-zcy/dachengzionly-skills
/plugin install feature-modification-workflow@dachengzionly-skills
```

### Claude.ai

Upload the `skills/` folder via [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude).

## Skills

### feature-modification-workflow

A structured workflow for modifying existing features. Determines scenario complexity first (simple issue/bug fix/complex issue/refactoring), then chooses appropriate workflow.

**Features**:

- Scenario-based workflow selection
- 5-step process for complex changes
- Built-in documentation check guidance
- User confirmation before execution

### 反向决策检查

在开发新功能、新产品、接新需求前，用芒格"反向思考"方法进行风险评估。

**触发场景**：用户说"我想开发..."、"我打算做..."、"有个新想法..."、"这个方向值得投入吗？"

**核心理念**：先列"死法"，再找活路——知道会死在哪里，就永远不去那里。

### 周复盘检查清单

用芒格思维进行每周自我校准，持续优化决策质量。

**触发场景**：用户说"这周复盘一下..."、"周日了，总结一下..."、"帮我做周复盘..."

**核心理念**：定期复盘是保持决策质量的关键，防止偏离轨道。

### 能圈边界审视

判断新需求/新方向是否在你的核心能力范围内，防止能圈溢出。

**触发场景**：用户说"有人找我合作..."、"这个需求我能接吗？"、"该不该接这个活..."

**核心理念**：知道自己能圈边界的人，比能圈很大但不知道边界的人更安全。

### 解决方案包装器

把工具/功能包装成用户想要的"解决方案"，提升产品价值和定价空间。

**触发场景**：用户说"帮我写个产品介绍..."、"这个功能怎么卖..."、"用户不买单..."

**核心理念**：用户买的不是"工具"，而是"结果"。

## License

Apache 2.0