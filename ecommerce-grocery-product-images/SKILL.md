---
name: ecommerce-grocery-product-images
description: Use when planning or generating a six-image 1:1 e-commerce product set from real grocery, fruit, vegetable, or food-product photographs.
---

# 电商果蔬食品商品图

根据用户提供的真实商品实拍，规划并生成六张独立的 1:1 电商商品图。目标是通过专业摄影级整理和适度优化呈现真实商品，保持商品身份、核心结构、材质、颜色和实拍质感。

## 执行原则

1. 先判断商品类型、实拍能证明的商品事实、可修整问题，以及当前图片属于常规商品图还是明确要求的场景图。
2. 按优先级处理：商品身份正确 > 实拍级真实感 > 核心特征保持 > 必要美化 > 摄影表现 > 美观。真实性与美观冲突时保留真实性。
3. 根据当前图号读取 [六图任务规范](references/six-image-plan.md)，制定该张唯一且具体的方案。六张图承担不同信息任务，不重复表达。
4. 写 Prompt 前读取 [四段提示词框架](references/prompt-framework.md) 和相关的 [真实性与修整边界](references/product-fidelity-and-retouch.md)、[摄影与构图规则](references/composition-lighting.md)。生成后按 [质检与返工规则](references/quality-and-retry.md) 检查。
5. 最终发送给生图模型的 Prompt 必须为四个紧凑自然语言段落：商品真实基准、本张拍摄方案、摄影与商业优化、真实性与失败约束。只发送已确定的一套执行方案，不附候选方案，不发送 Skill 原文。
6. 按用户当前请求交付方案、Prompt 或图片。按当前图号检查结果并依照质检规则返工；只有用户要求整套六图时才连续处理后续图。单张任务完成后停止当前任务。

## 固定要求

- 输出单张、独立的 1:1 图；六张图不能拼成一张图。
- 商品数量、品种、包装身份和实拍支持的特征不得擅自改变。
- 构图按原图状态和当前图任务决定：原构图合适时沿用并优化；不适合时可重新整理构图与摆放，同时保持商品身份、数量和真实形态。
- 01、02、03、06 默认采用简洁商业摄影棚逻辑；04、05 采用真实使用场景逻辑。场景光和摄影棚布光不可混用。
- 每张图的提示词只写本次允许的具体修整，以及本图最关键的失败约束。
