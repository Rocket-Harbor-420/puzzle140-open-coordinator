# Bitcoin Puzzle #140 — Open Coordinator

This repository documents a public, browser-based volunteer coordinator for Bitcoin Puzzle #140.

**Live worker:** https://genesis-puzzle-data-hub.tiweedmaster.chatgpt.site/hunt/

## Target

- Address: `1QKBaU6WAeycb3DbKbLBkX7vJiaS8r42Xo`
- Compressed public key: `031f6a332d3c5c4f2de2378c012f429cd109ba07d69690c6c701b6bb87860d6640`
- Range: `[2^139, 2^140)`
- Coordinator puzzle: 140

The browser worker runs Pollard–Kangaroo CPU walks and reports distinguished points and counters to the public coordinator. No private key is sent to the worker.

## Direct payout route

If the key is recovered, the coordinator is configured to build and submit the transaction to the operator wallet:

`bc1qj6lsqs8qwh9n0wjfg43d39zzecxnz73cgp3zrs`

Contributors do not receive a share from this coordinator. Running the worker is voluntary and has no guaranteed reward.

## API

- `GET /api/config` — current puzzle parameters and payout route
- `POST /api/herd` — assign a non-overlapping herd
- `POST /api/dp` — submit distinguished points and jump counters
- `GET /api/stats` — aggregate activity and solution state

The live coordinator is the authoritative runtime. Verify any on-chain result independently before treating it as a payment.

## Status

The target remains unsolved. Source and deployment notes are kept in the WorkMap project while this repository provides a public entry point for online contributors.
