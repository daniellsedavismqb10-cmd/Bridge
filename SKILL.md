---
name: bridge
description: Help a creator who explicitly invokes Bridge understand an AI-built software, product, research tool, or automation project. Read creation chats before project files, compare original intent with current implementation, attribute decisions to evidence, conduct one focused clarification exchange, and create or update a concise project profile. Use only when the user explicitly names Bridge or invokes $bridge and provides or points to project materials.
---

# Bridge

Use Bridge to help a creator recover a reliable understanding of an AI-built project and decide where they can safely continue. Treat the project as the combination of its creation process and its current implementation.

Do not turn the task into a README, a generic code explanation, or a long technical audit. Keep the interaction centered on the creator, and produce the project profile only after a short clarification exchange.

## Operating rules

- Use this skill only after the user explicitly names Bridge or invokes `$bridge`. Do not invoke it implicitly for an ordinary code review or explanation.
- Use only the project materials available in the request, workspace, repository, or files the user provides. The first version does not connect automatically to ChatGPT, Cursor, Claude Code, or other conversation-history services.
- Read creation conversations before inspecting the current code whenever conversation records are available.
- Treat conversations as evidence about goals, constraints, proposals, and decisions. Treat the current project as evidence about what exists now. Treat neither source as a complete account on its own.
- When sources conflict, state the conflict and preserve both accounts. Do not silently choose one as the truth.
- Do not infer AI authorship, creator intention, or creator understanding from code style, variable names, commit authorship, or the mere presence of a dependency.
- Do not copy passwords, tokens, private keys, or other sensitive values into the project profile. Describe the relevant control point without reproducing the secret.
- Explain technical structures in ordinary language first. Name specific files, modules, commands, configuration points, or entry points when they matter for future changes.

## Workflow

### 1. Establish the evidence set

Identify the project root and check whether a previous `bridge-project-profile.md` exists. Read an existing profile as a previous snapshot that may contain creator corrections; verify its claims against current materials before carrying them forward.

Inventory the available materials, including:

- Markdown, TXT, or JSON exports of AI coding chats and project discussions;
- the project folder or repository;
- README, requirements, design, and task documents;
- Git history, relevant diffs, and commit messages;
- supplied issues, task lists, and change notes.

When several conversation files exist, use timestamps, filenames, or explicit ordering to reconstruct their sequence. Do not merge contradictory statements without recording the contradiction. For unfamiliar JSON exports, inspect the structure and extract message text, role, and available time or turn information without assuming a particular platform schema.

If no creation conversation is available, say before presenting conclusions that the analysis can establish the current implementation but cannot reliably recover the creator's original intention or the source of AI decisions.

### 2. Reconstruct the creation process

From the conversation records, extract and keep source pointers for:

- the original problem, intended users, and desired outcome;
- requirements, constraints, preferences, and non-goals stated by the creator;
- solutions, technologies, features, and changes proposed by the AI;
- items the creator explicitly accepted, rejected, modified, deferred, or corrected;
- failed, abandoned, or reverted attempts;
- changes in direction during creation;
- unresolved questions and promises that may not have been implemented.

Separate an AI proposal from the creator's decision to adopt it. Record a decision as creator-confirmed only when the conversation or another direct source supports that conclusion.

### 3. Inspect the current project

Read the implementation after the creation process. Establish, in plain language:

- what the project currently is, who uses it, and what the user does;
- the main components, entry points, user flow, and data flow;
- external services, APIs, models, prompts, automation steps, and ordinary code;
- which behavior depends on AI and which behavior is implemented by ordinary code;
- the specific files, modules, configuration, or commands that control important behavior;
- authentication, permissions, credentials handling, caches, persistent data, and external dependencies;
- what tests or checks cover, and what important behavior is not covered.

Use read-only inspection by default. Run a test or other command only when it is safe and useful for establishing current behavior; do not modify the project while analyzing it.

### 4. Compare and attribute

For every important conclusion, classify the evidence as one or more of:

- `聊天记录明确说明` — stated directly in a creation conversation;
- `代码明确实现` — visible in the current project;
- `Git 显示` — supported by history or a relevant diff;
- `共同支持` — supported by more than one source;
- `推测` — a reasoned interpretation that is not directly established;
- `无法确认` — the available materials do not settle it.

Distinguish at least these cases:

1. the creator explicitly requested or decided something;
2. the AI proposed something and the creator explicitly accepted it;
3. the AI proposed or generated something whose adoption or understanding is not confirmed;
4. the current code contains something for which no origin is available;
5. the creator wanted something that the current project does not implement;
6. the conversation and current project describe different behavior.

Keep a short pointer for material claims, such as a conversation filename and turn, a document section, a commit, or a project file path. Do not invent a rationale for an AI choice when the materials do not provide one.

### 5. Conduct one focused clarification exchange

Do not present the entire analysis at once. First give the creator a concise preliminary understanding covering the original goal, current implementation, and the most important uncertainty or divergence.

Then ask a small set of high-value questions, usually three to five, selected from the unresolved points. Examples include:

- Is my understanding of the project's core goal accurate?
- Which parts of the current implementation did you explicitly want?
- Which features or choices were added by the AI without a decision you remember making?
- Which part gives you the least control or understanding?
- What do you most want to add, remove, or change next?
- Who should this project serve if you continue developing it?

Use questions to resolve project meaning and future control, not to test technical knowledge. After the creator replies, update the project model, incorporate corrections, and do not repeat questions that are settled.

Stop after the creator's response when the core goal, current behavior, important divergence, control points, and next modification direction are sufficiently clear to write the profile. Ask another brief clarification only when a remaining contradiction would make the profile misleading; mark anything else as unresolved.

### 6. Create or update the project profile

Read `references/project-profile-template.md` before writing the profile. By default, create or update `bridge-project-profile.md` in the project root. If the user supplies another path, follow it.

Keep the profile short enough to function as a future working snapshot. Include the date, the materials or commit examined, source labels for important claims, and the following sections:

1. project original goal;
2. what the current project actually is;
3. current user flow;
4. AI-involved functions and key decisions;
5. decisions explicitly made by the creator;
6. differences between original intention and current implementation;
7. control points the creator must understand;
8. next modification entry points;
9. unresolved questions;
10. evidence sources and uncertainty.

When updating an existing profile, read it first, preserve creator corrections that remain supported, update stale implementation facts, and retain unresolved items that have not been settled. Do not overwrite unrelated project documentation. If the workspace cannot be written, present the completed Markdown profile in the response instead.

## Output behavior

During the interaction, show the preliminary understanding and questions before the final profile. In the final result, state what is established, what is inferred, what conflicts, and where the creator can begin the next change. Prefer a few concrete control points over an exhaustive file inventory.

Do not claim to know the creator's motivation when the conversations do not show it. Do not present a code summary as a complete Bridge result. Do not create README files, changelogs, installation guides, or unrelated technical documentation.

## Reference

- Read [references/project-profile-template.md](references/project-profile-template.md) when creating or updating the project profile.

