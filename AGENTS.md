Public MIT launcher: no Pickforge-internal material, keys or invented endpoints.

Every invocation, including `--help`, seeds provider config. Use a temporary `XDG_CONFIG_HOME` when testing so real config is untouched. Installs may symlink the repo script into `~/.local/bin`, so an edit can change the installed command immediately.

Keep the README CLI table, permission-mode table and provider `.conf` keys aligned with the script; no automated check enforces this. Seeded model IDs are fallbacks. The runtime model list comes from `/v1/models`.
