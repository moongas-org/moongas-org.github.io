# moongas-org.github.io

Welcome to the **Moongas Organization** GitHub Pages website.

## About

This repository hosts the organization’s public website. It was created as a public GitHub Pages project.

## Repository

- [moongas.org](https://moongas.org)
- [github.com/moongas-org](https://github.com/moongas-org)
- [github.com/moongas-org/moongas-org.github.io](https://github.com/moongas-org/moongas-org.github.io)

## Organization repositories

The Moongas organization maintains these public repositories:

- [moongas-collection-demo](https://github.com/moongas-org/moongas-collection-demo) — Canonical example of a Moongas media collection, containing metadata only and no audio files.
- [moongas-mediascan-go](https://github.com/moongas-org/moongas-mediascan-go) — Go command-line utility that scans media files, extracts metadata such as ID3v2 tags, and saves it to an SQLite database.
- [moongas-mediascan-python](https://github.com/moongas-org/moongas-mediascan-python) — Python library for reading Moongas mediascan databases and metadata files.
- [moongas-mediascripts-python](https://github.com/moongas-org/moongas-mediascripts-python) — Python scripts for working with Moongas media collections.
- [moongas-mediatest-python-pytest](https://github.com/moongas-org/moongas-mediatest-python-pytest) — Pytest component for enforcing rules on media libraries.
- [moongas-mediatunes-svc-java-javalin](https://github.com/moongas-org/moongas-mediatunes-svc-java-javalin) — Java and Javalin API service for hybrid media collections, used by the Moongas mediatunes web application.
- [moongas-mediatunes-svc-python-blacksheep](https://github.com/moongas-org/moongas-mediatunes-svc-python-blacksheep) — Python and BlackSheep API service for hybrid media collections, used by the Moongas mediatunes web application.
- [moongas-mediatunes-web-vue](https://github.com/moongas-org/moongas-mediatunes-web-vue) — TypeScript and Vue single-page application for hybrid media collections, blending offline and streaming playback.
- [moongas-org.github.io](https://github.com/moongas-org/moongas-org.github.io) — Source for this public GitHub Pages website.


## The Philosophy of Moongas

### Moongas is chronological

Moongas is meant to be a historical archive of popular music culture. One of the original goals of this collection was to be able to filter music by time period (example use case: 80s dance party). In traditional music collections, the _year_ tag is usually set to the release year of the particular album-pressing, which is often a compilation or a re-release. This makes year sorting not particularly useful, since you may ask for 1990s music and get Paul McCartney. Moongas solves this by adhering to the following rules:

- Moongas album entries do not correspond to specific pressings or releases but to an album in the abstract sense, therefore qualifiers such as _(Deluxe Edition)_, _(Explicit)_, etc. are stripped from the album name.
- The year of an album is always set to the original or oldest year (typically the year it was recorded, or the year of the original release)
- Compilation albums are not allowed. Moongas provides scripts like `move_from_various_artists.py` to decompose compilation albums and move the tracks into appropriate individual artist and album directories.
- `albumartist` tags are required and must match the album directory name (after escaping) and must be consistent throughout an album.
- `artist` tags are required and may differ from `albumartist` on a per-track basis.
- Album directory names are required to contain the year in square brackets
