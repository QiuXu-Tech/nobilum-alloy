# Nobilum Alloy｜合金

Nobilum Alloy 研究面向模块 Agent 的专用语言模型，探索多教师概率蒸馏、跨模型知识迁移、模型结构调整与有限算力下的训练方法。

**本仓库用于公开部分研究成果。目前不对 Alloy 的开源范围、时间表或后续发布作任何承诺。**

## 当前方向

当前首个目标模型为 **Nobilum Alloy Files v1.0**，面向 Nobilum Forge 的 Files 模块 Agent。此前的前端 UI 专用模型方向属于早期探索，不再代表当前首模目标。

命名遵循 **Alloy + 对应模块 Agent 名称 + 版本号**，完整品牌名加 Nobilum 前缀。目标名称中的 v1.0 是研发目标标识，不代表已有正式发布的模型。

截至 **2026-11-11**，项目已开展小规模真实模型前后向、训练更新、保存与新进程重载试验，后续训练对照与质量验证仍在推进。这些工程进展不等于教师优势、结构改造收益或模型整体能力已获证明。本仓库尚未发布 Alloy 模型权重、完整训练实现或数据集。

## 研究重点

- **多教师概率蒸馏**：研究如何利用教师 next-token 概率分布，而非仅使用生成文本。
- **跨模型对齐**：处理不同 tokenizer、词表与输出位置之间的差异。
- **模型结构调整**：通过消融、裁剪与恢复训练验证结构选择，不预设可直接删除的语义功能分区。
- **有限算力训练**：比较 GPU 常驻与 CPU 协作的资源代价，分别检查数值一致性、显存和耗时。
- **独立质量验证**：区分工程运行成功、开发集观察和独立能力结论，保留失败及未完成结果。

这些是研究方向，不构成已验证能力清单。

## 已公开内容

| 内容 | 范围 |
|---|---|
| [CPU 激活卸载最小实机探针](docs/research/2026-11-10-resource-probe.md) | 一个短输入下的资源与梯度对照摘要；非模型质量评测 |
| [研究成果公开政策](PUBLICATION_POLICY.md) | 公开边界、开源承诺与许可说明 |

公开内容以仓库中实际存在的材料为准。当前发布的是经过整理的研究摘要，不是完整研发工作区。

## 许可

仓库保留已有的 [Apache License 2.0](LICENSE)，适用于本仓库中有权按该许可证提供、且未另行标注的原创公开内容。第三方材料遵循各自许可；仓库许可证不覆盖未公开的代码、模型、数据或其他内部成果，也不构成未来公开这些内容的承诺。

## English summary

Nobilum Alloy studies language models specialized for module agents, including multi-teacher probability distillation, cross-tokenizer alignment, model restructuring, and resource-constrained training. The current first model target is **Nobilum Alloy Files v1.0**, for the Files module agent in Nobilum Forge.

This repository shares **selected research findings**. We make **no commitment to an open-source scope, timetable, or future release**. Small-scale real-model experiments are underway; this repository does not currently provide Alloy model weights, a complete training implementation, or a dataset. Published resource measurements are limited to their stated experimental conditions and are not model-quality claims.
