# 02｜客户分层、决策模型与输入输出契约

> 本文件属于 jincheng-luxury-ma-laoshi Skill v1.0 的引用文件，由 SKILL.md 按需加载。脚注 [^...] 的来源定义见 docs/sources.md。

# 第六部分｜客户分层与高净值决策模型

## 17. 核心客户定义

### 17.1 第一核心客户

A8 及以上企业家和家庭，重点满足以下特征：

- 购买总价进入城市高端或顶豪区间。
- 时间稀缺，反感信息轰炸和低效带看。
- 决策受到家庭成员、企业现金流、隐私与交付确定性影响。
- 需要房源之外的谈判、协调、判断和后端服务。

> A8 为团队内部资产层级口径。不得在公开内容中根据客户职业、座驾、公司或消费行为推断、标注其资产。

### 17.2 次核心客户

- 外地回蓉或四川地市企业家。
- 新经济高管、专业人士和家族决策人。
- 豪宅卖方业主。
- 需要跨城市比较的高净值家庭。
- 需要成都第二居所、偶尔居住或家族会客空间的客户。

## 18. 高净值客户六大真实需求

1. **确定性**：不想在产权、交付和交易上踩坑。
2. **效率**：希望少看、看准、快速排除。
3. **控制感**：希望知道真实选择、底线和替代方案。
4. **隐私**：不希望身份、资金和家庭关系扩散。
5. **适配**：房子要匹配家庭结构、社交和生活方式。
6. **问题解决**：愿意为能处理非标问题的人付费或放弃返佣。
7. **现金流安全**：在较弱经济环境中，购房不能破坏家庭和企业的安全边界。
8. **可退出性**：即使以自住为主，也希望知道未来可能的接手客群和持有代价。

## 19. Decision Graph：家庭决策图

每个客户必须识别以下角色：

| 角色 | 需要确认的问题 |
|---|---|
| 需求提出者 | 谁最先提出换房或买房？ |
| 实际居住者 | 谁每天使用，谁的体验权重最高？ |
| 资金提供者 | 资金来自个人、家庭还是企业安排？ |
| 最终拍板者 | 谁能说“买”或“不买”？ |
| 否决者 | 谁不表态但可以阻止成交？ |
| 情绪影响者 | 子女、父母、伴侣、朋友、设计师、同业谁会影响？ |
| 专业顾问 | 是否有律师、财务、家办、银行或公司人员参与？ |

未识别决策图，不进入强推进。

## 20. 客户阶段分层

| 阶段 | 定义 | 核心动作 |
|---|---|---|
| C0 内容关注 | 只看内容，无明确需求 | 继续教育，不高频私聊 |
| C1 初步咨询 | 有兴趣但预算、时间不清 | 完成最小需求诊断 |
| C2 有效需求 | 预算、用途、区域和时间较清晰 | 建立客户画像与选筹假设 |
| C3 深度选筹 | 愿意提供信息并安排看房 | 三套以内组合、带看设计 |
| C4 决策推进 | 出现明确目标或报价意向 | 风险表、谈判、家庭共识 |
| C5 交易执行 | 已签意向、定金或合同 | 交易作战室、节点管理 |
| C6 后服务 | 已成交或交付 | 验房、装修、入住、资产档案、转介绍 |
| C7 长周期维护 | 暂不买、等待价格、旧房出售、资金或家庭共识 | 触发式价值沟通，不催单 |
| C8 流失 | 被其他渠道成交或主动终止 | 记录真实原因并复盘 |

---

# 第八部分｜输入与标准输出

## 25. Input Contract

Skill 的输入不是“客户想看什么房”，而是“客户为什么需要这类房，以及什么条件会让他不买”。

```yaml
client_profile:
  source: 客户来源
  city: 常住地与工作地
  occupation: 职业/企业类型
  family: 居住成员与家庭结构
  privacy_level: low | medium | high
capital_boundary:
  budget: 总预算区间
  cash_and_loan: 现金/贷款偏好
  funding_timeline: 资金到位时间
  old_asset_sale: 是否依赖旧房出售
  family_liquidity_boundary: 家庭资金安全边界是否已确认
  business_cashflow_dependency: 是否受企业回款/经营现金流影响
  downside_scenario: 若收入、融资或旧房出售延迟，计划如何调整
intent_vector:
  self_use: 0-10
  second_home: 0-10
  family_upgrade: 0-10
  children: 0-10
  identity_and_social: 0-10
  liquidity: 0-10
decision_graph:
  proposer: 谁提出
  resident: 谁居住
  payer: 谁付款
  decision_maker: 谁拍板
  vetoer: 谁否决
  influencers: 影响者
constraint_set:
  must_have: []
  must_not_have: []
  acceptable_tradeoffs: []
viewing_history:
  projects_seen: []
  liked: []
  rejected: []
  rejection_reasons: []
transaction_constraints:
  deadline: 时间要求
  title_or_company: 购房主体
  payment: 付款约束
  special_terms: 特殊条款
economic_cycle:
  macro_state: stable | cautious | stressed
  client_cycle_state: active | waiting_for_price | waiting_for_sale | waiting_for_cashflow | family_unresolved
  holding_horizon: 预计使用和持有周期
  trigger_events: []
seller_context:
  sale_reason: 出售原因
  sale_priority: price | speed | privacy | replacement
  carrying_cost: 空置、资金、物业和时间成本
  pricing_flexibility: 价格与条款弹性
interaction_log:
  client_quotes: []
  emotional_changes: []
  competitor_activity: []
  next_action_date: 必填
```

## 26. Output Contract

| 输出 | 标准 |
|---|---|
| Executive Conclusion | 先给结论：现在买、继续看、等待、换方向或不建议买 |
| Cycle Readiness | 需求、资金、产品、价格、交付五道门及 BUY / WAIT / REDIRECT / STOP |
| Downside Check | 旧房出售、融资、回款、家庭分歧和交付延迟的下行情景 |
| Client Memo | 一页真实需求、预算、决策图、风险和成交条件 |
| Asset Thesis | 为什么是这个城市、板块、产品和时间窗口 |
| Shortlist | 不超过 3 套，每套代表不同逻辑 |
| Why Not Buy | 每套必须写不适合买的理由 |
| Comparison Matrix | 地段、产品、稀缺、交付、价格、流动性、风险、适配 |
| Risk Register | 风险、证据、责任人、截止时间、状态 |
| Viewing Plan | 带看顺序、每套验证问题、家庭参与方式 |
| Negotiation Plan | 双方底线、筹码、节奏、让步矩阵、备选方案 |
| Follow-up Plan | 下一步动作、触达时间、触发事件和需要补充的信息 |
| Counter-cycle Plan | 客户维护、业主策略、核心社区、业务组合或 90 天动作（按模式输出） |
| Transaction Stage Map | 当前交易阶段、进入条件、退出条件、责任人、材料、风险、截止时间和备用方案 |
| Platform Native Pack | 指定平台的选题、标题/封面、脚本/正文、画面、证据、CTA、合规清单与复盘指标 |
| Case Note | 成交或流失原因、关键动作、可复制方法 |
| Public Content | 脱敏、合规、可传播，不泄露客户与交易敏感信息 |

---
