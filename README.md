# Public project assets

ARROW website assets are attached to tagged releases, starting with
[`arrow-assets-2026-10-02`](https://github.com/ifradlin/storage/releases/tag/arrow-assets-2026-10-02).

Each release contains:

- `arrow-assets.tar.gz`: the website's referenced assets, preserving the `assets/` directory structure.
- `asset-inventory.json`: each file's relative path, byte size, and SHA-256 digest.
- `SHA256SUMS`: checksums for the archive and inventory.

The **Publish ARROW assets** workflow verifies and extracts the release, then
publishes it at <https://ifradlin.github.io/storage/arrow/assets/> using GitHub
Pages. It runs when an `arrow-assets-` release is published, or manually with a
release tag. Publishing a new asset release replaces the served asset snapshot.
Media stays in release attachments rather than Git history.

The browser uses GitHub Pages URLs because release downloads do not provide the
cross-origin access needed by the interactive 3D viewers. Archived exports,
unused images, and export configuration/publish metadata are excluded.
