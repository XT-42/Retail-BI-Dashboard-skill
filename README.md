# Retail-BI-Dashboard-skill
### 🎯这个 Skill 到底要解决什么问题？
分析师在制作 BI 看板时，通常卡在三个地方：<br>
不知道该看什么 → 指标体系不清晰，不知道业务关心什么
不知道怎么组织 → 页面结构乱，老板看不懂<br>
不知道好不好 → 没有行业标准参照，只能凭感觉

这个 Skill 的核心价值应该是：给定行业+业务场景，输出一套"拿来即用"的标准化看板蓝图，包括指标体系、页面结构、可视化建议、数据口径说明。




### 🚀 如何使用这个 Skill 工作？

只需将 `system_prompt.md` 粘贴到你的大模型系统指令（System Instructions）中。当业务分析师对大模型说出请求时，例如：

> **🗣️ 分析师输入**: 
> *"我是个业务数据分析师，我们需要做一个关于【零食量贩】行业的‘店长经营日报’看板，老板想要管控那些不赚钱的加盟商，并且抓住卖得不好的商品。帮我出一个方案。"*

**大模型就会根据内置的结构与知识库，自动输出：**

1. **📖 指导手册 (How-to Guide)**：用券商和咨询顾问的语气，告诉分析师零食量贩的核心是看“极低毛利下的高周转和加盟商生命周期”，并且提醒在数据清洗时要剔除“总部直营补贴”的干扰因素。
2. **📊 PRD + 指标字典**：输出精准的计算逻辑（例如：明确提供 `SKU汰换率`、`单店盈亏平衡点预测` 的 SQL 级计算口径）。
3. **🎨 Quick BI 看板设计**：给出针对性的页面架构，包括全局过滤器、KPI翻牌器（日均GMV、缺货率）、加盟商留存分析图表，以及带有“标红预警条件格式”的交叉表详细布局方案。


### 📂 Skill 文件系统目录结构

```text
/mnt/skills/user/fmcg-bi-dashboard/
│
├── 📘 SKILL.md                    ← 主入口：触发说明 + 完整流程
│
├── 🏭 industries/                 ← 6个行业独立体系
│   ├── snack-retail.md             零食量贩
│   ├── beverage.md                 饮料
│   ├── dairy.md                    乳制品
│   ├── supermarket.md              商超
│   ├── convenience-store.md        便利店
│   └── community-retail.md         社区零售
│
├── 👥 roles/                      ← 6个角色的审查视角（内化用）
│   ├── data-scientist.md           数据科学家视角
│   ├── securities-analyst.md       证券分析师视角
│   ├── retail-operations.md        零售运营视角
│   ├── data-pm.md                  数据产品经理视角
│   ├── bi-architect.md             BI架构师视角
│   └── mckinsey-consultant.md      麦肯锡顾问视角
│
├── 🧩 templates/                  ← 交付物模板
│   ├── prd-template.md             PRD文档模板
│   ├── dashboard-wireframe.md      看板设计稿模板
│   └── metric-dictionary.md        指标字典模板
│
└── ⚙️ process/                    ← 标准化流程
    ├── step1-diagnosis.md          业务诊断
    ├── step2-metrics.md            指标体系
    ├── step3-structure.md          页面结构
    ├── step4-visualization.md      可视化方案
    └── step5-data-spec.md          数据口径
```
