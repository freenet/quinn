# freenet-quinn (temporary fork of `quinn`)

**Do not depend on this crate. Use upstream [`quinn`](https://crates.io/crates/quinn) instead.**

This is a temporary fork of [quinn-rs/quinn](https://github.com/quinn-rs/quinn)'s `0.11.x` branch,
published only because the Freenet node needs an upstream fix that has been merged to `0.11.x`
but not yet released: [quinn-rs/quinn#2987](https://github.com/quinn-rs/quinn/pull/2987)
("Avoid poisoned-lock panics during cleanup"). A panic in quinn's endpoint driver otherwise
causes a second panic during cleanup, which aborts the process.

The fork contains upstream's `0.11.x` branch unchanged apart from the package renames
(`quinn` to `freenet-quinn`, `quinn-proto` to `freenet-quinn-proto`) and this README.
The library names are unchanged (`quinn`, `quinn_proto`), so it is a drop-in replacement through
Cargo's `package` key.

It will be abandoned once upstream releases the fix. No support is offered.
Source: <https://github.com/freenet/quinn> (branch `freenet-0.11.13`).

Licensed under MIT OR Apache-2.0, as upstream; see the LICENSE files.
