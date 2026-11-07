# Agent Memory Boundary Designer

一个用于设计 AI Agent 记忆边界的可复用 Skill：将“加记忆”拆成分类、来源、读写范围、过期、撤销、冲突处理和回归验收。

## 适用场景

- “帮我设计多 Agent 的共享记忆规则”
- “哪些用户信息能被长期记住？”
- “给我们的 Agent 做记忆 TTL 和撤销机制”
- “How should we prevent stale or cross-project agent memory?”

## 流程

`范围盘点 → 分类字段 → 读写与共享边界 → 冲突规则 → 回归用例 → 试点包`

输出包括记忆分类表、读写矩阵、TTL/撤销规则、提示词注入防护点和可执行验收用例。

## 示例

输入：`为客服与销售两个 Agent 设计共享记忆；客户偏好不得跨客户读取，报价 30 天后失效。`

输出：可直接交给产品、安全与工程评审的 Markdown “Agent Memory Boundary Pack”，明确每类记忆的来源、所有者、读取范围、写入门槛、TTL 与撤销人。

## 安装

将本目录复制至 Claude Code 的技能目录：

```text
~/.claude/skills/agent-memory-boundary-designer/
├── SKILL.md
└── README.md
```

本机保留中文目录便于管理；安装目录应使用上面的英文 slug，而不是中文文件夹名。

## 发布

仓库建议名：`agent-memory-boundary-designer`。发布前先运行 `smoke-test.md` 中的结构和触发干运行检查；仅在新建空仓库、`gh` 已登录且不需要覆盖现有远端时发布。禁止强推。
