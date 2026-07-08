# SetupProof

SetupProof tests marked README quickstarts from a clean workspace before
contributors hit them.

The main project is [setupproof/setupproof](https://github.com/setupproof/setupproof).

```sh
go install github.com/setupproof/setupproof/cmd/setupproof@v0.1.3
setupproof review README.md
setupproof --require-blocks --no-color --no-glyphs README.md
```

Use the GitHub Action with a pinned Action tag and CLI version:

```yaml
- uses: setupproof/setupproof@v0.1.3
  with:
    cli-version: v0.1.3
    require-blocks: "true"
    files: README.md
```

SetupProof is intentionally narrow: it verifies explicitly marked shell blocks,
reports what passed or failed, sends no telemetry, and does not execute
unmarked Markdown examples.

Useful entry points:

- [Install guide](https://setupproof.github.io/setupproof/INSTALL.html)
- [GitHub Action usage](https://github.com/setupproof/setupproof#github-actions)
- [Architecture notes](https://setupproof.github.io/setupproof/ARCHITECTURE.html)
- [Troubleshooting](https://setupproof.github.io/setupproof/TROUBLESHOOTING.html)
