---
name: token-analyzer
description: 分析代币并给出评分与评价。基于代币经济模型、团队融资、市场表现、技术代码、社区氛围、链上数据及竞争优势进行 100 分制评分。适用于对特定加密货币（Token）进行深度尽职调查（DD）并输出标准化分析报告。
---

# Token Analyzer

## Overview

本 Skill 旨在为加密货币项目提供客观、基于数据的多维度评估。通过对 7 大维度（共 20 个细分项）的深度分析，输出一份包含汇总得分、评分依据、数据来源链接及总体评价的综合报告。

## Workflow

当用户请求分析某个代币（如 "分析 $ARB" 或 "分析 Arbitrum"）时，请遵循以下流程：

### Step 1: 基础信息收集 (Research)
使用 Google Search、CoinGecko、项目官网及文档收集以下信息：
- **代币合约地址**（多链需注明）
- **代币经济模型**：流通量、总供应量、持仓比例、解锁计划。
- **团队/融资**：创始团队背景、投资机构（VC）、融资总额及轮次。
- **市场**：上架交易所、交易深度、24小时成交量。
- **技术**：Github 仓库链接、最近提交频率、审计报告（CertiK, OpenZeppelin 等）。
- **社区**：X 关注人数、Discord/Telegram 活跃度、近期重大舆情。
- **链上**：持币地址数、大额转账趋势。

### Step 2: 评分 (Scoring)
参考 [scoring_rubric.md](references/scoring_rubric.md) 中的标准，为 20 个细分项分别打分（0-5分）。
- **严禁凭空捏造数据**。
- 如果信息不透明或无法获取（如团队未实名、代码未开源），根据“严厉惩罚”原则给 0 分或负分。
- **硬伤扣分**：如发现 Malicious Contract、Honeypot 等致命问题，直接在对应项给负分，总分底线为 0。

### Step 3: 生成报告 (Output)
使用 [report_template.md](assets/report_template.md) 作为输出模板：
1. **Summary Score**: 汇总所有项的得分。
2. **Score Breakdown**: 以表格形式列出每一项的得分及数据来源。
3. **Detailed Analysis**: 对每个大类给出详细的文字解释和证据链接。
4. **Overall Evaluation**: 结合得分给出最终投资风险/价值评价。

## Data Sources
优先从以下权威渠道获取数据并提供链接：
- **价格/市值/流通**: [CoinGecko](https://www.coingecko.com/), [CoinMarketCap](https://coinmarketcap.com/)
- **持仓/合约/链上**: [Etherscan](https://etherscan.io/), [BscScan](https://bscscan.com/), [Solscan](https://solscan.io/)
- **代码/开发**: [GitHub](https://github.com/)
- **团队/融资**: [Crunchbase](https://www.crunchbase.com/), [RootData](https://www.rootdata.com/), [CryptoRank](https://cryptorank.io/)
- **社区/舆情**: [X (Twitter)](https://twitter.com/), [LunarCrush](https://lunarcrush.com/)

## 示例请求
- "分析代币 $ETH 的经济模型和团队背景"
- "这个代币 $SOL 怎么样？帮我打个分"
- "深度调研并评分 PEPE 代币"

---
*注：本 Skill 仅提供数据分析，不作为财务建议。*
