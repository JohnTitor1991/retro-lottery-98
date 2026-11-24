# Retrò Lottery 98

![Network](https://img.shields.io/badge/Network-BNB%20Smart%20Chain-F0B90B?style=flat-square)
![Randomness](https://img.shields.io/badge/Randomness-Chainlink%20VRF%20v2.5-375BD2?style=flat-square)
![Execution](https://img.shields.io/badge/Execution-Chainlink%20Automation-375BD2?style=flat-square)
![Contract](https://img.shields.io/badge/Contract-Verified%20on%20BscScan-2E8555?style=flat-square)

A fully autonomous, non-custodial **CAKE** lottery on **BNB Smart Chain Mainnet**, wrapped in a lightweight **Windows 98 desktop interface**.

**Live dApp:** [https://retrolottery98.com](https://retrolottery98.com)

![Retrò Lottery 98 Desktop UI](./preview.png)

## Overview

**Retrò Lottery 98** strips away heavy DeFi dashboards and centralized trust assumptions. The frontend is a fast static web app hosted on Cloudflare Pages that communicates directly with a verified Solidity smart contract—no user accounts, no backend database, no KYC, and no manual admin draw trigger.

## Core Architecture

* **Non-Custodial by Design:** Players connect any standard Web3 wallet and interact directly with the smart contract on BNB Smart Chain. Funds never touch a centralized wallet.
* **Provably Fair Randomness (Chainlink VRF v2.5):** Winner selection is computed cryptographically on-chain via Chainlink VRF v2.5 (funded with native BNB). Draws cannot be predicted or manipulated by the deployer or any participant.
* **Autonomous Execution (Chainlink Automation):** Round closures, VRF requests, prize payouts, and refunds are triggered automatically by Chainlink Automation.
* **Anti-Lock Refund Mechanism:** If a round closes with fewer than **5 tickets**, the contract skips the draw and automatically triggers refunds so funds can never become stuck in an under-subscribed round.

## Protocol Economics & Parameters

| Parameter | Value |
| :--- | :--- |
| **Network** | BNB Smart Chain (BSC Mainnet) |
| **Ticket Currency & Price** | 1 CAKE per ticket (BEP-20) |
| **Winner Payout** | 95% of the prize pool (sent automatically to the winners) |
| **Protocol Fee** | 5% flat (covers Chainlink VRF & Automation upkeep) |
| **Minimum Threshold** | 5 tickets per round (auto-refund if not met) |

## On-Chain Verification

* **Live dApp:** [https://retrolottery98.com](https://retrolottery98.com)
* **Smart Contract (BSC Mainnet):** `0xCec1F2845C979D19d1fD9cAf06C6BDC58D8EE57B`
* **Verified Source on BscScan:** [View Contract on BscScan](https://bscscan.com/address/0xCec1F2845C979D19d1fD9cAf06C6BDC58D8EE57B#code)
* **Contract File in this Repo:** [`contracts/RetroLottery98.sol`](./contracts/RetroLottery98.sol)

## Technical Write-Ups

* **DEV.to:** [Architecture Breakdown on DEV.to](https://dev.to/john_titor_1991/i-built-a-non-custodial-cake-lottery-with-a-windows-98-ui-and-chainlink-vrf-v25-2ogl)
* **Hashnode:** [Architecture Breakdown on Hashnode](https://retrolottery98.hashnode.dev/)
* **Paragraph:** [Project Overview on Paragraph](https://paragraph.com/@retrolottery98/preview/EVoCMrt43dYmOT6zsv2e)

## Disclaimer

Retrò Lottery 98 is an independent, experimental Web3 project provided as-is. Always inspect the verified smart contract on BscScan before interacting and ensure compliance with your local regulations.
