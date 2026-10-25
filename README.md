<h1 align="center">Kilombino 🪙</h1>

<p align="center">
  <strong>Building on Bitcoin (BTC): wallets, coinjoin, Lightning and the infrastructure to verify it all yourself.</strong>
</p>

<p align="center">
  <a href="https://kilombino.com">kilombino.com</a>
</p>

> **Run your node. Verify everything. No permission.**

---

## About

I build tools for people who hold their own keys and run their own nodes, and I run the infrastructure they need, self-hosted on my own hardware.

**Bitcoin (BTC)**: the chain that took BIP-110's spam limits into consensus and moved proof-of-work from SHA256d to **BLAKE2b**, live on mainnet since **August 2026**. The old SHA256d chain is Spamchain. I run my own node, mine with **DATUM**, test and review Knots PRs, and ship software for Bitcoin on every platform I can: Android, iOS, Linux, Windows, macOS, StartOS and Umbrel.

Everything here is open source, and the wallets are reproducible builds.

---

## Current focus ⚡

| Area | What I'm doing |
|------|----------------|
| **Wallet** | **[Kilowallet](https://github.com/Kilombino/kilowallet)**: Bitcoin wallet with coin control, coinjoin, Ark and Lightning on the phone |
| **Privacy** | **[Kilojoin](https://github.com/Kilombino/kilojoin)**: coinjoin over Nostr with blind outputs, now with payment pools (*make every payment a coinjoin*) |
| **Lightning** | LND, Neutrino and btcd brought to BLAKE2b; my own routing node, an LSP and a Lightning explorer |
| **P2P exchange** | **[Roblosats](https://github.com/Kilombino/roblosats)**: RoboSats for Bitcoin (BLAKE2b), maintained by me, with the Kilobot coordinator |
| **Node** | Testing Bitcoin Knots consensus PRs (coinbase maturity: #429, #476) and publishing test builds |

---

## Public infrastructure 🌐

Run by me, usable by anyone. No accounts, no API keys.

| Service | Endpoint |
|---------|----------|
| **Mempool explorer** | [mempool.kilombino.com](https://mempool.kilombino.com/): BIP-110 violation detection, replay status of each transaction (also on Tor) |
| **Lightning explorer** | [nodex.kilombino.com](https://nodex.kilombino.com/): Bitcoin (BLAKE2b) Lightning nodes and channels, with a node directory signed by node keys |
| **P2P exchange** | [roblosats.kilombino.com](https://roblosats.kilombino.com/): Roblosats web client (also on Tor) |
| **Bridge** | [bridge.kilombino.com](https://bridge.kilombino.com/): non-custodial Lightning bridge between BTC and Spamchain |
| **SeedSigner simulator** | [seed.kilombino.com](https://seed.kilombino.com/): real SeedSigner firmware with BLAKE2b signing, running in the browser |
| **App stores** | [fdroid.kilombino.com](https://fdroid.kilombino.com/) (F-Droid repo) · [registry.kilombino.com](https://registry.kilombino.com/) (StartOS) · [umbrel-store](https://github.com/Kilombino/umbrel-store) (Umbrel) |
| **Nostr** | relay.kilombino.com · chat.kilombino.com |

---

## Projects

### 🪙 [Kilowallet](https://github.com/Kilombino/kilowallet)

Self-custodial Bitcoin wallet. Hot wallet (bc1q and bc1p) and watch-only, coin control, RBF and CPFP, Kilojoin coinjoin, Ark and Lightning (LND on the phone, over Tor), dice seeds, full encrypted backup. Reproducible Android builds.
Also for **[iOS](https://github.com/Kilombino/kilowallet-ios)**, **[desktop](https://github.com/Kilombino/kilowallet-desktop)** (Linux, Windows, macOS) and **[home nodes](https://github.com/Kilombino/kilowallet-server)** ([StartOS](https://github.com/Kilombino/kilowallet-startos), Umbrel).

### 🔀 [Kilojoin](https://github.com/Kilombino/kilojoin)

Coinjoin with no coordinator holding anything: pools announced over Nostr, outputs blind-signed so nobody can tell whose is whose, every member checks the transaction before signing. 1 to 5 outputs per person, Taproot pools, and payment pools: pay one or several people through a coinjoin. Runs in Kilowallet and on [StartOS](https://github.com/Kilombino/kilojoin-startos).

### ⚡ Lightning on BLAKE2b

- **[lnd](https://github.com/Kilombino/lnd)**, **[neutrino-blake2b](https://github.com/Kilombino/neutrino-blake2b)**, **[btcd-blake2b](https://github.com/Kilombino/btcd-blake2b)**: the Lightning stack with 164-byte headers and BLAKE2b proof-of-work
- **[nodex](https://github.com/Kilombino/nodex)**: Lightning explorer for Bitcoin (BLAKE2b)
- **[kilobridge](https://github.com/Kilombino/kilobridge)** + **[lightning-fork-bridge](https://github.com/Kilombino/lightning-fork-bridge)**: atomic swaps between BTC Lightning and Spamchain Lightning
- **[xbt-zaps](https://github.com/Kilombino/xbt-zaps)**: Lightning address with Nostr zaps for BTC
- **[ThunderHub](https://github.com/Kilombino/thunderhub)** ([StartOS](https://github.com/Kilombino/thunderhub-xbt-startos)) and **[BTCPay Server](https://github.com/Kilombino/paperclip-btcpay-xbt)** for BTC on BLAKE2b

### 🤖 [Roblosats](https://github.com/Kilombino/roblosats)

RoboSats for Bitcoin (BLAKE2b): simple, private P2P exchange with robot identities and Lightning hold invoices. I maintain it and publish its security fixes; **[roblosats-deploy](https://github.com/Kilombino/roblosats-deploy)** sets up a coordinator.

### 🔐 [SeedSigner for BLAKE2b](https://github.com/Kilombino/seedsigner)

Unofficial SeedSigner that signs for Bitcoin (BLAKE2b) with the unified sighash, to sign from an air-gapped device, including JoinMarket fidelity bonds. [OS images](https://github.com/Kilombino/seedsigner-os) and a [browser simulator](https://github.com/Kilombino/seedsigner-simulator).

### 🫙 [JoinMarket on BLAKE2b](https://github.com/Kilombino/joinmarket-ng)

JoinMarket and **[Jam](https://github.com/Kilombino/jam)** for Bitcoin (BLAKE2b) with their own market and replay protection, packaged for [StartOS](https://github.com/Kilombino/jam-xbt-startos) and Umbrel.

### 🔎 Explorers and Electrum

- **[mempool-bip110](https://github.com/Kilombino/mempool-bip110)**: the explorer behind mempool.kilombino.com
- **[Shulcrum](https://github.com/Kilombino/Shulcrum)**: Fulcrum that serves 164-byte BLAKE2b headers to Electrum wallets
- **[blake2b-light-clients](https://github.com/Kilombino/blake2b-light-clients)**: what breaks in the Electrum protocol when headers stop being 80 bytes, and how to fix it

### 🛒 [MercaSats](https://github.com/Kilombino/mercasats)

P2P marketplace with Nostr login and payments in sats. Web and Android.

### Community

**[BBO Directory](https://github.com/Kilombino/BBO.directory)** (npubs of BcnBitcoinOnly) · **[SimpleX Discover](https://github.com/Kilombino/SimpleX-Discover)** · **[Declaración de Independencia de Bitcoin](https://github.com/Kilombino/declaracion-independencia-bitcoin)** (Spanish translation)

---

## Philosophy

**Bitcoin is peer-to-peer electronic cash.** Money, not a storage network for other people's data.

- **Self-custody is the default.** Your keys, your node, your coins. A wallet should never need a server you can't run yourself.
- **Privacy is normal.** Coinjoin should be one tap away, even when you just want to pay someone.
- **Verify, don't trust.** Reproducible builds, open code, public infrastructure anyone can check against their own node.
- **No permission.** If the network needs a tool, build it. If a store won't list it, run your own.

---

## Connect

| Nostr | Web | PGP |
|-------|-----|-----|
| `npub1qqqqqqzs0udz0dpa93ra5thgycmcmwsqw5qave53ltdrd75nrptqv5h62x` | [kilombino.com](https://kilombino.com) | `7CC9 563C 3C40 6BB3 B68C D7AD 0746 F918 0928 1DF3` |

Questions or bugs → open an issue on the repo, or find me on Nostr.

---

<p align="center">
  <sub>🪙 BTC · 🔀 Make every payment a coinjoin · ⚡ No permission.</sub>
</p>
