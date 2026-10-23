# codeonym-oss Claude Code plugins

The marketplace for the open-source Claude Code plugins of [codeonym-oss](https://github.com/codeonym-oss).

```
/plugin marketplace add codeonym-oss/claude-plugins
```

| plugin | install | what it does |
|---|---|---|
| [groundwork](https://github.com/codeonym-oss/groundwork) | `/plugin install groundwork@codeonym-oss` | plan work before building it: grill an idea into epics, stories and tickets, keep every decision, build each ticket with your approval at every step |
| [design skills](https://github.com/codeonym-oss/design-skills) | `/plugin install codeonym-oss@codeonym-oss` | design skills with a reproducible headless toolchain (Blender, GIMP, Inkscape, Krita, Scribus, darktable, ffmpeg) |

## Already added `codeonym-oss` from design-skills?

Before this repo existed, the marketplace lived in `codeonym-oss/design-skills`. Two marketplaces can't share the
name `codeonym-oss`, so switch to this one, then install the plugins you want from it again:

```
/plugin marketplace remove codeonym-oss
/plugin marketplace add codeonym-oss/claude-plugins
```

## License

[MIT](LICENSE)
