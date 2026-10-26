# onioncrawler

Darknet (.onion/.i2p) crawler: the anti-leak host gate expressed as a type, URL canonicalizer, language guess, SOCKS5 fetch, storage, no-JS search.

Part of the [astrx suite](https://github.com/Vxmdzhb/astrx-suite): one of its engines. The suite repository assembles every engine into the single `astrx` binary (`astrx onioncrawler`) and deploys it.

## Build

    cargo build --release --features net   # the `onioncrawler` binary
    cargo test --all-features

Features: `rand`, `net`. The default build uses the standard library only; `net` (and `rand`) add the suite's two vetted dependencies, tokio and getrandom. CI asserts the default build stays first-party.

## History

This repository was split out of https://github.com/Vxmdzhb/astrx-suite with the full history of its files, each followed back through its renames. The cross-check goldens are explained in [GOLDENS.md](GOLDENS.md).
