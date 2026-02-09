# Contributing

## Getting started

Clone the repository:

```bash
git clone https://github.com/<org>/astral-codex-plugins
cd astral-codex-plugins
```

Install skills into your local Codex skills directory:

```bash
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$CODEX_HOME/skills"

ln -sfn "$PWD/skills/uv" "$CODEX_HOME/skills/uv"
ln -sfn "$PWD/skills/ruff" "$CODEX_HOME/skills/ruff"
ln -sfn "$PWD/skills/ty" "$CODEX_HOME/skills/ty"
```

Restart Codex after making changes so updates are picked up.

## Development workflow

1. Edit skill instructions in `skills/<name>/SKILL.md`.
2. Keep frontmatter Codex-compatible:
   - Required keys: `name`, `description`
   - No extra keys in frontmatter
3. Update `skills/<name>/agents/openai.yaml` when user-facing metadata changes.
4. Test by using the skill in Codex with prompts that mention `$uv`, `$ruff`, or `$ty`.

## Pull requests

- Keep changes scoped to relevant skills.
- Preserve existing guidance unless intentionally updating behavior.
- Update `README.md` when install or usage instructions change.
