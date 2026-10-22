# theodia.theoscripts

Official Theoscript catalog for the Theodia app.

This repository hosts Theoscript packages (`.theoscript.zip`) and a catalog in this `README.md` so the app can discover and download Theoscripts on demand.

## Layout

```
/
├── README.md
└── <theoscript-id>.theoscript.zip   # Theoscript package zip (latest version)
```

## Catalog

The catalog is published in this README at:

```
https://raw.githubusercontent.com/ecodiallc/theodia.theoscripts/main/README.md
```

| ID | Name | Version | Description | Package |
|---|---|---|---|---|
| theodia.examples | Example Theoscripts | 0.1.0 | Sample scripts demonstrating Theoscript syntax and common tasks. | Theodia-Examples.theoscript.zip |
| theodia.chapter-statistics | Chapter Statistics | 0.1.0 | Counts the words and sentences in a chapter. | Theodia-Chapter-Statistics.theoscript.zip |

## Theoscript packages

A `.theoscript.zip` file is a zip archive containing one or more `.theoscript` source files and a `manifest.json` that describes the package. The zip format mirrors the in-app Theoscript export format:

- `manifest.json` — package metadata (`version`, `exportedAt`, `appVersion`, `exportType`)
- `categories.json` — optional category definitions for imported scripts
- `scripts.json` — script metadata keyed by slug
- `*.theoscript` — source files

The Theoscript version lives only in this catalog table; the package filename is always the latest.

## Authoring Theoscripts

See the [Theoscript syntax documentation](https://github.com/ecodiallc/theodia.theoscripts/wiki) in the repo wiki.
