---
license: apache-2.0
library_name: diffusers
tags:
- text-to-video
- wan-ai
- wan2.2
- anime
- nsfw
- unrestricted
not-for-all-audiences: true
---

# 🌌 Wan2.2-Anime-Unlimited (v0.1 Alpha)

<div align="center">

### The First Truly Open-Source, Unrestricted Anime Video Model
### 首个真正开源、无限制的二次元视频生成模型

<a href="https://ko-fi.com/xieshen2">
  <img src="https://img.shields.io/badge/Ko--fi-Support%20Me%20(Global)-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white" alt="Support on Ko-fi"/>
</a>
&nbsp;&nbsp;
<a href="https://afdian.com/a/233rrdou">
  <img src="https://img.shields.io/badge/爱发电-为我充电%20(China)-946CE6?style=for-the-badge&logo=electric&logoColor=white" alt="Support on Afdian"/>
</a>
<br><br>

[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Download%20Model-ffc107?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/你的用户名/你的模型仓库名)

<br>

**Based on Wan2.2-5B | Runs on 6GB VRAM | Uncensored**
**基于 Wan2.2-5B 架构 | 6GB 显存即可运行 | 无限制内容**

</div>

---

## 📢 Project Mission / 计划愿景

I am building the **ultimate open-source anime video generation model**. 
My goal is to fine-tune the Wan2.2 architecture on **50,000+ high-quality anime clips**, aiming for distinct art styles, intense battle scenes (like the *Fate* series), and pure anime aesthetics.

我正在打造**最完美、唯一的开源二次元视频大模型**。
我的最终目标是使用 **5万+** 高质量动漫素材进行全量微调，目标是实现 **720P分辨率、8秒时长** 的完美生成，专注于呈现如《Fate》系列般高质量的战斗场景与极致的动漫美学。

---

## 🚧 Current Status: v0.1 Alpha (Proof of Concept)

This is the first experimental release to prove the concept.
这是第一个实验性版本，用于验证可行性。

* **Base Model:** Wan2.2-5B (Optimized for consumer GPUs, runs on 6GB VRAM!)
* **Training Data:** 531 video clips (Small dataset for testing).
* **Resolution:** 480p/720p mixed.
* **Duration:** Currently optimized for **5 seconds**.
* **License:** Open Source / Unrestricted.

### ⚠️ Content Warning & Biases (模型偏好说明)

**This model is UNRESTRICTED / UNCENSORED.**
**本模型是无限制/无审查版本。**

Since v0.1 was trained on a small dataset (531 clips), it is **heavily biased** towards specific concepts present in the training data. Currently, it excels at and naturally leans towards:
由于 v0.1 仅使用了 531 个视频训练，模型权重目前严重偏向于训练集中的特定内容。当前版本最擅长（且倾向于）生成：

* **X-Ray views (内部透视/X射线)**
* **Mating Press / Compression interactions (特定体位/挤压感)**

*Please note: Future versions will generalize to a much broader range of anime actions and styles as we scale to 50,000 clips.*
*请注意：随着我们扩展到 5 万个素材，后续版本将支持更广泛、更通用的动漫动作和风格，而不仅限于上述内容。*

---

## 📚 Example Prompts & Dataset Previews (必看！提示词示例)

**Don't know how to prompt? Start here!**
**不知道怎么写提示词？先看这里！**

To help you get the best results, I have extracted representative frames and their corresponding prompts from the training data.
为了防止大家像无头苍蝇一样乱试 (Prevent random guessing)，我特意提取了训练集中的画面及其对应的提示词。

👉 **[Download the Demo Pack (ZIP)](https://huggingface.co/你的用户名/你的模型仓库名/resolve/main/demo_prompts.zip)** 👈
*(Click "Files and versions" if the link doesn't work, look for `demo_prompts.zip`)*

**How to use:**
1. Download and unzip the file.
2. Look at the images (`.jpg`) to find a style/action you like.
3. Open the matching text file (`.txt`) to see exactly how to prompt for it.
4. **Copy the tags/sentences into your generation tool.**

**使用方法：**
1. 下载并解压压缩包。
2. 浏览图片，找到你想要的效果。
3. 打开同名的 TXT 文件，复制里面的提示词。
4. 这样能保证 100% 还原模型原本的画风和动作！

---

## 🚀 Roadmap / 路线图

This is just the beginning. With your support, we can reach the final form:
这仅仅是个开始。在你们的支持下，我们将达成最终形态：

- [x] **v0.1 (Current):** Proof of concept with 531 clips, 5s generation.
- [ ] **v0.5 (Beta):** Scale to 5,000 clips, improve generalization, fix biases.
- [ ] **v1.0 (Final Goal):** **50,000 clips**, 720p Native, **8 Seconds** generation. Focus on "Sakuga" (high-quality animation) and battle aesthetics.

---

## 💰 Support the Development / 支持开发

Training a large-scale video model requires significant GPU resources. If you believe in an open, unrestricted anime model, please consider supporting the project!
训练大规模视频模型需要大量的显卡算力资源。如果你也期待一个完全开源、无限制的二次元模型诞生，请支持我！

**👇 Click below to donate directly / 点击下方直达赞助 👇**

### 🌍 Global Users (国外用户)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-Donate%20via%20PayPal%2FCards-FF5E5B?style=flat-square&logo=ko-fi&logoColor=white)](https://ko-fi.com/xieshen2)
> **https://ko-fi.com/xieshen2**

### 🇨🇳 Chinese Users (国内用户)
[![Afdian](https://img.shields.io/badge/爱发电-支持微信%2F支付宝-946CE6?style=flat-square&logo=bilibili&logoColor=white)](https://afdian.com/a/233rrdou)
> **https://afdian.com/a/233rrdou**

---
*Powered by the Open Source Community & Wan2.2*
