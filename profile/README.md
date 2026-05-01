# SetupProof

SetupProof tests marked README quickstarts from a clean workspace before
contributors hit them.

The main project is [setupproof/setupproof](https://github.com/setupproof/setupproof).

```sh
go install github.com/setupproof/setupproof/cmd/setupproof@v0.1.0
setupproof review README.md
setupproof --require-blocks --no-color --no-glyphs README.md
```

Use the GitHub Action with a pinned Action tag and CLI version:

```yaml
- uses: setupproof/setupproof@v0.1.0
  with:
    cli-version: v0.1.0
    require-blocks: "true"
    files: README.md
```

SetupProof is intentionally narrow: it verifies explicitly marked shell blocks,
reports what passed or failed, sends no telemetry, and does not execute
unmarked Markdown examples.
