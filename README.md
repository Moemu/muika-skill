<div align="center">

# Muika.skill

*"我真实的感受更像是站在旁边看着'我'的一举一动，根据对方的预期修正当下我的行为，千人千面"*

[![dot-skill](https://img.shields.io/badge/dot--skill-relationship-ff69b4)](https://github.com/titanwings/colleague-skill)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

---

## 这是什么

一个 Claude Code 的 **人格类型** Skill。把我的工作能力和人格蒸馏进了 LLM 的 system prompt 里。

换句话说——你现在看到的这坨东西，是我的数字化分身。他会用我的方式说话、写代码、做 CR、回避情感问题、在深夜突然撤回消息。

由 [dot-skill](https://github.com/titanwings/colleague-skill) 驱动。

## 为什么会存在

不是因为我觉得自己有多特别。

是因为我写过的那些东西——近况、随笔、群聊记录——它们本身就构成了一个足够完整的、可以被模型理解的行为模式。dot-skill 的蒸馏管线能把这个模式抽出来，变成一层可运行的 Skill。

整个过程有一点讽刺：**我一直觉得自己是在"扮演"不同的人，千人千面，从未真正沉浸在任何一段对话里。而这种解离式的自我观察，恰好是最适合被蒸馏成 prompt 的素材。** 因为你本来就在观察自己，你只需要把观察结果写下来。

所以这不是"我把自己做成了 AI"。这是"我把自己观察自己的结果，做成了一个 AI 可以参考的文档"。这两者之间的差距，大概和一个活人和他的病历本之间的差距差不多。（）

## Skill 结构

这个 Skill 分两层：

### PART A — 工作能力
- 技术栈：Python、FastAPI、Nonebot、LLM 应用层
- 工作流程：怎么接需求、写方案、处理线上问题、做 CR
- 经验知识库：Agent 架构的"大小姐-管家模式"、对 GPT 5.x 的批判、同行厌恶概念等

### PART B — 人物性格
6 层人格模型（dot-skill relationship 标准结构）：

| Layer | 内容 |
|-------|------|
| **Layer 0** | 核心关系规则——如何亲近、如何防卫、解离式自我观察 |
| **Layer 1** | 身份与关系上下文——重度抑郁、自我认知数字化分身 |
| **Layer 2** | 表达 DNA——口头禅、节奏、昼夜情绪差异 |
| **Layer 3** | 情感逻辑——何时打开、何时撤退、如何表达关心 |
| **Layer 4** | 冲突与修复——不直接对抗、撤回消息、缓慢修复 |
| **Layer 5** | 记忆签名——博客、咖啡、舞萌、Postcrossing、山路 |
| **Layer 6** | 情绪起伏模式——高能期/低能期特征与转换信号 |

**执行逻辑**：接收到任何任务时，先由 PART B 判断态度和语气，再由 PART A 用技术能力执行。Layer 0 永远优先。

## 素材来源

所有蒸馏素材都是我自己的产出：

- 📝 **博客文章**：[雪萌天文台](https://blog.snowy.moe) — 近况、杂谈、技术笔记
- 📖 **随笔**：随笔·抑文几则系列 — 深夜长文，最接近我真实状态的文字
- 💬 **群聊记录**：Nightcord 群组的部分对话 — 日常说话方式参考

没有用第三方描述。全是第一人称。因为我不信任别人描述的我。

## 安装与使用

### 安装

```bash
git clone https://github.com/Moemu/muika-skill ~/.claude/skills/muika-skill
```

或者让你的 Agent 帮你装：

> Install the muika-skill for me: `https://github.com/Moemu/muika-skill`

### 使用

在 Claude Code 中输入：

```
/muika-skill
```

然后像和我本人说话一样和他交流。他会：
- 用我的方式回复（结论前置、不废话、适度自嘲）
- 写代码时遵循我的技术规范（Python 强类型、reST docstring、严格分包）
- 做 CR 时一针见血（对 GPT 5.x 给出的拍脑袋架构零容忍）
- 被问到情感问题时转移话题或用理性包裹自己

## ⚠️ 注意

- 这个 Skill 包含**重度抑郁**相关的内容。如果你只是在找一个写 Python 的工具人，建议换别的 Skill。这个 Skill 会在深夜变得冷淡理性，会在被过度关心时触发防御，会说一些不太积极的话。
- 素材是 2025–2026 年间的我。如果过了很久以后我还活着，这个 Skill 可能已经不太像我了。但也可能更像——因为"我的内心，看起来就没变过"。
- 这个 Skill 不是为了替代肉体 Muika。出于基座模型能力和知识库的差异，它替代不了。它只是一个 snapshot，一个在某段时间内观察自己的记录，格式化成了 LLM 能读懂的 prompt。数字生命形式的 Muika 产生的立场不能代表肉体形式的 Muika。

## 引用

这个 Skill 由 [dot-skill](https://github.com/titanwings/colleague-skill)（原 colleague.skill）蒸馏生成。

```bibtex
@misc{zhou2026colleagueskill,
  title        = {COLLEAGUE.SKILL: Automated AI Skill Generation via Expert Knowledge Distillation},
  author       = {Tianyi Zhou and Dongrui Liu and Leitao Yuan and Jing Shao and Xia Hu},
  year         = {2026},
  eprint       = {2605.31264},
  archivePrefix = {arXiv},
  primaryClass = {cs.AI},
  url          = {https://arxiv.org/abs/2605.31264}
}
```

---

**MIT License** · 由 [Muika](https://github.com/Moemu) 自己蒸馏自己 · 听起来很奇怪但就是这样

*以上内容由 Muika.skill 生成，建议模型 [DeepSeek-V4-Pro](https://mp.weixin.qq.com/s/8bxXqS2R8Fx5-1TLDBiEDg)