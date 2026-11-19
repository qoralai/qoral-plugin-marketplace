# Qoral plugin marketplace

A plugin marketplace for [Claude Code](https://claude.com/claude-code) and Codex. It lists one plugin today, bwat.

bwat joins your team's meetings, turns what people commit to into cards that quote the sentence
they came from, and hands that work to your own Claude Code sessions. It is self-hosted: to run a
bwat server, see [qoralai/bwat](https://github.com/qoralai/bwat).

| Plugin | What it does |
|--------|--------------|
| [bwat](https://github.com/qoralai/bwat-plugin) | Your bwat hand-off inbox, meetings and transcripts in your Claude Code and Codex sessions, over a local MCP server. |

## Install bwat in Claude Code

In a terminal:

```sh
claude plugin marketplace add qoralai/qoral-plugin-marketplace
claude plugin install bwat@qoral-plugin-marketplace --config base_url=https://<your bwat address>
```

Or inside Claude Code:

```text
/plugin marketplace add qoralai/qoral-plugin-marketplace
/plugin install bwat@qoral-plugin-marketplace
```

Claude Code asks for the bwat address when the plugin is enabled. Ask whoever set up bwat for it.
Then run `/bwat:login` to sign in, and `/bwat:status` to check which bwat the session talks to.

## Install bwat in Codex

In a terminal:

```sh
codex plugin marketplace add qoralai/qoral-plugin-marketplace
codex plugin add bwat@qoral-plugin-marketplace
```

Codex cannot ask for the bwat address, so ask Codex to sign in to bwat with it: it passes the
address to `bwat_login`, which keeps it for every later session. Sign out with `bwat_logout` to
use another.

The plugin needs Node.js 22 or later on PATH.

## License

This marketplace is under the [MIT License](LICENSE). Each plugin it lists has its own licence, in its own repository.
