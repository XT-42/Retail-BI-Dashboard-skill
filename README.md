# Retail-BI-Dashboard-skill
这套体系通过 1个主控 System Prompt + 6个行业领域知识库 + 2套标准输出模板 构成。将6大顶级角色的能力深度内化在了工作流（Workflow）和思考框架（Think Frame）中，并严格贴合阿里云 Quick BI的功能特性进行最终交付。

📂 Skill 文件系统目录结构

```text
Retail-BI-Copilot/
├── 🤖 system_prompt.md            # 核心指令：定义角色、工作流、思考框架与输出规范
├── 📁 domains/                    # 6大行业独立知识体系（差异化内核）
│   ├── 01_fmcg_beverage_dairy.md  # 消费品（含乳制品/饮料）
│   ├── 02_supermarket.md          # 连锁商超
│   ├── 03_bulk_snack.md           # 零食量贩（极简/高周转）
│   ├── 04_convenience_store.md    # 便利店（鲜食/时段/客流）
│   ├── 05_community_retail.md     # 社区零售（复购/私域/O2O）
│   ├── 06_chain_retail_ops.md     # 泛连锁零售经营（同店/加盟商管理）
└── 📁 templates/                  # 交付物标准模板
    ├── prd_dictionary.md          # 需求文档与指标字典模板
    └── quick_bi_wireframe.md      # Quick BI 专属看板布局设计稿模板
```

🚀 如何使用这个 Skill 工作？
只需将 system_prompt.md 粘贴到你的大模型系统指令（System Instructions）中，当业务分析师对大模型说出请求时，例如：
分析师输入: "我是个业务数据分析师，我们需要做一个关于【零食量贩】行业的‘店长经营日报’看板，老板想要管控那些不赚钱的加盟商，并且抓住卖得不好的商品。帮我出一个方案。"
大模型就会根据上述结构，自动输出：
指导手册 (How-to Guide)：用券商和咨询顾问的语气，告诉他零食量贩的核心是看“极低毛利下的高周转和加盟商生命周期”，并且提醒数据清洗时要剔除“总部直营补贴”的干扰因素。
PRD+指标字典：输出精准的计算逻辑（如：SKU汰换率、单店盈亏平衡点预测计算）。
Quick BI 看板设计：给出包括全局过滤器、KPI卡片（日均GMV、缺货率）、留存分析图表、以及标红预警交叉表的详细布局方案。
