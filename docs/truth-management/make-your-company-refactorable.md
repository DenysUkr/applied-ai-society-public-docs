---
sidebar_position: 7
title: Make Your Company Refactorable
---

# Make Your Company Refactorable

Can you grep and make edits to your entire company "OS" with an agent call? If not, why?

The test: *Pick any operational change (renaming a concept, updating a policy, restructuring a workflow). Can an AI agent implement it across your entire organization's documentation in a single session?*

If the answer is no, you've built abstractions that cost more than they save.

## Why This Matters

The cost of abstraction has never been higher. Traditional tools (CMS platforms, no-code builders, siloed databases) introduce layers that AI agents can't navigate. Every abstraction between your intent and your documentation is friction that compounds with scale.

When Lee Robinson migrated cursor.com from a CMS to raw code and Markdown, he estimated weeks but finished in three days with $260 in tokens. The same tasks that required navigating admin panels, plugins, and database tables became single prompts.

## The Refactorability Principle

Your organizational truth should be:

### Grep-able
- Plain text formats (Markdown, not proprietary databases)
- Flat file structures over nested abstractions
- Content lives in code, not behind APIs

### Git-first
- All changes flow through version control
- No hidden state in CMS databases or admin panels
- Publishing is a commit, not a button click

### Agent-accessible
- An AI can read, understand, and modify any document
- No authentication walls between agent and content
- Standard formats that every model understands

## Implementation Guidelines

### Audit Your Current Stack
- Where does organizational knowledge live? (Notion, Confluence, Google Docs, SharePoint)
- How many clicks to edit? How many systems to update for one change?
- Can an AI agent access and modify it programmatically?

### Migrate to Refactorable Formats
See [Migrate to Refactorable Systems](./migrate-to-refactorable-systems) for the full process.

### Design for Agent Collaboration
- Structure files so agents can make targeted edits
- Use consistent naming conventions across all documentation
- Keep related content co-located rather than spread across systems

## The Trade-off

Some abstractions exist for good reasons (permissions, workflows, non-technical editors). The question isn't "eliminate all tools" but "can agents still work with the output?"

A Markdown file exported from Notion is refactorable. A policy locked in a proprietary database is not.

## The North Star

An organizational operating system where any strategic change (terminology updates, process revisions, policy shifts) can be implemented across all documentation by an agent in a single session. Not because agents are doing your thinking, but because your thinking is stored in formats they can act on.

---

## Further Reading

- [The Self-Improving Enterprise](/docs/concepts/self-improving-enterprise): Refactorability is the prerequisite for enterprises that evolve on their own
- [Supersuit Up Workshop](/docs/workshops/supersuit-up): The starting point for making your operation refactorable
- [Personal Agentic OS](/docs/concepts/personal-agentic-os): The system that operates on your refactorable files
- [Harness Engineering](/docs/concepts/harness-engineering): The code layer that reads and modifies your refactorable documents
- [Game Design](/docs/concepts/game-design): Defining the rules by which agents operate on your system
