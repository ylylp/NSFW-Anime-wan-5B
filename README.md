# Wan2.2 Anime Video — 3.0Pro / 动漫视频微调项目

个人动漫视频模型微调实践与后续动作生成研究。长期关注动漫画面表现、复杂动作与时序连续性；下一阶段将围绕**动漫战斗、高速运动、肢体结构与运动模糊**开展专项研究。

[模型权重与下载](https://huggingface.co/yaleiyaleichiling/NSFW-Anime-wan-5B) · [GitHub 项目](https://github.com/ylylp/NSFW-Anime-wan-5B)

## 已完成：Wan2.2-5B 微调实践

基于 [Wan2.2-TI2V-5B](https://huggingface.co/Wan-AI/Wan2.2-TI2V-5B) 的旧项目约于 **2026 年 1 月完成**，使用**单卡 NVIDIA RTX PRO 6000 级别 GPU**，进行了约**三个月的训练与迭代**。**3.0Pro 为该阶段最终版本**，现保留权重并恢复项目档案。

这一阶段积累了视频模型持续训练、参数调整、权重保存和生成效果评估的实践经验。训练涉及动漫视频的特定内容与风格，包含成人向专项实验。作者观察到部分目标场景有所改善，但综合画质、结构与时序表现仍受底模能力限制。动漫战斗与高速运动是后续研究方向，目前尚无可验证的旧模型战斗能力提升结论。

原 Hugging Face 仓库曾删除，本次依据保留文件与历史材料恢复，作为后续算力申请的既往实践参考。训练持续时间、硬件及完成时间依据作者回顾记录；原始训练配置、步数、优化器状态及 loss 日志尚未恢复。具体微调方法仍待历史文件确认。

## 新阶段：Anime Video Motion Fine-Tuning Research

计划转向海螺 H3 等视频模型，重点研究：

- 动漫高速运动与复杂战斗动作的生成表现。
- 肢体结构稳定性、运动模糊和跨帧动作连续性。
- LoRA、部分层微调、BAdam 与全参数微调等方法的适配及效果比较。

**已为新项目准备约 20,000 条动漫视频数据**（作者提供的数据准备规模）。计划先完成训练流程验证，再开展专项实验与固定条件对比。实际训练规模、评测结论及数据授权情况将随研究进展记录。

当前个人算力不足，正在寻求面向独立开发者的算力支持：

| 资源 | 申请需求 |
| --- | --- |
| GPU | 初始 2 张，理想 4 张 RTX PRO 6000 96GB 或同等级显卡 |
| 时间 | 约 30 天；资源预算为 1,440–2,880 GPU 小时 |
| 环境 | SSH、CUDA/PyTorch、多卡训练及持久化存储 |

希望在已有实践基础上形成更好的动漫视频模型、可复核的实验记录和公开技术资料。目标模型具体版本、许可与训练支持需在实施前核实；成果公开范围依据底模许可证、数据授权和资助方要求确定。

## 3.0Pro 权重与推理

| 项目 | 已检查结果 |
| --- | --- |
| 文件 | `3.0Pro.safetensors` |
| 大小 | 9,999,658,848 字节 |
| 参数元素数 | 4,999,787,712 |
| 精度与张量 | FP16，825 个张量 |
| 主体结构 | 30 个 Transformer block，隐藏维度 3072，输入通道 48 |
| 文件读取 | 所有张量可通过 safetensors 读取，未发现 NaN 或 Inf |

SHA-256：

```text
69299be08b667a6a8b6d1a02727afd8e31a87a47daf508e1addec6b6dab83acf
```

该文件为完整扩散主模型权重形式，具体训练方法不能由导出形式确定。ComfyUI 中分别加载：

- `models/diffusion_models/3.0Pro.safetensors`
- `models/text_encoders/umt5_xxl_fp16.safetensors`
- `models/vae/wan2.2_vae.safetensors`

已有本地 Wan2.2 5B 工作流引用上述三个文件。辅助模型从其授权来源获取。本次恢复完成了文件检查，端到端 GPU 推理仍待重新验证；40 步、CFG 5、UniPC 为已有工作流的推理设置。

## 历史记录

GitHub 提交历史保留了早期 v0.1 说明。作者另保留 2026 年 1 月的社区格式转换需求留言，作为历史互动线索。早期版本数据量不直接代表 3.0Pro 的训练规模，现有材料也不构成量化性能评测。

## 使用范围与许可

旧版 3.0Pro 权重具有成人向（NSFW）内容偏向，仅供成年人合法合规使用，普通提示也可能生成不适合所有受众的内容。公开项目页与算力申请材料仅展示技术信息和适宜公开的研究内容。

底模与历史仓库标注 Apache-2.0，本归档沿用该许可并保留 LICENSE。使用与再分发应遵守适用许可及第三方权利要求。

## English overview

A personal anime-video fine-tuning project based on Wan2.2-TI2V-5B, completed around January 2026 after approximately three months of training and iteration on a single RTX PRO 6000-class GPU, according to the author's records. 3.0Pro is the final checkpoint of this phase and includes adult-oriented specialization. The next research phase focuses on anime combat motion, anatomical stability, motion blur and temporal continuity, with approximately 20,000 prepared clips. Compute sponsorship is sought for this future work; no verified combat-quality improvement is claimed for the archived model. Release scope depends on applicable licenses and dataset rights.

## 支持研究

[Ko-fi](https://ko-fi.com/xieshen2) · [爱发电](https://afdian.com/a/233rrdou)
