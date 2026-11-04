# Repository import

- [x] Download and inspect source without credentials or repository metadata.
- [x] Import source pages, styles, assets and service code 1:1 (2356 src + 109 public files, 409 routes).
- [x] Reconcile dependencies and shared components (bun install clean, build OK).
- [x] Verify public homepage, documentation routes and account pages in a browser.
- [x] Run the imported test suite (1979/1982 tests pass).
- [x] Connect the user's own Neon database (DATABASE_URL, PUBLIC_ORIGIN, BETTER_AUTH_SECRET saved; live reads, sign-in form and signed-out dashboard redirect verified).
- [ ] Link the user's own Supabase — user action: project settings → General → External Supabase → Connect. Blocks /about and /explore (HTTP 500).
- [ ] Request remaining provider keys as features are tested (Stripe, bunq, Bluesky, Mastodon, Spotify, YouTube, Steam, Last.fm, Telegram, Snapchat, weather, OMNI, ROUT OAuth, NEON_API_KEY).
- [ ] Regenerate `db/schema.snapshot.json` (stale vs migrations: `agent_sandboxes`, 8 `rout_agent_sandbox_*` functions, `agent_workspace_claims` columns) — pre-existing in the source repo.
- [ ] Fix `src/test/smoke/privacy.test.ts` false positive (`gtag\(` matches `qr.createSvgTag(`) — pre-existing in the source repo.
- [ ] Decide cutover: does this project replace the original deployment (webhooks, cron, OAuth redirect URIs)?
