Taswoq hosting upload package - 2026-11-15

This package was assembled from the current Taswoq_Cleaned working tree, including uncommitted working-copy changes present at build time. It contains the PostgreSQL production server and the complete public web directory.

Before deployment:
1. Read DEPLOYMENT_GUIDE_VPS_CLOUDFLARE.md and POSTGRES_MIGRATION.md.
2. Replace domain and host placeholders in the Nginx configuration and deployment settings.
3. Create real secrets directly on the VPS. .env.production.example is a template only; do not use it as a production secrets file.
4. Confirm the intended production database and take a backup before any schema migration or data import. Those actions are not performed by this package build.
5. Install the service and Nginx configuration according to the guide, then validate them on the VPS before exposing the site.

This is a file bundle only. No VPS upload, database connection, migration, production test, DNS change, commit, or push was performed. It does not establish that the deployment is production-ready.

Excluded intentionally: Git metadata, local JSON databases and backups, real .env files, APKs, signing keystores, tests, local-only server.py, caches, and temporary files.
