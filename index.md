# 量潮客户支持手册

客户支持领域的工作手册。本手册介绍客户支持的核心工作流程——CODE 循环。

## 核心工作流程：CODE 循环

客户支持云的知识生产遵循 CODE 循环（Capture → Organize → Distill → Express），把原始对话流变成可复用的解决方案资产，再让资产服务客户并回流新问题——循环转得越快、人工越少，支持能力越强。

```
原始对话流（群聊/邮件/工单）
   │ ① Capture 保真
   ▼
消息流 ──② Organize 建模──▶ 五要素案例流（journal）
   │ ③ Distill 造资产
   ▼
解决方案条目库（profile）
   │ ④ Express 生价值
   ▼
AI 应答客户 + 信号反哺需求地图 ──▶ 新问题回流 ①，循环闭合
```

### ① Capture：保真

全量捕获支持触点的原始记录（群聊、邮件、工单、一对一），多源归一成统一消息模型。**只保真，不筛选**——筛选是下一步的事，这里丢一条，蒸馏就少一块原料。执行规范见 journal 的来源格式。

### ② Organize：建模

把消息按「一次支持事件」聚类成五要素案例：**客户 → 问题 → 解答 → 状态 → 沉淀**。聚类单元是事件不是天；系统消息与寒暄在此过滤。五要素是下一步的契约：`状态：已解决` 是蒸馏触发旗标，`沉淀` 是条目种子，`来源` 让复用率可数。

### ③ Distill：造资产

把已解决的案例蒸馏成解决方案条目（适用场景/解答/升级判据/来源与复用），入库并登记索引。要点：

- **三种触发**：流（案例关闭即蒸馏，FAQ 当天）、批（每周清扫未蒸馏案例）、频率（同类问题 2+ 次提级）
- **蒸馏分两档**：FAQ/制度/操作指引走自动档（AI 起草、人抽查）；背景/演进类走人工档（AI 备料、人拼因果链）——错误的背景比没有背景更毒
- **质量门**：升级判据强制显式化（空字段 ≠ 没有）；入库即索引（只入库不进索引等于没入库）
- **执行形态**：候选条目 = 对 profile 仓库的 PR，回答者 approve 后 merge 即生效
- 条目生命周期：`案例 → 候选条目 → 生效条目 → 归档条目`，失效显式标记不删除，保留演进史

条目库：`data/profile/`，现状见 [profile/qtclass/README](https://github.com/quanttide/quanttide-profile-of-customer-support/blob/main/qtclass/README.md)。

### ④ Express：生价值

条目库被消费，产出双向价值：

- **对外**：AI 检索条目第一级应答，回答附「由条目 X 支持，已复用 N 次」（引用即交付信任）；命中升级判据即转人工
- **对内**：需求与缺陷信号结构化后喂给需求地图——支持是法源的传感器；无需人参与比例、复用率从 journal 基线持续出趋势线

Express 的输出（新问题、升级案例）回流 Capture，**循环闭合**——自进化就是这个环转得越来越快、人工越来越少。

## 配套文档

| 文档 | 内容 |
|---|---|
| 意图 | [data/intention](https://github.com/quanttide/quanttide-intention-of-customer-support)——为什么做、自进化、储电站模式 |
| 洞察 | [data/insight](https://github.com/quanttide/quanttide-insight-of-customer-support)——背景类知识、管线设计 |
| 日志 | [data/journal](https://github.com/quanttide/quanttide-journal-of-customer-support)——案例流（Capture/Organize 的产物） |
| 档案 | [data/profile](https://github.com/quanttide/quanttide-profile-of-customer-support)——解决方案库（Distill 的产物） |
| 开发指南 | [qtcloud-support docs/dev-guide](https://github.com/quanttide/qtcloud-support/blob/main/docs/dev-guide/index.md)——设计原则与最小闭环 |
| 用户指南 | [qtcloud-support docs/user-guide](https://github.com/quanttide/qtcloud-support/blob/main/docs/user-guide/index.md)——核心循环的用户视角 |
