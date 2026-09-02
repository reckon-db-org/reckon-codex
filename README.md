# The Reckon Codex

**No Nonsense Event Sourcing.**

The opinionated book that ships with the [reckon](https://github.com/reckon-db-org) stack: *reckon-db*, *evoq*, *reckon-gateway*, *reckon-proto*, *reckon-go*, *reckon-dotnet*.

## Reading

The book is published as a PDF on the [releases page](https://github.com/reckon-db-org/reckon-codex/releases) and as a browsable HTML site (link to follow). The PDF is the canonical form.

## Status

Scaffolding stage. Chapter 2 (the D5 model) is the gold-standard reference for the rest. Other chapters are present as stubs and will be filled in subsequent revisions; each stub names what the chapter will cover so the spine is visible even before the prose is.

| Part | Chapter | Status |
|---|---|---|
| Front | Preface, How to read this book | ✅ drafted |
| I | 1. Why event sourcing | ✅ first cut |
| I | 2. The D5 model | ✅ first cut |
| I | 3. Pizza Architecture | ✅ first cut |
| I | 4. Names that scream | ✅ first cut |
| I | 5. Dossiers and Decisions | ✅ first cut |
| I | 6. Pipelines and Process Managers | ✅ first cut |
| I | 7. The Reckon Cycle | ✅ first cut |
| II | 8. reckon-db | ✅ first cut |
| II | 9. evoq | ✅ first cut |
| II | 10. reckon-gateway and reckon-proto | ✅ first cut |
| II | 11. Worked example: a lending library | ✅ first cut |
| III | 12. Antipatterns | ✅ first cut |
| III | 13. Glossary | ✅ first cut |
| Appendix | Reckon and the Critter Stack | ✅ first cut |
| Back | Colophon | ✅ drafted |

## Building locally

The book is built with [Quarto](https://quarto.org/).

```bash
# Install Quarto (see https://quarto.org/docs/get-started/)
quarto --version

# Render to PDF + HTML (output in _book/)
quarto render

# Or just PDF
quarto render --to pdf
```

PDF rendering requires a TeX distribution. The first run installs the necessary packages via `tinytex`:

```bash
quarto install tinytex
```

## Building in CI

Every push to `main` triggers `.github/workflows/build.yml`. The workflow:

1. Sets up Quarto and tinytex.
2. Renders to PDF + HTML.
3. Uploads the PDF as an artifact.
4. On tag push (`v*`), creates a release and attaches the PDF.

## Contributing

Errata, structural feedback, prose corrections welcome via issues or pull requests. The book is intended to evolve with the stack; substantive content changes ship as numbered revisions.

## Licence

- **Prose**: [Creative Commons Attribution-ShareAlike 4.0 International (CC-BY-SA 4.0)](LICENSE-CONTENT). You may share and adapt with attribution and a share-alike licence.
- **Code samples**: [Apache License 2.0](LICENSE-CODE). You may use them in commercial work.

See [`LICENSE`](LICENSE) for the top-level summary.

## Related

- [reckon-db](https://github.com/reckon-db-org/reckon-db) — the event store
- [evoq](https://github.com/reckon-db-org/evoq) — the CQRS/ES framework
- [reckon-gateway](https://github.com/reckon-db-org/reckon-gateway) — the gRPC ingress
- [reckon-proto](https://github.com/reckon-db-org/reckon-proto) — the canonical wire contract
- [reckon-go](https://github.com/reckon-db-org/reckon-go) — idiomatic Go client
- [reckon-dotnet](https://github.com/reckon-db-org/reckon-dotnet) — idiomatic .NET client
