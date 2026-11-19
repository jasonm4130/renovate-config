# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) presets.

```json
{ "extends": ["github>jasonm4130/renovate-config"] }
```

- `default.json`: 7-day minimum release age, a weekly grouped non-major PR that merges itself when CI passes, majors and 0.x minors held for review, security fixes without the wait.
- `deploys-on-merge.json`: add `"github>jasonm4130/renovate-config:deploys-on-merge"` after the default where merging deploys something; nothing merges itself.

Registries that report no release time (GHCR, quay.io and others) get no wait rather than a stalled update (`minimumReleaseAgeBehaviour: timestamp-optional`).
