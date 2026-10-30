# ExponentialTalk 0.2.3

eTalk for Swift: the call machine (the ring, the warm-up, the agent speaks
first; fixture-locked by `voice-call.json`) and the Opus codec (PCM in,
packets out) on iOS 15+ and macOS 12+. Audio I/O and transport stay in the
app. Docs: **https://exponential.at/talk/**; the API:
`apps/desktop/crates/etalk-ffi/README.md` in the monorepo.

```swift
// Package.swift
.package(url: "https://github.com/Niach/exponential-talk-swift", exact: "0.2.3")
// target
.product(name: "ExponentialTalk", package: "exponential-talk-swift")
```

```swift
import ExponentialTalk

let encoder = try TalkEncoder(rate: 16000, bitrate: 24000, lossPercent: 10)
let packet = try encoder.encode(pcm: frame)  // one 20 ms frame of i16 PCM
```

Kotlin: `at.exponential:etalk:0.2.3` on Maven Central. Licence: see
LICENSE and NOTICE. Generated from the Exponential monorepo
(`apps/desktop/crates/etalk-ffi`, tag `etalk-v0.2.3`); issues and
changes go there.
