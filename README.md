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

I build tools for people who hold their own keys, run their own nodes and mine with their own templates, and I run the infrastructure they need, self-hosted on my own hardware.

**Bitcoin (BTC)**: the chain that took BIP-110's spam limits into consensus and moved proof-of-work from SHA256d to **BLAKE2b**, live on mainnet since **August 2026**. The old SHA256d chain is Spamchain. I run my own node, mine with **DATUM**, test and review Knots PRs, and ship software for Bitcoin on every platform I can: Android, iOS, Linux, Windows, macOS, StartOS and Umbrel.

Everything here is open source, and the wallets are reproducible builds.

---

## Current focus ⚡

| Area | What I'm doing |
|------|----------------|
| **Home nodes** | A signed **[StartOS registry](https://registry.kilombino.com/)** and an **[Umbrel store](https://github.com/Kilombino/umbrel-store)** with the whole BLAKE2b stack: node, Lightning, coinjoin, explorer, exchange |
| **Mining** | **[MRR Command Center](https://github.com/Kilombino/mrr-command-center)**: rent BLAKE2b hashrate and audit that what you pay for reaches your own DATUM gateway |
| **P2P exchange** | **[Roblosats](https://github.com/Kilombino/roblosats)**: RoboSats for Bitcoin (BLAKE2b). Android app, web client and coordinator, now packaged for [StartOS](https://github.com/Kilombino/roblosats-startos) and Umbrel so anyone can [run a coordinator](https://github.com/Kilombino/roblosats-coordinator-startos) |
| **Privacy** | **[JoinBlaket](https://github.com/Kilombino/joinblaket)**: JoinMarket for Bitcoin (BLAKE2b) with its own market, and a guide to [run a directory](https://github.com/Kilombino/joinblaket/blob/xbt/directory-xbt/README.md). **[Kilojoin](https://github.com/Kilombino/kilojoin)**: coinjoin over Nostr with blind outputs and payment pools |
| **Wallet** | **[Kilowallet](https://github.com/Kilombino/kilowallet)**: coin control, coinjoin, Ark and Lightning on Android, iPhone, desktop and home nodes |
| **Lightning** | LND, Neutrino and btcd brought to BLAKE2b; my own routing node, an LSP, a Lightning explorer and a bridge that now pays Lightning addresses |

---

## Run a Bitcoin (BLAKE2b) node 🧭

New here? This is the short path to your own node, with Lightning and mining on top. Each step is an app you install and can update or remove yourself.

| Step | StartOS | Umbrel |
|------|---------|--------|
| **0. Add my store** | Marketplace → add `https://registry.kilombino.com` and my signing key ([copy both here](https://kilombino.com/)) | App Store → Community App Stores → add [`umbrel-store`](https://github.com/Kilombino/umbrel-store) |
| **1. Node** | [Bitcoin Knots](https://github.com/Kilombino/bitcoin-knots-startos) | Bitcoin Knots |
| **2. Lightning** | [Lightning XBT](https://github.com/Kilombino/lightning-xbt-startos) + [ThunderHub](https://github.com/Kilombino/thunderhub-xbt-startos) | Lightning XBT + ThunderHub |
| **3. Mining** | [DATUM Gateway](https://github.com/Kilombino/datum-gateway-startos), with your own block templates | DATUM CONVOY |
| **4. Wallet and privacy** | [Kilowallet](https://github.com/Kilombino/kilowallet-startos), [Kilojoin](https://github.com/Kilombino/kilojoin-startos), [JoinBlaket](https://github.com/Kilombino/jam-xbt-startos) | Kilowallet, JoinBlaket |
| **5. Explorer** | [Mempool](https://github.com/Kilombino/mempool-kilombino-startos) | Mempool |

Every app shows the version you are installing and updates only when you press the button. Step-by-step guides: [Kilowallet](https://kilombino.com/kilowallet/) · [JoinBlaket](https://kilombino.com/joinblaket/).

---

## Public infrastructure 🌐

Run by me, usable by anyone. No accounts, no API keys.

| Service | Endpoint |
|---------|----------|
| **Mempool explorer** | [mempool.kilombino.com](https://mempool.kilombino.com/): BIP-110 violation detection, replay status of each transaction (also on Tor) |
| **Lightning explorer** | [nodex.kilombino.com](https://nodex.kilombino.com/): Bitcoin (BLAKE2b) Lightning nodes and channels, with a node directory signed by node keys |
| **P2P exchange** | [roblosats.kilombino.com](https://roblosats.kilombino.com/): Roblosats web client (also on Tor), with an [interactive tutorial](https://kilombino.com/roblosats/) |
| **Bridge** | [bridge.kilombino.com](https://bridge.kilombino.com/): non-custodial Lightning bridge between BTC and Spamchain; pays invoices, Lightning addresses and LNURL-pay, with a public API |
| **SeedSigner simulator** | [seed.kilombino.com](https://seed.kilombino.com/): real SeedSigner firmware with BLAKE2b signing, running in the browser |
| **App stores** | [fdroid.kilombino.com](https://fdroid.kilombino.com/) (F-Droid repo) · [registry.kilombino.com](https://registry.kilombino.com/) (StartOS) · [umbrel-store](https://github.com/Kilombino/umbrel-store) (Umbrel) |
| **Guides** | [kilombino.com/joinblaket](https://kilombino.com/joinblaket/) (coinjoin with JoinBlaket, step by step) · [kilombino.com/kilowallet](https://kilombino.com/kilowallet/) (downloads and how to verify them) · [bitcoin.kilombino.com](https://bitcoin.kilombino.com/) (why proof-of-work moved to BLAKE2b) |
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

RoboSats for Bitcoin (BLAKE2b): simple, private P2P exchange with robot identities and Lightning hold invoices. I maintain it and publish its security fixes; **[roblosats-deploy](https://github.com/Kilombino/roblosats-deploy)** sets up a coordinator, and there are packages of the client ([StartOS](https://github.com/Kilombino/roblosats-startos), Umbrel) and of the coordinator ([StartOS](https://github.com/Kilombino/roblosats-coordinator-startos), Umbrel) for home nodes.

### 🔐 [SeedSigner for BLAKE2b](https://github.com/Kilombino/seedsigner)

Unofficial SeedSigner that signs for Bitcoin (BLAKE2b) with the unified sighash, to sign from an air-gapped device, including JoinMarket fidelity bonds. [OS images](https://github.com/Kilombino/seedsigner-os) and a [browser simulator](https://github.com/Kilombino/seedsigner-simulator).

### 🫙 [JoinBlaket](https://github.com/Kilombino/joinblaket)

JoinMarket for Bitcoin (BLAKE2b): its own market, replay protection, and makers with fidelity bonds only. With **[Jam](https://github.com/Kilombino/jam)** as the web interface, packaged for [StartOS](https://github.com/Kilombino/jam-xbt-startos) and Umbrel. Anyone can add a [directory](https://github.com/Kilombino/joinblaket/blob/xbt/directory-xbt/README.md) to make the market harder to take down. Guide: [kilombino.com/joinblaket](https://kilombino.com/joinblaket/).

### ⛏️ Mining

- **[MRR Command Center](https://github.com/Kilombino/mrr-command-center)**: rent BLAKE2b hashrate by hand and check it against your own DATUM gateway; when a rental underdelivers, it prepares the evidence for the refund ticket. For [StartOS](https://github.com/Kilombino/mrr-command-center-startos) and Umbrel
- **[sc5-flasher](https://github.com/Kilombino/sc5-flasher)**: dashboard, control panel and software fan curve for the Goldshell SC5 Pro II, with no firmware flashing

### 📦 Apps for home nodes

**[registry.kilombino.com](https://registry.kilombino.com/)** (StartOS, every package signed with my key) and **[umbrel-store](https://github.com/Kilombino/umbrel-store)** (Umbrel) carry what a BLAKE2b node needs: [Bitcoin Knots](https://github.com/Kilombino/bitcoin-knots-startos), [Lightning](https://github.com/Kilombino/lightning-xbt-startos), [ThunderHub](https://github.com/Kilombino/thunderhub-xbt-startos), [Mempool](https://github.com/Kilombino/mempool-kilombino-startos), Kilowallet, Kilojoin, JoinBlaket, Roblosats and MRR Command Center. Registry URL and signing keys to copy: [kilombino.com](https://kilombino.com/).

### 🔎 Explorers and Electrum

- **[mempool-bip110](https://github.com/Kilombino/mempool-bip110)**: the explorer behind mempool.kilombino.com
- **[blake2b-light-clients](https://github.com/Kilombino/blake2b-light-clients)**: what breaks in the Electrum protocol when headers stop being 80 bytes, and how to fix it

### 👁 [Kilombinel](https://github.com/Kilombino/kilombinel)

Sentinel watch-only wallet for Android, rebuilt with a current Tor so it connects again. **For Spamcoin (the old SHA256d chain) only**: it does not follow Bitcoin (BLAKE2b).

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

Questions or bugs → open an issue on the repo, or find me on [kilombino.com](https://kilombino.com).

---

<p align="center">
  <sub>🪙 BTC · 🔀 Make every payment a coinjoin · ⚡ No permission.</sub>
</p>
