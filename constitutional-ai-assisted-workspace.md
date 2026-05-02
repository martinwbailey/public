# A Constitutional Approach To Setting Up An AI-Assisted Workspace

## Executive Summary

Many people first encounter AI through simple chatbots. That experience is useful, but it is also fragile: the conversation is temporary, context is easily lost, and important knowledge can remain trapped in a chat window.

A constitutional AI-assisted workspace is a different pattern. It treats a folder or repository on the user's own machine as the durable memory of the work. The AI assistant is not just answering questions; it is helping maintain a structured body of knowledge, with clear rules for what to read, what to trust, what to ignore, and what to update.

The core idea is simple:

- create a written constitution for the workspace
- create a map of the knowledge base
- store important knowledge as ordinary files
- distinguish raw evidence from interpreted summaries
- require the AI assistant to read and update the workspace rules
- use an AI agent that can read files, write files, and run file-based commands on the user's desktop

This approach can be used in many domains: architecture, law, policy, healthcare operations, audit, research, engineering, education, finance, service design, organisational change, and any setting where knowledge needs to be captured, reused, challenged, and trusted.

## The Problem With Chat-Only AI

Chatbots are good at short conversations. They are less good as long-term working partners.

In a normal chatbot workflow:

- context lives mainly in the current conversation
- useful decisions may not be written down
- evidence and interpretation can become mixed together
- a new chat may not know what happened before
- the user has to keep re-explaining the project
- different assistants may read different material and reach different conclusions

This creates a trust problem. The AI may sound confident, but the user cannot easily see what it has read, what it has assumed, or whether it is using current project knowledge.

A constitutional workspace solves this by moving durable knowledge out of the chat and into files that both the human and the AI can read.

## What "Constitutional" Means

In this approach, a constitution is a plain-language operating document for the workspace.

It is a durable set of instructions that says:

- what the workspace is for
- who the work is for
- where important knowledge belongs
- what files should be read first
- what evidence should be trusted
- how uncertainty should be labelled
- when the AI should update the knowledge base
- what the AI should not do

The constitution gives the AI assistant a stable operating model. It also gives humans a visible way to inspect and improve how AI is being used.

## The Basic Structure

A constitutional AI-assisted workspace normally has five layers.

## 1. The Constitution

The constitution is the first file the AI should read.

It defines the workspace's purpose, working conventions, and AI behaviour rules. It should be located at the root of the workspace and can be called something like:

```text
ai-context.md
```

The exact name does not matter. What matters is that it is stable, easy to find, and consistently used.

A good constitution explains:

- the purpose of the workspace
- the role of the human owner
- the main documentation areas
- what counts as source evidence
- how to treat assumptions, risks, and open questions
- where the AI may add continuity notes
- what files the AI should avoid editing without permission
- how to bootstrap a new AI session

The constitution turns "please help me with this project" into a repeatable working protocol.

## 2. The Map

The map is a lightweight index of the workspace.

It tells the AI what exists, what each file is for, and when to read it. It can be called something like:

```text
ai-index.md
```

The map avoids two common failures:

- the AI reads too little and misses important context
- the AI reads too much and gets distracted by irrelevant material

A useful map contains short entries, not long summaries. For each durable file or folder, it records:

- path
- purpose
- when to read it
- evidence status, where relevant

The map is not a replacement for the documents themselves. It is a routing layer.

## 3. Local Rules

Some folders need their own rules.

For example, a folder containing raw transcripts may tell the AI:

- these files are source evidence
- do not read them by default
- prefer the condensed summaries
- only return to the raw files when evidence or wording matters

Those local rules can be stored in files such as:

```text
docs/Recordings/raw-transcriptions/ai-context.md
docs/Recordings/ai-context-material/ai-context.md
```

This allows different parts of the workspace to have different handling rules without overloading the root constitution.

There is also a useful distinction between human-facing and AI-facing folder guidance.

A `readme.md` file is for people. It explains what a folder is for, how humans should use it, and any practical conventions that make the contents understandable.

An `ai-context.md` file is for the AI assistant. It tells the agent how to interpret the folder, what to read first, what to skip, what counts as evidence, and what maintenance rules apply.

Either file can exist at the root or inside any folder where it adds value:

```text
docs/readme.md
docs/ai-context.md
docs/Research/readme.md
docs/Research/ai-context.md
docs/Evidence/readme.md
docs/Evidence/ai-context.md
```

Not every folder needs both. The pattern is optional and should stay lightweight:

- add `readme.md` when humans need orientation
- add `ai-context.md` when the AI needs special instructions
- add both when a folder has important meaning for both humans and AI
- avoid adding either when the folder is self-explanatory

This keeps the workspace navigable without turning every folder into a documentation project.

## 4. Durable Knowledge Files

The main body of knowledge should be stored as ordinary files, usually Markdown.

Markdown works well because it is:

- readable by humans
- readable by AI
- easy to diff and version
- portable across tools
- suitable for both rough notes and formal documents

Durable knowledge files can include:

- research notes
- meeting extracts
- decision records
- architecture notes
- process maps
- policy summaries
- risk logs
- investigation findings
- design options
- glossary entries

The important principle is that valuable context should not remain trapped in chat history. If it will matter later, write it back into the workspace.

## 5. Human And AI Journals

A constitutional workspace can benefit from two different journals: one owned by the human, and one maintained by the AI assistant.

They should be separate because they serve different purposes.

The human journal is the user's working notebook. It can contain:

- personal observations
- meeting notes
- decisions made outside the AI session
- stakeholder context
- priorities
- concerns
- reminders

The AI should normally treat the human journal as read-only unless explicitly asked to edit it. This preserves the human's voice and avoids the assistant accidentally rewriting the user's own record.

The AI assistant journal is different. It is a continuity log for the AI-assisted workspace. It can contain:

- assumptions the AI has made
- investigation breadcrumbs
- summaries of previous AI work
- useful associations between documents
- unresolved questions
- warnings for future sessions
- notes about how the workspace is evolving

The AI assistant journal is not a hidden memory. It is visible, editable, and inspectable by the human. This is important: the AI's continuity should live in the workspace, not inside an opaque model memory or a disappearing chat.

Used well, the two-journal pattern gives the workspace both human continuity and AI continuity while keeping ownership clear.

## 6. Evidence And Extracts

Trust improves when the workspace distinguishes raw evidence from interpreted material.

For example:

- raw meeting transcript: source evidence
- condensed AI-readable summary: working context
- formal report: curated output
- journal note: working memory

This distinction lets the AI work efficiently while preserving traceability. It can use the concise summary most of the time, but return to the raw evidence when nuance, wording, or verification matters.

This pattern is especially useful for knowledge-transfer recordings, interviews, workshops, policy documents, service manuals, research material, or operational procedures.

## The Role Of The AI Agent

This approach requires more than a basic chatbot.

The AI assistant needs to act as a file-aware agent. It must be able to:

- read files on the user's desktop or workspace
- write and update files
- search folders
- run file-based commands
- inspect differences between versions
- maintain indexes and context files

The important capability is not the brand of agent; it is that the agent can safely operate on local files and commands under the user's control.

Without file access, the assistant can still give advice, but it cannot reliably maintain a durable workspace memory.

## How A Session Starts

A constitutional workspace should make session startup simple.

The user can begin with a prompt such as:

```text
Please read docs/ai-context.md first, then use this repository as the source of truth for the work.
```

The constitution then tells the AI what to read next. A typical order is:

1. root constitution
2. workspace map
3. relevant journal or continuity notes
4. active files mentioned by the user
5. local rules in the relevant folder
6. the smallest set of relevant source documents
7. raw evidence only when needed

This turns every new chat into a recoverable continuation rather than a restart.

## How The AI Maintains The Workspace

The AI assistant should not only consume the workspace. It should help maintain it.

Common maintenance duties include:

- adding new durable files to the map
- updating the constitution when a durable operating rule emerges
- converting raw transcripts into concise context extracts
- recording assumptions and open questions
- preserving uncertainty labels
- keeping human-owned notes separate from AI continuity notes
- avoiding unrelated rewrites
- avoiding secrets in documentation

This is where the approach becomes powerful. The workspace teaches the AI how to help maintain the workspace.

## Human Ownership And Safety

A constitutional workspace does not remove human judgement. It makes human judgement easier to apply.

The human remains responsible for:

- deciding what the workspace is for
- approving important changes
- reviewing evidence and conclusions
- deciding what can be shared
- setting boundaries around sensitive information
- correcting the constitution when the AI's behaviour needs to change

The AI assistant is useful because it can read, search, summarise, compare, and maintain structure at speed. It is not a substitute for accountability.

Important safety practices include:

- label assumptions clearly
- keep raw evidence available
- separate facts from interpretations
- do not store secrets in notes
- record open questions rather than hiding uncertainty
- make important AI instructions visible in files
- keep indexes short and navigable
- prefer source files over generated exports

## Why This Builds Trust

Trust comes from traceability and repeatability.

In this model, a human can inspect:

- what the AI was told to do
- what documents exist
- what sources were used
- what has been summarised
- what remains uncertain
- where a conclusion came from
- whether a new session followed the same rules

This is very different from relying on a single chat answer. The AI becomes part of a documented working system.

## A Reusable Pattern

The approach can be copied into a new domain with a small starting structure:

```text
workspace/
    ai-context.md
    ai-index.md
    Journal/
      journal.md
      ai-assistant-journal.md
    Evidence/
      ai-context.md
    Context/
      ai-context.md
```

The constitution explains the workspace. The map tells the AI where things are. Local context files explain how to treat specific folders. The journal records continuity. Evidence is preserved. Curated context makes the evidence usable.

Each profession can adapt the folder names:

- legal teams may use matters, evidence, advice, and authorities
- researchers may use literature, interviews, datasets, and findings
- architects may use current state, decisions, risks, and designs
- policy teams may use source policy, stakeholder input, options, and decisions
- operational teams may use processes, incidents, service notes, and runbooks

The underlying pattern stays the same.

## Common Anti-Patterns

Avoid these failure modes:

- relying on chat history as project memory
- asking the AI to read everything every time
- mixing raw evidence and AI interpretation without labels
- creating large indexes that are as expensive to read as the source material
- letting the AI create documents without updating the map
- storing passwords, keys, or confidential material in general notes
- treating AI summaries as evidence when they are actually interpretations
- hiding uncertainty because it makes the document look cleaner

The goal is not to make the AI sound certain. The goal is to make the work more navigable, inspectable, and reusable.

## Implementation Checklist

1. Create a root constitution file.
2. Define the purpose of the workspace and the human owner's role.
3. Define where durable knowledge should live.
4. Create a lightweight map of important files.
5. Add local rules for folders that contain raw evidence or special material.
6. Decide how assumptions, risks, decisions, and open questions will be labelled.
7. Create a human journal and an AI continuity journal if useful.
8. Tell the AI to update the map whenever durable files are added or materially changed.
9. Use an agent that can read and write files and run local file-based commands.
10. Periodically review the constitution as the working practice matures.

## Conclusion

A constitutional AI-assisted workspace turns AI from a temporary chat partner into a structured collaborator.

The constitution gives the assistant operating rules. The map helps it navigate. Durable files preserve knowledge beyond the current conversation. Local rules protect evidence and context. Human review keeps the system accountable.

This approach is deliberately simple. It uses files, folders, plain text, and disciplined conventions. That simplicity is its strength: it lets people in many professions capture knowledge, preserve trust, and use AI in a way that is structured, safe, and repeatable.
