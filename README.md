# ai-app-driver

[中文版](README_CN.md)

A practical approach to turn existing applications into AI-driven apps through code understanding, capability extraction, driver layers, and task skills.

下面给你一套可以直接放进仓库的初始内容。

你可以先建这几个文件：

* `README.md`
* `docs/vision.md`
* `docs/skills/README.md`
* `docs/cases/README.md`
* `docs/templates/README.md`

然后再发一篇 GitHub Discussion 首帖。

先给你完整内容。

README.md

````md
# ai-app-driver

Turn existing applications into AI-driven apps by teaching AI how to understand codebases, extract capabilities, design driver layers, implement them, and author task skills.

## What is this

This project explores a practical path for turning existing applications into AI-driven applications.

The core idea is simple:

AI should not only chat with an app, call a few tools, or click UI elements.

Instead, AI should be able to:

1. read an application's codebase
2. understand its structure and real features
3. identify the stable capability boundaries inside the app
4. build an AI driver layer on top of those capabilities
5. generate task-specific skills for real work

This repository is not just about prompts, wrappers, or demos.  
It is an attempt to build a reusable methodology for application AI-enablement.

## Why this exists

Today, many attempts to "add AI to an application" stop at one of these layers:

- a chat UI inside the app
- function calling or tools
- UI automation
- agent workflows without stable capability boundaries

These approaches can work, but they often miss a more important middle layer:

How should AI systematically understand an application, extract its usable capabilities, and turn them into a maintainable AI-driven layer?

This repository focuses on that missing layer.

## Core pipeline

The current working pipeline is:

1. **Codebase Comprehension**  
   AI reads and understands the codebase structure.

2. **Feature Inventory Extraction**  
   AI extracts real application features and usable capabilities.

3. **AI Driver Layer Design**  
   AI decides how the application's AI driver layer should be structured.

4. **AI Driver Implementation**  
   AI adds or generates the driver layer code.

5. **Task Skill Authoring**  
   AI writes task-oriented `skill.md` files for real-world work.

## What this repository is not

This repository is not:

- a model-specific prompt collection
- a UI automation project
- a simple function-calling wrapper
- a single-agent demo
- a framework tied to one language, stack, or vendor

## Current scope

Right now, this repository focuses on:

- defining the problem clearly
- proposing a reusable work pipeline
- drafting top-level work skills
- exploring how `skill.md` can guide AI system behavior
- collecting examples, counterexamples, and implementation cases

## Contributing

Contributions are welcome, especially if you have:

- built AI features into existing applications
- used AI to understand or refactor codebases
- designed task-oriented skill documents
- opinions on where AI driver layers should live
- cases from different stacks such as desktop apps, web apps, IDE tools, internal systems, or SaaS products

Please join the Discussions and share:

- similar projects
- disagreements
- examples
- design suggestions
- edge cases
- failure cases

## Repository structure

```text
docs/
  vision.md
  roadmap.md
  discussions.md
  skills/
  cases/
  templates/
````

## Discussion

This project starts as an open discussion:

How can we build a reusable path for turning arbitrary applications into AI-driven applications?

If this direction resonates with you, join the discussion.

