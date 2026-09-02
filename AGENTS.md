# claude-oss

One bash script, `claude-oss`, that launches Claude Code against Anthropic-compatible endpoints from other providers. No build, no dependencies. Public MIT repo: nothing Pickforge-internal, no keys, no made-up endpoints.

```
bash -n claude-oss
shellcheck claude-oss
printf '1\n' | ./claude-oss list
```

Worth knowing:

- The script writes provider config to `~/.config/claude-oss/` and seeds presets on any invocation, even `--help`. When trying things out, point it somewhere harmless: `XDG_CONFIG_HOME=$(mktemp -d) ./claude-oss list`.
- People install it by symlinking the repo file into `~/.local/bin`, so an edit here is live on the machine immediately.
- The README is the user docs. Its CLI table, permission-mode table and provider `.conf` key list have to match the script; nothing enforces it.
- Model ids in the seeded presets are fallbacks. The real list comes from `/v1/models` at runtime.
