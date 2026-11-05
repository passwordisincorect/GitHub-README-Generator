# GitHub README Generator

GitHub README Generator is a ChatGPT plugin that bundles an **evidence-backed README skill**. It can help inspect an existing repository, audit its documentation, and draft or update the root `README.md` using information verified against code, manifests, tests, CI and repository metadata.

The packaged plugin version is **`1.0.0-beta.1`**. This repository hosts its plugin source; **pushing the source to GitHub does not install or publish the plugin inside ChatGPT**.

## Requirements

- A ChatGPT environment that supports importing skill-based plugins.
- Repository files or a connected source-access tool (such as GitHub) for evidence collection.
- Write permission only when you explicitly request changes to the target repository.

No application runtime, API key, standalone executable or MCP server is bundled with this plugin.

## Installation

1. Download or clone this repository.
2. Create a ZIP archive **of the repository contents**, keeping `plugin.json`, `.codex-plugin/` and `skills/` at the **archive root** (not inside an extra parent directory).
3. Import that archive into ChatGPT using **Plugin Creator**, then connect/enable the plugin as permitted by your ChatGPT workspace.

The repository is the auditable source of the plugin; installation and permissions are managed separately in ChatGPT.

## Configuration

- [`plugin.json`](plugin.json) — plugin identity and ChatGPT interface metadata.
- [`.codex-plugin/plugin.json`](.codex-plugin/plugin.json) — Codex-compatible plugin manifest.
- [`SKILL.md`](skills/github-readme-generator/SKILL.md) — workflow and safety rules for README work.

The Skill does not grant filesystem or GitHub access by itself. Available tool permissions remain controlled by the ChatGPT environment and connected apps.

## Quick start

After installing the plugin, try these requests in ChatGPT:

- **Audit:** "Audit my repository README without changing files. Compare documentation with the code."
- **Draft:** "Write a README from verified repository evidence. Show the draft before editing."
- **Update:** "Update this repository's README to match the current source. Do not change production code."
- **Push:** "Commit and push only the reviewed README changes to the repository."

The skill requires concrete evidence for commands, versions, feature descriptions and links. An audit is read-only; edits, commits and pushes require an explicit request.

## Contents

```text
plugin.json
.codex-plugin/
  plugin.json
skills/
  github-readme-generator/
    SKILL.md
    LICENSE.md
    references/
      evidence-policy.md
      readme-structure.md
      validation-checklist.md
```

The reference documents cover evidence requirements, README structure and a final validation checklist. The plugin has no automated test suite in this repository; a basic source check consists of parsing both JSON manifests and checking the referenced files are present. Real plugin execution must be verified after importing it into ChatGPT.

## Attribution and license

This package adapts the GitHub README Generator skill by [Petr Král](https://github.com/pekral/github-readme-generator). The original author's MIT copyright notice is preserved in [`skills/github-readme-generator/LICENSE.md`](skills/github-readme-generator/LICENSE.md), and the root [`LICENSE`](LICENSE) provides the repository's MIT license.
