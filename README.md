# theodia.theoscripts

| ID | Name |
| --- | --- |
| `theodia.examples` | Example Theoscripts |
| `theodia.chapter-statistics` | Chapter Statistics |

Official Theoscript catalog for the Theodia app.

This repository hosts Theoscript packages (`.theoscript.zip`) and a catalog in `index.json` so the app can discover and download Theoscripts on demand.

## Catalog

The app reads the machine-readable catalog in `index.json` at:

```
https://raw.githubusercontent.com/ecodiallc/theodia.theoscripts/main/index.json
```

`index.json` is the authoritative catalog. The table above is a human-readable mirror of it.

## Layout

```
/
├── README.md
├── index.json
└── <theoscript-id>.theoscript.zip   # Theoscript package zip (latest version)
```

## Theoscript packages

A `.theoscript.zip` file is a zip archive containing one or more `.theoscript` source files and a `manifest.json` that describes the package. The zip format mirrors the in-app Theoscript export format:

- `manifest.json` — package metadata (`version`, `exportedAt`, `appVersion`, `exportType`)
- `categories.json` — optional category definitions for imported scripts
- `scripts.json` — script metadata keyed by slug
- `*.theoscript` — source files

The Theoscript version lives only in this catalog; the package filename is always the latest.

## Authoring Theoscripts

The scripts are defined in the app repo (`src/theoscripts/sources.ts`) and packaged with `npm run package-theoscripts`, which writes both the archives and `index.json`.

See the [Theoscript syntax documentation](https://github.com/ecodiallc/theodia.theoscripts/wiki) in the repo wiki.

## Sources

- `theodia.examples` — sample scripts demonstrating the Theoscript syntax.
- `theodia.chapter-statistics` — counts the words and sentences in a chapter.
