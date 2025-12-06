# DSSpec
EN: A formal specification defining the minimal computable structure for AI-native decision systems.  
CN: 定义 AI 原生决策系统最小可计算结构的形式化规范。

---

# Decision Space Specification (DSSpec)
# 决策空间规范（DSSpec）

Version 0.4 — Early Draft
0.4 版 —— 初始草案

## Overview
## 概述

DSSpec defines the minimal semantic structure a system must expose to become AI-native: interpretable, composable, and capable of real decision collaboration with agents.
DSSpec 定义了一个系统要成为 AI 原生、可解释、可组合、并能与智能体协同决策所必须暴露的最小语义结构。

Traditional digital systems expose data and workflows.
AI-native systems must expose decision semantics.
传统数字化系统暴露的是数据和流程。
AI 原生系统必须暴露的是 决策语义。

This repository contains the evolving draft of DSSpec, version history, and reference directions for future implementations.
本仓库包含 DSSpec 的演化草案、版本历史，以及未来实现方向的参考结构。

DSSpec is not a final standard. It is a foundation that will evolve rapidly with contributions from researchers, engineers, designers, and domain experts.
DSSpec 不是最终标准，而是一个将在研究者、工程师、设计师和行业专家共同推动下快速演化的基础。

---

## Vision
## 愿景

Systems of the future must be understandable by AI.
To do that, they must expose structured decision semantics, not just data.
未来的系统必须能够被 AI 理解。
为了做到这一点，它们必须暴露结构化的决策语义，而不仅仅是数据。

DSSpec aims to build a shared decision language across industries, enabling humans, AI agents, and digital systems to understand decisions in the same structured way.
DSSpec 致力于构建跨行业的共享决策语言，使人类、AI 智能体和数字系统能够以同一种结构化方式理解决策。

This specification is an early step toward AI-deployable, interoperable decision ecosystems grounded in computable reasoning.
该规范是迈向可由 AI 部署、可互操作，并基于可计算推理的下一代决策生态的早期步骤。

---

## Motivation
## 动机

For decades, digital systems were designed around data—not decisions.
数十年来，数字系统都是围绕数据构建的——而不是围绕决策。

This led to:
这导致了：
- siloed systems
  系统割裂
- no shared reasoning semantics
  缺乏统一推理语义
- opaque business logic
  业务逻辑不透明
- expensive integrations
  对接成本高昂

AI therefore is unable to collaborate meaningfully
AI 因此无法与业务进行有效协作

AI is forcing a paradigm shift
AI 正在推动范式转变。

To integrate AI into real-world processes, systems must reveal:
为了让 AI 进入真实业务流程，系统必须暴露：
- what matters (Ontology, Events, Indicators)
  重要的是什么（本体、事件、指标）
- what constraints exist (C)
  有哪些约束（C）
- what options are possible (P)
  有哪些可行路径（P）
- how trade-offs are evaluated (V)
  取舍如何评估（V）

DSSpec provides the missing semantic layer between enterprise systems and AI reasoning.
DSSpec 提供了企业系统与 AI 推理之间缺失的语义层。

---

## Why DSSpec? A Short Story
## 为什么需要 DSSpec？（一个简短故事）

Imagine a hospital deciding whether to purchase a new CT machine.
想象一家医院要决定是否购买一台新的 CT 设备。

Different systems know different fragments of the world:
不同系统掌握着世界的不同碎片：
- Asset system → existing inventory
  资产系统 → 当前设备
- Maintenance system → failure history
  维修系统 → 故障历史
- Finance system → available budget
  财务系统 → 可用预算
- Clinical system → patient demand
  临床系统 → 病患需求

Yet no system can answer:
但没有系统能回答：

> “Given constraints and values, what should we do?
> What options exist, and which is best?”
> “在所有约束和价值偏好下，我们该怎么做？
> 有哪些方案？哪一个最好？”

Because systems expose data—not decisions.
因为系统暴露的是数据，而不是决策。

---

## With DSSpec
## 有了 DSSpec

Each system exposes its fragment of the Decision Space:
每个系统都会暴露自己的决策空间片段：
- O — relevant entities
  O — 相关实体
- E — events defining state changes
  E — 状态变化事件
- I — computable indicators
  I — 可计算指标
- C — feasibility constraints
  C — 可行性约束
- P — possible paths
  P — 可选路径
- V — value functions
  V — 价值函数

The AI agent can assemble a complete DS and answer transparently:
AI 智能体可以组装完整的 DS，并透明地回答：

- What options exist?
  有哪些方案？
- Which paths are infeasible and why?
  哪些不可行，为什么？
- How do trade-offs shift under different value preferences?
  在不同价值偏好下决策如何变化？
- What assumptions were used?
  使用了哪些假设？
  
**Systems stop being data islands and become decision-ready components.**
**系统不再是数据孤岛，而成为可决策组件。**

---
## What DSSpec Defines
## DSSpec 定义的内容

DSSpec formalizes the structure of a Decision Space:
DSSpec 形式化定义决策空间结构：

<p style="text-align:center">𝐷𝑆 =(𝑂,𝐸,𝐼,𝐶,𝑃,𝑉)</p>
<p style="text-align:center">DS=(O,E,I,C,P,V)</p>

Including:
包括：
- Query → Perspective → Domain projection
  Query → 视角 → 领域的投影过程
- Factor extraction (Ontology, Events, Indicators, Constraints)
  因子抽取（本体、事件、指标、约束）
- Path generation & pruning
  路径生成与剪枝
- Value function modeling
  价值函数建模
- Multi-agent coupling rules
  多智能体耦合规则

---

## Relationship to Paper & Implementation
## 与论文及工程实现的关系

  ‘’Decision Space Theory (paper)
        ↓ formalizes why
  DSSpec (this repository)
        ↓ defines how
  Cognito-OS (planning, reference implementation)
        ↓ shows what it looks like in practice‘’

  ‘’决策空间理论（论文）
        ↓ 奠定“为什么”
  DSSpec（本仓库）
        ↓ 定义“如何做”
  Cognito-OS（计划中，参考实现）
        ↓ 展示“实际长什么样”‘’


---

## Draft Specification
## 草案文档

Latest Draft (Feishu):https://ai.feishu.cn/wiki/A6rKwRLhGi0WSekwkPMc5Ke1nCe
最新草案（飞书）：（中文版暂无）

Archived versions will be added under /spec/ as the draft stabilizes.
草案稳定后将发布在 /spec/ 目录下的版本快照中。

---

## Planned Directory Structure
## 计划目录结构

  ‘’/spec/
    ├── v0.2.md
    ├── v0.3.md (Perspective)
    ├── v0.4.md (Multi-Agent)

  /schemas/
    ├── ds.json
    ├── domain.json
    ├── factor.json
    ├── perspective.json

  /examples/
    ├── medical_procurement.json
    ├── manufacturing_risk.json

  /reference/
    ├── glossary.md
    ├── constraints.md
    ├── principles.md‘’

---

## Versioning
## 版本管理

DSSpec follows a flexible semantic versioning model:
DSSpec 采用灵活的语义化版本模型：
- v0.x — conceptual stabilization
  v0.x — 概念稳定化阶段
- v1.0 — first coherent formal specification
  v1.0 — 第一份完整的正式规范
- v1.x+ — extensions and domain packs
  v1.x+ — 扩展与行业包
- v2.0 — potential standardization track
  v2.0 — 潜在标准化路径

All updates are documented in CHANGELOG.md.
所有更新记录在 CHANGELOG.md 中。

---

## Roadmap
## 路线图

v0.6 — Formal semantics of Perspective
v0.6 — 视角的形式语义

v0.7 — Multi-Agent decision coupling
v0.7 — 多智能体决策耦合

v1.0 — Complete auditable specification
v1.0 — 完整可审查规范

---

## Contact
## 联系方式

Email: chenshancscs@gmail.com
X: @Shan_AiNote
Medium: Shan_AiNote


