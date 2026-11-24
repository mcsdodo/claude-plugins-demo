# claude-plugins-demo

A tiny demo of sharing Claude skills through a GitHub repository that works as a **plugin marketplace**.

It contains one plugin, `weird-greetings`, with one skill: say "Hi" in any language and Claude answers with a totally weird movie quote.

## Install

### Claude Code

```
/plugin marketplace add mcsdodo/claude-plugins-demo
/plugin install weird-greetings@mcsdodo-plugins
```

Then start a new session and type `Hi`, `Ahoj`, `Hola` or `こんにちは`.

To pull updates later:

```
/plugin marketplace update mcsdodo-plugins
```

### Claude desktop app

Download `weird-greetings.plugin` from the [Releases](../../releases) page and open it, or add the repo as a marketplace if your app supports custom marketplaces.

## Repository layout

```
claude-plugins-demo/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace catalog: lists the plugins in this repo
├── plugins/
│   └── weird-greetings/
│       ├── .claude-plugin/
│       │   └── plugin.json       # Plugin manifest
│       └── skills/
│           └── weird-movie-greeting/
│               └── SKILL.md      # The skill itself
└── README.md
```

## How it works

- **`marketplace.json`** turns the repo into a marketplace. Each entry in `plugins` points at a folder in the repo (or at another git repo).
- **`plugin.json`** describes one plugin: name, version, author.
- **`SKILL.md`** holds the instructions. Its `description` tells Claude when to use the skill; the body tells Claude what to do.

## Add your own plugin

1. Create `plugins/<your-plugin>/.claude-plugin/plugin.json`.
2. Add skills under `plugins/<your-plugin>/skills/<skill-name>/SKILL.md`.
3. Add an entry for it in `.claude-plugin/marketplace.json`.
4. Bump `version` when you change it, commit and push. Users get it with `/plugin marketplace update`.

## Note

Claude decides when to load a skill from its description, so a bare greeting usually triggers it, but not with 100% certainty. That is expected for a demo.

## License

MIT
