---
title: "Hyperliquid agent wallets and nonce state machine"
url: "https://chainstack.com/hyperliquid-agent-wallets-nonce-state-machine/"
date: "2026-07-29"
author: "Andrey Obruchkov"
feed_url: "https://chainstack.com/feed/"
---
An agent wallet signs for a master without holding funds. The signature commits to exact bytes — Msgpack, nonce, target address, expiration. Here's what each field controls.
