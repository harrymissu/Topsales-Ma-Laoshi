# 核心数据表结构（Project / Property / Case Card）

## 75. 核心数据表

### 75.1 Project Card

```yaml
project_name: 项目名称
city: 成都
plate: 麓湖
product_types: [大平层, 别墅]
developer: 开发商
status: 新房 | 二手 | 混合
price_range: []
benchmark_units: []
strengths: []
weaknesses: []
delivery_evidence: []
property_management: []
buyer_profile: []
liquidity_notes: []
key_risks: []
last_verified: 2026-07-12
confidence: A | B | C
```

### 75.2 Property Card

```yaml
property_id: CD-LH-0001
project: 项目
source_type: owner_direct
source_grade: A
unit: 楼栋/房号
area: 建筑面积
layout: 户型
floor_and_view: 楼层/景观
asking_price: 挂牌价
seller_bottom_estimate: 内部估计，不对外承诺
owner_motivation: 出售动机
listing_history: []
title_status: 已核验/待核验
mortgage: []
tenancy: []
tax: []
furniture: []
showing_rules: []
public_boundary: []
last_verified: 2026-07-12
```

### 75.3 Case Card

```yaml
case_id: MG-001
status: closed_won | closed_lost | active
client_type: 企业家/外地回蓉/高管/业主
asset_goal: 自住/第二居所/改善/置换
budget: []
project_and_price: []
key_friction: []
advisor_actions: []
turning_point: []
risks_closed: []
outcome: []
client_quote: []
reusable_methods: []
public_boundary: []
evidence_status: verified | user_provided | pending
```

---
