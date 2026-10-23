# codeonym-oss plugins

The marketplace for the open-source plugins of [codeonym-oss](https://github.com/codeonym-oss), available in
Claude Code and Codex. The repository name remains `claude-plugins` for existing installations.

## Claude Code

```
/plugin marketplace add codeonym-oss/claude-plugins
```

| plugin | install | what it does |
|---|---|---|
| [groundwork](https://github.com/codeonym-oss/groundwork) | `/plugin install groundwork@codeonym-oss` | plan work before building it: grill an idea into epics, stories and tickets, keep every decision, build each ticket with your approval at every step |
| [design skills](https://github.com/codeonym-oss/design-skills) | `/plugin install design-skills@codeonym-oss` | design skills with a reproducible headless toolchain (Blender, GIMP, Inkscape, Krita, Scribus, darktable, ffmpeg) |

## Codex

Run these commands in your terminal with a Codex CLI that supports `codex plugin`:

```bash
codex plugin marketplace add codeonym-oss/claude-plugins
codex plugin list
codex plugin add groundwork@codeonym-oss
```

To install Design Skills as well:

```bash
codex plugin add design-skills@codeonym-oss
```

Start a new Codex session and use `/skills` to find the installed skills. For example, ask Codex to use
Groundwork's `init` skill in your project. Claude's `/groundwork:...` command syntax is specific to Claude Code.

If you registered this repository before Codex support was added, refresh it:

```bash
codex plugin marketplace upgrade codeonym-oss
codex plugin list
```

The Codex catalog is `.agents/plugins/marketplace.json`; the Claude catalog remains
`.claude-plugin/marketplace.json`. Both expose the same plugin names and repositories. The marketplace is
`codeonym-oss`; the plugins are `groundwork` and `design-skills`. When adding a plugin, update both catalogs.
Registering a marketplace does not install all its plugins; each plugin is selected explicitly.

Design Skills was previously named `codeonym-oss`. Existing installations should follow its
[plugin rename migration](https://github.com/codeonym-oss/design-skills#migrating-from-the-old-plugin-name).

Codex installation has been checked with both plugins in an isolated configuration. This verifies packaging,
skills and bundled references; it does not establish that every skill workflow has been tested in Codex or install
Design Skills' external toolchain. Follow each plugin's setup instructions for its dependencies.

See the [Codex marketplace documentation](https://developers.openai.com/plugins/build/plugins).

## Already added `codeonym-oss` from design-skills?

Before this repo existed, the marketplace lived in `codeonym-oss/design-skills`. Two marketplaces can't share the
name `codeonym-oss`, so switch to this one, then install the plugins you want from it again:

```
/plugin marketplace remove codeonym-oss
/plugin marketplace add codeonym-oss/claude-plugins
```

The same name conflict can occur in Codex. Only if `codeonym-oss` is registered from `design-skills` instead of
this repository, replace that source and install the desired plugins again:

```bash
codex plugin marketplace remove codeonym-oss
codex plugin marketplace add codeonym-oss/claude-plugins
```

## License

[MIT](LICENSE)
