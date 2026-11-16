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
- There are no bottles yet, so the first install builds every Python dependency from source, and Homebrew also
  installs Rust and its toolchain as a build dependency. Expect several minutes and a large download on a
  clean machine; the build itself took about 2.5 minutes with the toolchain already present.
- Tested on Linux with Homebrew 7.0.12: `brew install`, `brew test`, `brew style` and
  `brew audit --strict --new`, including a plain `brew install Opencomplai/tap/opencomplai` from this tap.
  macOS has not been tested yet.
- The formula puts the `opencomplai` command on your PATH. The two CI connector scripts that come with
  `opencomplai-cli` are installed inside the formula's virtualenv but not linked. Where you need them, run
  `uv tool install opencomplai-cli`, or `pip install opencomplai` into a virtualenv.
- Without Homebrew, `uv tool install opencomplai` or `pip install opencomplai` install the same CLI.

Bugs and questions belong in the [main repository](https://github.com/Opencomplai/opencomplai/issues).
