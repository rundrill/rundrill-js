# RunDrill JavaScript / TypeScript

Your personal **JavaScript & TypeScript coach** inside your AI agent — learn the language the way it
actually bites: by **reading, tracing, and predicting** code, and by **reviewing real code for the
bug it hides**, not by watching the AI write it for you. Short targeted drills, an honest picture of
your level, mistake memory that resurfaces what you got wrong, and optional hands-on exercises you
write and run yourself. Your level and progress live on the RunDrill MCP server (`mcp.rundrill.com`),
synced across machines — not in a local file.

**Why this course is different.** JavaScript's hardest concepts — `this`, closures, and the async
event loop — all need an execution model the syntax never shows, and TypeScript's types vanish at
runtime. When an AI can draft any function on demand, the real risk is the *illusion of competence*:
accepting code that reads fine and is quietly wrong — a `==` coercion, a `this` lost in a callback, a
`var` loop-closure capturing the wrong value, an un-awaited promise, an `innerHTML` XSS, an
over-confident `as` cast that lies to the type checker. The **signature drill hands you plausible
AI-written JS/TS with the bug unlabeled and asks you to find and name it, like a pull-request
review** — the one skill that matters most once an AI writes the first draft. Around it: predict-the-
output drills (coercion tables, async ordering), read-the-error, fix-the-bug, and refactor-with-
justification.

**TypeScript is woven in.** TS is JavaScript with a type system, so you learn the runtime first and
the types on top — from `M` (Mid) onward: basic types and inference, narrowing, generics, utility
types, `keyof`/`typeof`, declaration files, and at the Expert tier conditional/mapped/template-literal
types, variance, branded types, and `satisfies`.

The course mirrors a five-level spine — **Novice → Junior → Mid → Senior → Expert** — plus three
applied tracks you can opt into: **Frontend** (the DOM, events, fetch, the render pipeline, Web
Components, React), **Backend / Node** (the runtime, streams & backpressure, HTTP, REST, databases,
auth, deployment), and **Internals** (the engine pipeline, the event loop in depth, hidden classes,
garbage collection, the TypeScript compiler). `core` is always in scope.

> **Hands-on is optional.** By default every drill is chat-deliverable (predict, trace, review). Turn
> on hands-on and the coach gives you exercises to write and run in your own `node`/`tsc`/browser
> workspace, scored against a rubric. The coach never writes the solution for you.

**Learn in your language.** Set your native language and the coach explains in it while giving every
JS/TS term as *native (English original)* — so you reason naturally and still recognise the exact
term in real code, errors, and docs.

## One plugin, three hosts

The coaching skill (`skills/js-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its own
manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` |

The MCP endpoint is `https://mcp.rundrill.com/prog/js` — the programming-course host, passing
`language: "js"`. The server routes on the `/prog` segment and ignores the course name; the name
makes JavaScript register as its own MCP server in your agent. On first use the host opens a browser
tab for the OAuth handshake, then closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/rundrill
  /plugin install rundrill-js@rundrill
  ```
  Then run `/js-coach`.
- **OpenAI Codex** — `codex plugin marketplace add rundrill/rundrill`, then install `rundrill-js`.
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-js/` (global) or
  `<workspace>/.agents/plugins/rundrill-js/` (workspace-scoped).

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0
International (CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE). You may view, run, and share this
plugin unchanged, non-commercially, with attribution; you may not use it commercially or publish
modified/derivative versions. For other licensing, contact **hello@rundrill.com**.
