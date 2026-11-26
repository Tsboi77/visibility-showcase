# tsboi.ai visibility register

Every URL tsboi.ai submits on a client's behalf, recorded per day. Each day is one file plus a SHA-256 of the batch, so a later edit is detectable.

This is the readable register. The tamper-proof version writes each submission as an EAS attestation on Base, timestamped by the chain rather than by us.

| Day | Submissions | Accepted | Files | SHA-256 |
|---|---|---|---|---|
| 2026-11-26 | 75 | 67 | [2026-11-26.md](./2026-11-26.md) · [2026-11-26.json](./2026-11-26.json) | `0b0e50ab9c8b08aa…` |
| 2026-11-25 | 75 | 67 | [2026-11-25.md](./2026-11-25.md) · [2026-11-25.json](./2026-11-25.json) | `b0e314959a207811…` |
| 2026-11-24 | 75 | 67 | [2026-11-24.md](./2026-11-24.md) · [2026-11-24.json](./2026-11-24.json) | `83973e426f97003f…` |
| 2026-11-23 | 75 | 75 | [2026-11-23.md](./2026-11-23.md) · [2026-11-23.json](./2026-11-23.json) | `e68fbdeee30f53da…` |
| 2026-11-22 | 113 | 113 | [2026-11-22.md](./2026-11-22.md) · [2026-11-22.json](./2026-11-22.json) | `0918482f19185ba5…` |
| 2026-11-21 | 113 | 113 | [2026-11-21.md](./2026-11-21.md) · [2026-11-21.json](./2026-11-21.json) | `2bf5eefe259d1329…` |
| 2026-11-20 | 113 | 113 | [2026-11-20.md](./2026-11-20.md) · [2026-11-20.json](./2026-11-20.json) | `9e16653d9a30a516…` |
| 2026-11-19 | 169 | 169 | [2026-11-19.md](./2026-11-19.md) · [2026-11-19.json](./2026-11-19.json) | `05db58077bcac4f5…` |

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
