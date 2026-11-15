# Ready Room plugin for Claude Code

Adds [Ready Room](https://readyroom.dev) to Claude Code:

- **The Ready Room connector**, at `https://mcp.readyroom.dev/mcp`. Your agent
  uses it to send your working copy's product intent to Ready Room, open the
  room card, check the code against the intent, and ask you questions.
- **A skill for writing your product intent**: the format of the intent
  package under `product/` (the Ready Intent Package, or RIP) and how to
  validate it, send it, and check code against it.

## Install

In Claude Code:

```
/plugin marketplace add swabbieeth/readyroom-plugin
/plugin install readyroom@readyroom
```

No credential is stored. The first time a Ready Room tool is used, Ready Room
opens in your browser: sign in if you aren't already, check that the page names
the app you expect, and choose **Approve**. If Claude Code lists the server as
needing sign-in, run `/mcp`, choose **readyroom**, and sign in from there.

Then ask Claude to send your working copy and open the room. See
[Getting started](https://readyroom.dev/docs/getting-started).

## Claude on the web or the desktop app

You don't need this plugin there. Add a custom connector with the same
address, `https://mcp.readyroom.dev/mcp`, then sign in and approve.

To check an intent package's format on your computer, run
`npx @readyroom/ready validate .` from the repository root (see
[`@readyroom/ready`](https://www.npmjs.com/package/@readyroom/ready)).

Version 1.0.0. This repository is generated from Ready Room;
changes made here are overwritten.
