# ecosystem-keepwarm

A tiny GitHub Actions cron that pings the ecosystem's free-tier Render backends every ~10 minutes so real users never hit a ~50-second cold start. Free (public repo → unlimited Actions minutes). To stop: disable the workflow or delete this repo.

**Why there is a `stay-enabled` job:** GitHub silently switches off scheduled workflows in a public repo after 60 days without a commit. That happened on 2026-09-09 and the pings stopped for about two months without anyone noticing. Every run now re-enables the workflow through the API, which resets that clock. Do not remove it.
