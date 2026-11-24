# Boft's build of cortendesk-server

Boft (photo printing terminals) runs RustDesk's open source server for remote support. This fork builds
cortendesk-server ourselves from its tag, because the binary holds our server's private key.

- Branch `boft-1.5.1` = tag `v1.5.1` (`a0b469e`, hbb_common `229b904`) + this file and `boft-linux.yml`.
  No source changes. Upstream's workflows are removed on the branch, so nothing runs on a push.
- `boft-linux.yml` (manual): the x86_64 musl `hbbs`, `hbbr`, `cortendesk-utils` as upstream's release workflow
  builds them, Rust 1.99.1 (stable when v1.5.1 was released) and cross at `a9301e9` pinned; artifact
  `boft-cortendesk-server-linux-amd64` with SHA256SUMS, COMMIT, HBB_COMMON, RUSTC.
- Why: WebRTC signalling for RustDesk 1.5 clients (the stock hbbs 1.1.16 drops it).
- Licence: AGPL-3.0, as upstream (LICENSE, NOTICE).
