# README structure

Adapted compact reference for ChatGPT Web based on Petr Král's original `readme-structure.md`.

## Default order

Use the following order if the repository provides verified content. Omit unsupported sections, and keep the path from prerequisites to first successful use contiguous.

1. Header (project logo if present, title, evidenced badges)
2. One short paragraph: what the project does and for whom
3. Requirements (verified tools, runtime, hardware prerequisites)
4. Installation (verified installation instructions)
5. Configuration (real option names and example environment variable names, no secrets)
6. Quick start (smallest verified example)
7. Features/What it does, only when necessary
8. Documentation, only with confirmed destinations
9. Testing (documented test command)
10. Upgrading, only with supported procedure
11. Changelog, Contributing, Security (only existing files)
12. Credits (only verified sources)
13. License (only verified license)

Optional Architecture, Hardware, Pinout, API, Deployment, Roadmap only when appropriate and supported by source; apply hardware safety when relevant. For a library, emphasize real API calls; for an app, show the first-run path; for monorepo, direct readers to package README files.

## Writing rules

- Keep the first paragraph concise. Never pad sections with generic marketing copy.
- Every sentence must add a verifiable fact. Prefer commands to paragraphs describing commands.
- Preserve the existing README language when updating it. For a new README, follow the requested language; otherwise default to English for public OSS.
- Do not copy unrelated project names, logos, version numbers or support URLs into the output.
- Keep Markdown headings consistent and write meaningful image alt text.
- Only include badges with verified registries/licenses/workflow triggers; prefer four or fewer.
- Use a light/dark `<picture>` header only when the repository owns the requisite assets.
- Structure quick-start examples around the project's actual main use case, taking signatures and configuration from code/tests/examples.

## Example (omit any unsupported sections, including headings)

```markdown
# Project name or verifiable benefit

Brief description grounded in source.

## Requirements
Verified prerequisites

## Installation
Verified command(s)

## Configuration
Verified option names

## Quick start
Verified example

## Testing
Verified command(s)

## Contributing
Link to existing guide

## License
Link to actual license
```

## Ecosystem pointers (evidence, not defaults)

- Node: package.json scripts + lockfile package manager, actual published registry
- Python: pyproject.toml, test configuration and deployed entry points
- PHP: composer.json and published Packagist entries, if confirmed
- Rust: Cargo.toml, crate sources, tests
- Go: go.mod, current packages and tests
- Arduino/STM32 embedded: board/MCU configuration, wiring, pin mappings, power constraints, firmware entry points and verified build/flash instructions
