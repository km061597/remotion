# @remotion/skills

This package holds the Remotion Agent Skills (`skills/`) and doubles as a
[Claude Code plugin](https://code.claude.com/docs/en/plugins).

## Install in Claude Code

The repository root is a Claude Code plugin marketplace
(`.claude-plugin/marketplace.json`). Add it and install the `remotion` plugin:

```bash
/plugin marketplace add remotion-dev/remotion
/plugin install remotion@remotion
```

This makes the `remotion` skill available so Claude Code knows the best
practices for building videos programmatically with Remotion — animations,
timing, audio, captions, 3D, transitions, charts, text effects and rendering.

The skill is defined in `skills/remotion/SKILL.md` and is the single source of
truth shared with the [`@remotion/codex-plugin`](../codex-plugin) package.
