# tsboi.ai visibility register

Every URL tsboi.ai submits on a client's behalf, recorded per day. Each day is one file plus a SHA-256 of the batch, so a later edit is detectable.

This is the readable register. The tamper-proof version writes each submission as an EAS attestation on Base, timestamped by the chain rather than by us.

| Day | Submissions | Accepted | Files | SHA-256 |
|---|---|---|---|---|
| 2026-11-19 | 169 | 169 | [2026-11-19.md](./2026-11-19.md) · [2026-11-19.json](./2026-11-19.json) | `01b8e3c4fa2be4d2…` |

## What is in each entry

| Field | Meaning |
|---|---|
| ts | UTC timestamp of the submission call |
| engine | google, indexnow or exa |
| url | the exact URL submitted |
| ok | whether the engine accepted it |
| status | HTTP status returned |

## Verify

Recompute SHA-256 over the JSON with the `sha256` field removed. Any change to the batch breaks the hash.
