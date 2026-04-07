
# Vision

## Background

A lot of current work around "adding AI to applications" focuses on the visible layer:

- adding chat inside the product
- exposing tools or function calls
- automating UI actions
- building agent workflows on top of ad hoc capabilities

These approaches are useful, but they often skip an important engineering question:

How should AI systematically understand an application and transform it into something that can be driven by AI in a stable and reusable way?

This repository is an attempt to explore that question.

## Core belief

The key to AI-driven applications is not only the model, the chat UI, or a list of tools.

The deeper layer is this:

AI should be able to read code, understand the application, identify stable capability boundaries, design an AI driver layer, implement it, and then generate task-specific skills for real work.

In other words, this is not only about "using AI inside an app".  
It is about building a reusable path for application AI-enablement.

## The pipeline

### 1. Codebase Comprehension

AI first reads the codebase and builds a structured understanding of the application.

This includes:

- entry points
- module boundaries
- UI layer, service layer, data layer
- pages, windows, commands, workflows
- models and state flow
- important dependency relationships

The goal of this phase is understanding, not code modification.

### 2. Feature Inventory Extraction

After understanding the codebase, AI should extract real application features.

This is not a raw list of classes or functions.  
It should capture:

- user-visible features
- important business actions
- querying, editing, generating, exporting, deleting, syncing, notifying
- which capabilities are suitable for AI driving
- which ones require confirmation or stronger controls

The goal of this phase is to convert code structure into a capability map.

### 3. AI Driver Layer Design

Once capabilities are visible, AI should decide how to add an AI driver layer.

Questions in this phase include:

- where should the AI driver layer live
- what capabilities should be exposed
- what should remain read-only
- what requires confirmation
- how context, logging, errors, and return structure should be handled
- how to preserve the original architecture

The goal of this phase is to design the layer before implementing it.

### 4. AI Driver Implementation

Only after design is clear should AI begin to generate or modify code.

The implementation should aim to:

- reuse existing business logic whenever possible
- avoid rewriting the application's core
- avoid binding the driver layer directly to fragile UI event handlers unless necessary
- produce a maintainable and extensible middle layer

The goal of this phase is to make the application actually AI-drivable.

### 5. Task Skill Authoring

Once the application has an AI driver layer, AI should be able to generate task-oriented `skill.md` files.

These task skills define how AI should complete real work inside the application, such as:

- filtering and exporting customers
- updating records and notifying stakeholders
- scanning project state and generating reports
- cleaning data and building summaries
- preparing content and publishing outputs

The goal of this phase is to move from atomic actions to reusable work skills.

## Why this matters

If this process can be made reusable, then "adding AI to applications" stops being a one-off integration exercise.

It becomes a repeatable engineering path.

That means:

- different applications can share the same high-level workflow
- different stacks can test the same method
- different communities can contribute examples and counterexamples
- task skills can become reusable assets instead of isolated prompts

## What we want to discuss

This repository exists to make that discussion concrete.

Key discussion questions include:

1. Is this five-phase pipeline valid and useful?
2. Where should an AI driver layer ideally live?
3. How should `skill.md` be structured for this kind of work?
4. Can this approach generalize across different stacks?
5. What does a strong real-world case look like?
6. What are the failure modes of this approach?

## Invitation

This is not presented as a final answer.

It is an attempt to open up a direction:

building a reusable path for turning arbitrary applications into AI-driven applications through code understanding, capability extraction, driver layer design, implementation, and task skill generation.

If you are exploring anything close to this, your feedback, criticism, examples, and counterexamples are all valuable.