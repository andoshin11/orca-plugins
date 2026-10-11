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

Each entry pins a Git tag; a new plugin version is published by updating its `ref` in `orca-marketplace.json`.
