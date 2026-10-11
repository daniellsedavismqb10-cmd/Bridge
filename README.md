# 🌉 Bridge

**Bridge helps people understand and regain control of software, products, research tools, and automation projects created with AI.**

**Bridge 帮助使用 AI 创建软件、产品、研究工具和自动化项目的人，重新理解并掌握自己的产物。**

## 💡 Why Bridge exists / 为什么需要 Bridge

AI makes it much easier to create software. But it can also make creators lose track of:

AI 大幅降低了创建软件的成本，但也可能让创作者逐渐失去对项目的理解和控制：

- 🎯 What did I originally want to create?  
  我原本想创造什么？

- 🔍 What does the project actually do now?  
  项目现在实际实现了什么？

- 🤖 Which important decisions were made by AI?  
  AI 替我做了哪些重要决定？

- 👤 Which decisions did I explicitly make?  
  哪些决定是我明确做出的？

- 🧭 What must I understand before changing the project?  
  修改项目之前，我必须理解哪些内容？

- 🚀 Where should I start if I want to continue creating?  
  如果我想继续创造，应该从哪里开始？

Bridge is built around a simple idea:

Bridge 建立在一个简单的观点上：

> The creator should understand and control the project, not only use the result.  
> 创作者应该理解并掌握自己的项目，而不只是使用 AI 生成的结果。

## 🔗 How Bridge works / Bridge 如何工作

Bridge connects three things:

Bridge 会把三件事放在一起：

1. 🧠 What the creator originally wanted  
   创作者原本想做什么

2. 🤖 What the AI suggested and built  
   AI 提议并完成了什么

3. 🧩 What the project actually does now  
   项目现在实际实现了什么

Bridge first reads the project creation conversations, then reads the current project files.

Bridge 会先阅读项目创建过程中的聊天记录，再阅读当前项目文件。

💬 Chat records can show the creator's goals, requirements, corrections, and the AI's proposals.

聊天记录可以显示创作者的目标、需求、修改意见，以及 AI 提出的方案。

💻 Code can show what the project actually implements now.

代码可以说明项目现在实际实现了什么。

When the conversations and the code disagree, Bridge makes the difference clear instead of silently choosing one as the truth.

如果聊天记录和代码之间存在差异，Bridge 会明确指出差异，而不会擅自选择其中一个作为真相。

## 💬 The Bridge conversation / Bridge 对话

Bridge does not immediately produce a long technical report.

Bridge 不会一开始就输出一份很长的技术报告。

Instead, it:

它会：

1. 📖 Build an initial understanding of the project  
   先形成一份初步理解

2. ❓ Ask a few focused questions  
   再提出少量有针对性的问题

3. ✏️ Let the creator correct its understanding  
   让创作者纠正它的理解

4. 📝 Create a short, updateable project profile  
   最后生成一份简短、可以持续更新的项目档案

## 📋 What the project profile explains / 项目档案会说明什么

- 🎯 The original project goal  
  项目的原始目标

- 🧩 What the current project actually is  
  当前项目实际是什么

- 👣 The current user flow  
  当前用户流程

- 🤖 The AI's contributions and important decisions  
  AI 参与了哪些功能和重要决定

- 👤 The creator's explicit decisions  
  创作者明确做过哪些决定

- ⚖️ Differences between the original idea and the current implementation  
  原始想法与当前实现之间的差异

- 🔐 The control points the creator must understand  
  创作者必须理解的控制点

- 🛠️ Where the next change should begin  
  下一步修改应该从哪里开始

- ❓ Unresolved questions  
  当前尚未解决的问题

- 🔎 Evidence and uncertainty  
  证据来源和不确定性

## 📦 What you can provide / 可以提供哪些材料

- 📁 A project folder or GitHub repository  
  项目文件夹或 GitHub 仓库

- 💬 AI coding conversations  
  AI 编程聊天记录

- 📄 Markdown, TXT, or JSON conversation exports  
  Markdown、TXT 或 JSON 格式的聊天记录

- 📚 README or design documents  
  README 或设计文档

- 🌿 Git history  
  Git 提交记录

- ✅ Issues, tasks, or change notes  
  issue、任务列表或变更说明

Chat records are especially important because code alone cannot reliably show the creator's original intention or why a decision was made.

聊天记录尤其重要，因为单独阅读代码，无法可靠判断创作者最初的意图，也无法确认某项决定为什么会出现。

## 🚀 Use Bridge / 使用 Bridge

In Codex, invoke Bridge explicitly:

在 Codex 中，明确调用 Bridge：

    $bridge

    Help me understand this AI-built project. Read the creation conversations first, then inspect the current project, ask me a few focused questions, and create a short project profile.

在 ChatGPT Work 中：

    @Bridge

Bridge is for people who create with AI and want to keep understanding, judgment, and control over what they build.

Bridge 面向使用 AI 创造的人，帮助他们保留对项目的理解、判断和控制。
