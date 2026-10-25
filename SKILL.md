---
name: shangsi-tujian
display_name: 上司图鉴
display_name_en: Boss Illustrated
description: 生成可离线打开的「上司图鉴」自测网页，十题情境测评从四个维度给上级出鉴定报告，单文件、数据不出本机。当用户说要做老板或上级性格测评、职场鉴定工具时触发。
description_zh: 生成可离线打开的「上司图鉴」自测网页，十题情境测评从四个维度给上级出鉴定报告，数据不出本机。
description_en: A single-file offline webpage that profiles your boss across four behavior dimensions through ten situational questions and renders an illustrated report, with all computation on-device.
category: productivity
version: 1.0.0
author: 番茄排骨
license: MIT
allowed-tools:
  - Read
  - Write
  - Edit
  - Bash
  - Glob
  - Grep
  - present_files
---

# 上司图鉴

一份能离线打开的单文件网页。十道职场情境题，从四个维度给上级出一份鉴定报告，顺便算算你一年要为他多花多少个工作日。全程在本机计算，不上传、不发任何请求。

## 这个 Skill 做什么

- **核心产物**：一份单文件 HTML（`assets/shangsi-tujian.html`），双击即可在浏览器打开，零外部依赖、可离线使用。
- **结构要点**：开场说明 → 十道情境题（点选即进下一题）→ 给上级起名窗口 → 海报式鉴定报告。报告含四维行为轴、八种原型画像、血压指数（绿/黄/红三档）、「他说·你回」话术、三年推演与保命清单。
- **数据边界**：全部计算在浏览器端完成，不联网、不上传任何数据；上级姓名只存在本机 `localStorage`；结果可通过 URL hash 还原答案分享，链接不含任何个人信息。

## 何时使用

- 用户说「想做个老板 / 上级性格测评」「生成职场鉴定工具」「我要这个测评网页」。
- 用户想把这个网页发给同事、嵌进文章或自己的产品。

## 如何使用（给智能体的工作流）

1. 把 `assets/shangsi-tujian.html` 复制到用户当前工作区（默认文件名 `shangsi-tujian.html`）。
2. 用 `present_files` 打开预览，让用户直接使用。
3. 若用户要改题、改色、改文案或导出图片，在本文件同目录的文档或代码基础上调整。

## 说明与免责

- 这是基于通用职场行为方法论设计的**自评 / 自测工具**，不是标准化心理量表，未做信效度检验，不做临床诊断。
- 全部计算在本地浏览器完成，不联网、不上传。
