# homebrew-agentuna

Homebrew tap for [AgenTuna](https://github.com/tapas-joshi/AgenTuna): skills, MCP servers and rule
files for coding agents, managed across scopes.

```sh
brew tap tapas-joshi/agentuna

# The desktop app (macOS Apple Silicon, macOS 13+) and the `agentuna` command
brew install --cask agentuna

# Or only the command-line tool (macOS Apple Silicon and Linux x86_64)
brew install agentuna-cli
```

The two conflict on purpose: the cask already links `agentuna` from the app bundle.

## About the app build

AgenTuna 0.x is a preview. The macOS app is **ad-hoc signed and not notarized** (no Apple Developer
ID yet). The cask clears the quarantine flag after installing so that it opens without the
Gatekeeper prompt; the download is verified against the SHA-256 recorded in the cask. Read the
[release notes](https://github.com/tapas-joshi/AgenTuna/releases) and the cask source before you
install, as you would for any third-party tap.

## How this tap is maintained

`Casks/agentuna.rb` and `Formula/agentuna-cli.rb` are generated from each release's `SHA256SUMS` by
`scripts/homebrew-tap.sh` in the AgenTuna repository. Do not edit them by hand; open an issue on the
main repository instead.
