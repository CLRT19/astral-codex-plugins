# Astral Codex Skills

This repository provides Codex skills for Astral's Python tools:

- `uv` (package and project management)
- `ruff` (linting and formatting)
- `ty` (type checking)

## Installation

Install the skills into your Codex skills directory (`$CODEX_HOME/skills`, or
`~/.codex/skills` by default):

```bash
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$CODEX_HOME/skills"

cp -R skills/uv "$CODEX_HOME/skills/"
cp -R skills/ruff "$CODEX_HOME/skills/"
cp -R skills/ty "$CODEX_HOME/skills/"
```

If you are developing this repository, symlink instead of copying:

```bash
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$CODEX_HOME/skills"

ln -sfn "$PWD/skills/uv" "$CODEX_HOME/skills/uv"
ln -sfn "$PWD/skills/ruff" "$CODEX_HOME/skills/ruff"
ln -sfn "$PWD/skills/ty" "$CODEX_HOME/skills/ty"
```

Restart Codex after installing or updating skills.

## Usage

Use the skills by name in prompts:

- `$uv` for dependency management, environments, and script/project workflows
- `$ruff` for linting, formatting, and auto-fixes
- `$ty` for type checking and rule configuration

Example:

```text
Use $ruff and $ty to fix lint and type errors in this Python package.
```

## Repository Layout

```text
skills/
  uv/
    SKILL.md
    agents/openai.yaml
  ruff/
    SKILL.md
    agents/openai.yaml
  ty/
    SKILL.md
    agents/openai.yaml
```

## License

Licensed under either of:

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  http://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for development setup and guidelines.

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
