This repository contains a Clarity smart contract designed to serve as a secure, audit-friendly escrow mechanism for Web3 agreements. Built to run seamlessly on the Stacks blockchain, this escrow contract integrates with any SIP-010 compliant token (such as stablecoins or wrapped assets) and can be monitored in analytics tools like Google Clarity for transaction insights.

🚀 Key Features

Universal Token Support
Works with any SIP-010 fungible token (STX-wrapped assets, USDT, USDC, etc.).

Safe Escrow Lifecycle

create → Define payer, payee, token, and deadline.

lock → Ensure contract balance is funded before escrow becomes valid.

release → Payer sends funds securely to payee.

refund → Payer reclaims funds if deadline passes and payment not released.

Clear On-Chain Events
Every major action (escrow_created, escrow_locked, escrow_released, escrow_refunded) emits a structured print event for easy off-chain tracking in analytics dashboards (Google Clarity, Microsoft Clarity, or custom Web3 monitors).

Time-Lock Safety
Prevents funds from being locked indefinitely. If not released by the deadline, payer can always reclaim tokens.

Minimal Attack Surface

Uses as-contract execution to ensure only the contract itself performs token transfers.

Strong error handling (ERR-ALREADY-LOCKED, ERR-NOT-PAYER, etc.) for predictable execution.

🛠️ Prerequisites

Stacks Blockchain Dev Environment

Clarinet
 installed locally.

A wallet or devnet setup with SIP-010 compatible tokens.
