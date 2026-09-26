---
"mattpocock-skills": patch
---

`wizard` now settles where a repo's secrets live before scoping a procedure that captures any. It reads `docs/agents/secrets.md`; on a repo's first wizard, when that file is missing, it asks how secrets are managed and explicitly whether there's an external secret store (Infisical, Vault, 1Password, Doppler, a cloud secret manager), works out how this machine reaches it, and records the access details (never a credential) so later wizards don't ask again. When a store is recorded, each captured secret is written there as well as to `.env` and CI, through a helper below the `STAGES` marker, so the template library is unchanged.
