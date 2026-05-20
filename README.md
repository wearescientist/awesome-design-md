# Awesome Design MD Skill

This repository is packaged so the repository root can be used directly as a Codex/agent skill.

It bundles a curated `DESIGN.md` style library and a skill router that helps an AI coding agent choose the right style for UI work instead of blindly applying one default look.

## Install

Clone this repository into your skills directory as `awesome-design-md`.

Windows PowerShell:

```powershell
git clone https://github.com/wearescientist/awesome-design-md "$env:USERPROFILE\.codex\skills\awesome-design-md"
```

macOS/Linux:

```bash
git clone https://github.com/wearescientist/awesome-design-md ~/.codex/skills/awesome-design-md
```

After installation, restart your agent session if it does not reload skills automatically.

## Use

Ask for UI work naturally:

```text
Redesign this admin page with a polished big-tech product style.
```

```text
Use Awesome Design MD and redesign this dashboard.
```

The skill will:

- choose one suitable style for the product context;
- read only that style's `DESIGN.md`;
- apply its visual rules to the current frontend task;
- preserve the target project's framework, flows, accessibility, and data density.

## Repository Layout

```text
SKILL.md                         # Skill entrypoint
STYLE_INDEX.txt                  # Available style list
design-md/<style>/DESIGN.md      # Bundled style references
references/style-selection.md    # Extra selection guidance
agents/openai.yaml               # Skill metadata for OpenAI-style skill UIs
```

## Notes

- The repository root is the skill root.
- `SKILL.md` uses paths relative to the skill root, so it works after cloning into another machine's skills folder.
- Do not load the entire `design-md/` library into context. The skill is designed for progressive disclosure: select one style, then read one `DESIGN.md`.

## License

See [LICENSE](LICENSE).
