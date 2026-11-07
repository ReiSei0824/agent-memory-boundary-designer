# Smoke Test — 2026-11-07

## 结构检查：通过

- `name` 为 `agent-memory-boundary-designer`，仅小写字母与连字符。
- 初稿 `description` 为 167 个字符，超出 150 字符规范；已修复前不能发布。

## 修复记录

- 将 description 压缩为 149 个字符，保留“何时触发、记忆生命周期、可信召回”。

## 复检：通过

- 必要章节齐全：核心定位、触发场景、工作流、输出格式、Gotchas。
- 工作流为 6 步；Gotchas 为 6 条；SKILL.md 中不存在未填充占位符。
- README 的安装路径、仓库名、文件树、示例触发词均指向 `agent-memory-boundary-designer`。

## 触发干运行：通过

| 输入 | 预期落点 | 结果 |
|---|---|---|
| `帮我给客服 Agent 设计记忆规则，客户偏好不能串给别的客户。` | 分类、读取范围、TTL、撤销和回归用例 | 输出会进入 Boundary Pack，而非泛泛建议。 |
| `How do we set expiry and revocation for shared agent memory?` | shared-memory lifecycle and test matrix | 输出会进入同一 Boundary Pack，并区分计划与已验证。 |

## 结论

**修复后通过。** description 的最终长度已按文件内容复算为 149 characters；可进行新仓库发布检查。
