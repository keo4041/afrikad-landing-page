# AGENT.md - Project Context & Operational State

## 1. Project Overview & Identity
- **Repository:** `afrikad-landing-page` (`keo4041/afrikad-landing-page`)
- **Domain:** Afri-KAD Market (Fresh prepared meal kits / "Prêt à Cuisiner" in Lomé, Togo)
- **Architecture:** Zero-build static web application (Tailwind CSS CDN, Google Fonts, Vanilla JavaScript) deployed directly to GitHub Pages.

---

## 2. Infrastructure & CI/CD Pipeline
- **Deployment Strategy:** GitHub Actions workflow ([`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)).
- **Permissions:** `contents: read`, `pages: write`, `id-token: write`.
- **Target Host:** GitHub Pages Edge CDN.
- **Troubleshooting Note:** Previous deployment error `HttpError: Failed to create deployment (status: 500)` was traced to an unhandled NTFS `Zone.Identifier` stream file with a colon in the filename inside the tarball artifact. The file has been excised and filtered out in `.gitignore`.

---

## 3. Directory Layout & Key Artifacts
- [`index.html`](index.html): Production entry point containing full UI, styling configs, and client interaction scripts.
- [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml): Official static Pages deployer.
- [`.gitignore`](.gitignore): OS, editor, and build artifact exclusions.
- [`.agentignore`](.agentignore) / [`.geminiignore`](.geminiignore): Context exclusion patterns.
- [`README.md`](README.md): System architecture, local setup instructions, and deployment guide.
- [`CHANGELOG.md`](CHANGELOG.md): SemVer release history.

---

## 4. Operational Boundaries & Rules for Future Agent Sessions
1. **Never commit OS metadata:** Keep NTFS streams (`*:Zone.Identifier`) and macOS `.DS_Store` out of git commits.
2. **Preserve Documentation Triad:** Always update `CHANGELOG.md`, `README.md`, and `AGENT.md` after any functional, deployment, or structural change.
3. **No Unverified AI Logic:** If dynamic API endpoints or backend order databases are added in future iterations, adhere to the Deterministic Verification Layer principles outlined in global rules.
