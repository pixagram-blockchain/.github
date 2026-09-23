# Pixagram

**Where blockchain meets pixel art.** Pixagram is a social network for pixel art that runs on its own public blockchain. Every artwork is stored fully on chain, and creators and curators are paid directly out of protocol inflation.

The chain is a fork of [Hive](https://hive.io), so the standard Hive RPC surface, tooling and libraries work out of the box. Mainnet has been live since 4 September 2026.

[pixagram.com](https://pixagram.com) · [Documentation](https://pixagram-blockchain.github.io/doc-website/) · [Witness status](https://pixagram.com/witness-status/) · [pixa.org](https://pixa.org)

---

## The chain at a glance

| | |
|---|---|
| Consensus | Delegated Proof of Stake, 3-second blocks |
| Tokens | **PIXA** (liquid), **PXS** (stable, pegged to $1 of PIXA), **VESTS** (staked) |
| Key prefix | `PIX` |
| Public RPC | `https://api.pixagram.com` |
| P2P seed | `api.pixagram.com:2001` |
| Current release | hived **1.29.0**, hardfork 29 active since block 402205 |

Pixagram has **no passive yield by design**. PXS interest and the vesting reward are both fixed at zero in consensus code. Rewards go to people who create, curate and run the network.

## Start here

| I want to… | Repository |
|---|---|
| Understand the chain and its code | [`pixagram`](https://github.com/pixagram-blockchain/pixagram) — the blockchain node (`hived`), C++ |
| Run a witness | [`witness`](https://github.com/pixagram-blockchain/witness) — minimal Docker setup that joins mainnet |
| Run a public API node | [`pixagram-node`](https://github.com/pixagram-blockchain/pixagram-node) — hived, HAF, Hivemind, Jussi and TLS |
| See the reference deployment | [`alphanet`](https://github.com/pixagram-blockchain/alphanet) — the stack behind api.pixagram.com |
| Publish a witness price feed | [`bigmac-feed`](https://github.com/pixagram-blockchain/bigmac-feed) — Go |
| Build an app in JavaScript | [`dpixa`](https://github.com/pixagram-blockchain/dpixa) — RPC client library |
| Give an AI agent chain context | [`pixagram-skill`](https://github.com/pixagram-blockchain/pixagram-skill) — Claude skill with endpoints, tokens and differences from Hive |

Supporting infrastructure: [`haf`](https://github.com/pixagram-blockchain/haf) and [`hivemind`](https://github.com/pixagram-blockchain/hivemind) index the chain for social APIs. [`witness-status`](https://github.com/pixagram-blockchain/witness-status) powers the live witness dashboard.

## Pixel-art toolkit

Open-source libraries behind the Pixagram app, most of them usable on their own:

- **Rendering and scaling:** [`pixagram-upscaler`](https://github.com/pixagram-blockchain/pixagram-upscaler), [`smart-downscaler`](https://github.com/pixagram-blockchain/smart-downscaler), [`depixelize`](https://github.com/pixagram-blockchain/depixelize)
- **Originality checks:** [`paph-js`](https://github.com/pixagram-blockchain/paph-js), a perceptual hash for detecting pixel-art plagiarism
- **On-device safety:** [`toxicity`](https://github.com/pixagram-blockchain/toxicity), [`nsfw`](https://github.com/pixagram-blockchain/nsfw), [`sanitizer`](https://github.com/pixagram-blockchain/sanitizer)
- **Keys and storage:** [`pixa-bip39`](https://github.com/pixagram-blockchain/pixa-bip39), [`pixa-vault`](https://github.com/pixagram-blockchain/pixa-vault), [`LacertaDB`](https://github.com/pixagram-blockchain/LacertaDB)
- **Fast primitives:** [`pixahash`](https://github.com/pixagram-blockchain/pixahash), [`turboserial`](https://github.com/pixagram-blockchain/turboserial), [`heic`](https://github.com/pixagram-blockchain/heic)

## Try it

```bash
curl -s https://api.pixagram.com -H 'Content-Type: application/json' \
  -d '{"jsonrpc":"2.0","method":"condenser_api.get_dynamic_global_properties","params":[],"id":1}'
```

## Governance

Witnesses are elected by stake-weighted vote and produce blocks in turn. Protocol changes ship as hardforks that activate only after enough scheduled witnesses vote for them. Community projects are funded through the **DPF** (Decentralized Proposal Fund), which receives 15 % of inflation.

---

<sub>Pixagram SA · Zug, Switzerland</sub>
