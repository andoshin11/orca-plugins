# andoshin11/orca-plugins

An [Orca](https://www.onorca.dev) plugin marketplace.

## Add this marketplace

In Orca, open Settings → Plugins → Marketplaces, add a Git source, and enter:

- URL: `https://github.com/andoshin11/orca-plugins`
- Ref: `main`

The plugins below then appear in the plugin list. Installing one shows the permissions it asks for; Orca enables it only after you approve them.

## Plugins

| Plugin | Description |
| --- | --- |
| [`andoshin11.agent-status-relay`](https://github.com/andoshin11/orca-agent-status-relay) | Forwards agent status changes (turn done, waiting, blocked) to a URL, signed with Standard Webhooks. Used by [orca-dots-bridge](https://github.com/andoshin11/orca-dots-bridge) to notify ChatGPT dot. |
| [`andoshin11.milestone`](https://github.com/andoshin11/orca-milestone) | Shows the tasks Claude Code and Codex are working through as milestones in the right sidebar. Needs Orca 1.4.247 or later. |

## Publishing a release

Plugins are listed in `orca-catalog.json`, and each release pins an exact commit and content hash, which lets Orca update them automatically.

1. Tag the release in the plugin's repository.
2. In a clean checkout of that tag, run `orca plugin release-entry .` and put the printed entry first in the plugin's `releases`. Paste it rather than writing it by hand, since Orca refuses bytes that differ.
3. Check the file with `orca plugin validate orca-catalog.json`.

`orca-marketplace.json` is the older format for Orca before 1.4.245. Orca reads `orca-catalog.json` first. New releases of these plugins need a newer Orca, so that file is left as it is.
