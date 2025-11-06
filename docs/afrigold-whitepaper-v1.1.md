# AfriGold (AFGD) — Whitepaper v1.1

**Date:** 2025-11-06  
**Network:** Solana Mainnet  
**Mint:** `8KbB5DkHTS3ZwWqwe1FUgZvR8kQJWPafU7CRrUL1RjKG`  
**Program:** SPL **Token-2022** (Transfer Fee extension)  
**Decimals:** 9  
**Website:** https://afrigold-dev.github.io/afrigold-assets/  
**JSON Metadata (immutable):** https://raw.githubusercontent.com/Afrigold-dev/afrigold-assets/main/listing-pack/afrigold-v2-mainnet.json

---

## 1. Executive Summary

AfriGold (AFGD) is a fixed-supply community token on Solana using **Token‑2022** with a modest **1% transfer fee (capped at 0.05 AFGD per transfer)** to fund development, marketing and charitable initiatives. The token’s brand and metadata (name, symbol, URI) are locked on-chain; the mint and freeze authorities are revoked, making the supply permanent.

**Key properties**
- **Chain:** Solana (fast, low-fee, high-throughput)  
- **Supply cap:** 1,000,000,000 AFGD (fixed); **current minted ≈ 999,976,819.58975806 AFGD**  
- **Transfer fee:** 1.00% with a **hard cap of 0.05 AFGD** per transfer  
- **Immutability:** Metadata locked; mint & freeze authorities not set  
- **Liquidity:** Initial pool on **Raydium** (AMM ID `BUV4vgrkMARGvsnL4h4pmRxv941mZH4d4VDz3mwFqpxB`) paired with USDC  
- **Socials:** Twitter/X https://x.com/AfgdAfrigold · Telegram https://t.me/AFGD_Official · Website https://afrigold-dev.github.io/afrigold-assets/

---

## 2. Mission & Rationale

AfriGold aims to cultivate an energized community around a simple, verifiable token with transparent funding for ongoing development and outreach. The transfer‑fee model is designed to be **predictable** (capped) and to avoid the runaway “tax” dynamics found in some fee tokens. Fees are collected by the protocol and later withdrawn by the project’s withdrawal authority for distribution to public wallets.

---

## 3. Token Specification

- **Mint:** `8KbB5DkHTS3ZwWqwe1FUgZvR8kQJWPafU7CRrUL1RjKG`  
- **Program:** SPL Token‑2022 (Transfer Fee Extension)  
- **Decimals:** 9  
- **Ticker:** AFGD · **Name:** AfriGold  
- **Logo:** https://raw.githubusercontent.com/Afrigold-dev/afrigold-assets/main/afrigold.png  
- **Metadata URI (immutable):** https://raw.githubusercontent.com/Afrigold-dev/afrigold-assets/main/listing-pack/afrigold-v2-mainnet.json  
- **Authorities:**  
  - **Mint authority:** _not set_ (supply locked)  
  - **Freeze authority:** _not set_  
  - **Fee config & withdrawal authority:** `FZSC3GKVMA9X3Y1XzEH3ose1zzUCnXqYuGKJhL9PPfdr`

---

## 4. Transfer Fee Policy

- **Rate:** 1% of the transferred amount  
- **Absolute cap:** 0.05 AFGD per transfer  
- **Collection:** Fees accumulate in recipient token accounts and are **harvestable only** by the withdrawal authority (Token‑2022 mechanism).  
- **Distribution policy (initial):**
  - **Development — 50%:** `HTCN3h8ZZR7Pq1y7gnoES6iBBBQZUGgGJsoKBGVJy1Ek`  
    Explorer: https://explorer.solana.com/address/HTCN3h8ZZR7Pq1y7gnoES6iBBBQZUGgGJsoKBGVJy1Ek
  - **Marketing & Charity — 50%:** `5qe9R5dW7q6n8UAiYVQAPgfo17w1jiJXeRqCvsyKvERx`  
    Explorer: https://explorer.solana.com/address/5qe9R5dW7q6n8UAiYVQAPgfo17w1jiJXeRqCvsyKvERx
- **Cadence:** **Weekly on Fridays**. After harvesting, on‑chain tx links are posted to **Telegram**.

> _Note:_ Token‑2022 does not auto‑split fees. Harvesting and distribution are executed by the withdrawal authority. Ratios and addresses can be adjusted by governance (and then updated here).

---

## 5. Liquidity & Market Structure

- **Primary AMM:** Raydium  
- **Pool (AMM ID):** `BUV4vgrkMARGvsnL4h4pmRxv941mZH4d4VDz3mwFqpxB`  
- **Base pair:** AFGD / USDC  
- **Policy:** Seed initial liquidity, monitor depth & slippage, and top up opportunistically. Publish short updates after significant changes.

---

## 6. Governance & Transparency

- **Current admin key (fee/withdrawal/metadata update authority):** `FZSC3GKVMA9X3Y1XzEH3ose1zzUCnXqYuGKJhL9PPfdr`  
- **Planned controls:** evaluate migration to a **multisig** as the community grows; publish a public ledger of fee harvests and distributions.  
- **Auditability:** All addresses are public; metadata is immutable; mint is revoked.

---

## 7. Roadmap (initial)

- **Q4 2025** — CoinGecko submission; site/docs polish; publish fee wallets & first distribution report.  
- **Q1 2026** — Optional multisig migration; fee/distribution dashboard; additional listings.  
- **Q2 2026** — Community micro‑grants funded from the marketing/charity allocation; regional meetups.

---

## 8. Risks & Disclosures

Crypto assets are volatile and can lose value. AfriGold does **not** represent a security, equity claim, or promise of profit. No guarantee of liquidity, listings, or future utility is made. Users must comply with their local laws and accept all risks when interacting with on‑chain systems.

---

## 9. Official Links

- **Website:** https://afrigold-dev.github.io/afrigold-assets/  
- **Metadata JSON:** https://raw.githubusercontent.com/Afrigold-dev/afrigold-assets/main/listing-pack/afrigold-v2-mainnet.json  
- **Explorer (Mint):** https://explorer.solana.com/address/8KbB5DkHTS3ZwWqwe1FUgZvR8kQJWPafU7CRrUL1RjKG  
- **Raydium Pool:** https://raydium.io/pools/?ammId=BUV4vgrkMARGvsnL4h4pmRxv941mZH4d4VDz3mwFqpxB  
- **Twitter/X:** https://x.com/AfgdAfrigold  
- **Telegram:** https://t.me/AFGD_Official

---

## 10. Contact

**Primary contact (Telegram):** `@AfriGold_AFGD`

---

### Appendix — Token‑2022 Notes
- Transfer‑fee collection & withdrawal occur at the mint level via the **Token‑2022 Transfer Fee** extension.  
- The **fee configuration authority** can adjust fee parameters if retained; otherwise it can be renounced later.  
- **Metadata immutability:** name, symbol and URI are locked (`isMutable=false`).
