# Changelog

All notable changes to **satware(R) AI Canvas** are documented here.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed
- Public mirror initialized and CI auto-mirror verified (runs 17099-17104)

## [1.0.0] - 2026-08-24

### Added
- Frankenstein unification of the canvas plugin exports from chat.demo.satware.ai and chat.satware.ai (byte-identical function code; metadata differences merged)
- `render_interactive_canvas`: full HTML document render (outputType render_html)
- `update_interactive_canvas`: incremental find-and-replace patches via previousRunOutput
- Fleet conformance: hybrid pattern (GitHub-hosted primary fn), bilingual DE/EN overview, per-tool guidance consolidated into single `canvas-environment-constraints` context entry
- From demo export: iconURL asset + example prompts
