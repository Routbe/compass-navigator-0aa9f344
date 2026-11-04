# Repository import

- [x] Download and inspect source without credentials or repository metadata.
- [x] Import source pages, styles, assets and service code 1:1 (2356 src + 109 public files, 409 routes).
- [x] Reconcile dependencies and shared components (bun install clean, build OK).
- [x] Verify public homepage, documentation routes and account pages in a browser.
- [x] Run the imported test suite (1979/1982 tests pass).
- [ ] Connect the database backend — blocked on the user's choice: Lovable Cloud or their own Neon + Supabase.
- [ ] Restore account/data and connected services — blocked by compatible external service configuration and original data access.
- [ ] Regenerate `db/schema.snapshot.json` (stale vs migrations: `agent_sandboxes`, 8 `rout_agent_sandbox_*` functions, `agent_workspace_claims` columns) — pre-existing in the source repo.
- [ ] Fix `src/test/smoke/privacy.test.ts` false positive (`gtag\(` matches `qr.createSvgTag(`) — pre-existing in the source repo.
- [ ] Import existing records and users once exports are supplied.
- [ ] Decide cutover: does this project replace the original deployment (webhooks, cron, OAuth redirect URIs)?
