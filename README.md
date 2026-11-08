# Homebrew tap for opencomplai

[opencomplai](https://github.com/Opencomplai/opencomplai) checks AI systems against the EU AI Act from the
command line. This tap installs the CLI.

```bash
brew install Opencomplai/tap/opencomplai
opencomplai --version
```

You can also run `brew tap Opencomplai/tap` once and then `brew install opencomplai`. To update:
`brew update && brew upgrade opencomplai`.

## Good to know

- The formula installs the `opencomplai` package from PyPI into its own virtualenv, on Python 3.12.
- There are no bottles yet, so the first install builds some dependencies from source and needs Rust at build time.
  Expect a few minutes.
- Tested on Linux with Homebrew 7.0.12: `brew install --build-from-source`, `brew test` and
  `brew audit --strict --new`. macOS has not been tested yet.
- The formula installs the `opencomplai` command only, not the two CI connector scripts that ship in the package.
- Without Homebrew, `uv tool install opencomplai` or `pip install opencomplai` install the same CLI.

Bugs and questions belong in the [main repository](https://github.com/Opencomplai/opencomplai/issues).
