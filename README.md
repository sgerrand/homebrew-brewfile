# homebrew-brewfile

A curated list of [Homebrew](https://brew.sh) software to install via [strap](https://github.com/MikeMcQuaid/strap).

## Development

### Requirements

- [Homebrew](https://brew.sh)

### Setup

Run the setup script to install dependencies and activate git hooks:

```sh
bin/setup
```

This installs [lefthook](https://github.com/evilmartians/lefthook) and registers a pre-commit hook that lints the `Brewfile` before each commit.

### Linting

To run the linter manually:

```sh
bin/lint
```

The linter checks for:

- Duplicate `brew`, `cask`, `tap`, and `mas` entries
- Deprecated taps (`homebrew/cask-drivers`, `homebrew/cask-fonts`, `homebrew/cask-versions`)

### Continuous integration

The lint script runs automatically on every push and pull request via GitHub Actions.
