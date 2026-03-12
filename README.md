# Design Proposal Skill for Claude Code

A Claude Code plugin that transforms brainstorming design docs into concise, human-reviewable proposals.

## What It Does

This skill takes a brainstorming design doc and walks you through creating a structured proposal document, one section at a time. It asks clarifying questions, drafts each section for your review, and saves the final proposal to your repo.

**Proposal sections:**

1. Problem Statement
2. User Stories
3. Proposed Solution
4. Why This Approach
5. Scope & Non-Goals
6. Risks & Open Questions
7. Success Criteria

The output is written for mixed audiences — engineers, product owners, and designers can all evaluate it without needing the technical design doc.

## Installation

### 1. Add the marketplace

```
/plugin marketplace add gbrowdy/claude-design-doc-skill
```

### 2. Install the plugin

```
/plugin install design-proposal@gbrowdy-claude-design-doc-skill
```

Or run `/plugin`, go to the **Discover** tab, and select **design-proposal**.

## Usage

Invoke the skill directly:

```
/design-proposal
```

Or Claude will automatically use it when you're working with a brainstorming design doc that needs to become a reviewable proposal.

**Expected input:** A brainstorming design doc, typically at `docs/plans/YYYY-MM-DD-<topic>-design.md`.

**Output:** A proposal saved to `docs/proposals/YYYY-MM-DD-<topic>-proposal.md` and committed to git.

## License

MIT
