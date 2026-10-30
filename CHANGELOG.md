# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.1] - 2026-10-30

### [Fixed]
- Resolved GitHub Pages deployment failure (`status: 500`) by removing extraneous Windows NTFS `Zone.Identifier` metadata artifact.
- Fixed root artifact archive compatibility for GitHub Pages deployment unpacker.

### [Added]
- Added deterministic GitHub Actions CI/CD deployment pipeline in `.github/workflows/deploy.yml` with explicit OIDC write permissions and concurrency management.
- Configured `.gitignore` to prevent tracking OS metadata (`*:Zone.Identifier`, `.DS_Store`, `Thumbs.db`) and IDE configurations.
- Added `.geminiignore` and `.agentignore` for AI context security and token optimization.
- Added comprehensive repository documentation (`README.md`, `CHANGELOG.md`, `AGENT.md`).

## [1.0.0] - 2026-10-30

### [Added]
- Initial release of Afri-KAD Market landing page (`index.html`) featuring:
  - Tailored color palette and typography (Plus Jakarta Sans & Playfair Display).
  - Responsive navigation with mobile menu drawer.
  - Value proposition and "Prêt à Cuisiner" concept breakdown.
  - Interactive product catalog & pricing cards.
  - Direct WhatsApp order attribution links.
  - Customer review testimonials and FAQ accordion.
