# thesis_oracle

## Project Title
thesis_oracle

## Project Description
thesis_oracle is a Soroban smart contract that acts as an on-chain registry for university thesis defenses. A candidate (student) registers a thesis by committing its title hash and an identifier, committee members cast one approval or rejection vote each, and the chair finalizes the defense to record a tamper-proof verdict that anyone can later verify.

## Project Vision
To give academic institutions a transparent, censorship-resistant record of thesis defenses. By anchoring proposals, votes, and final outcomes on Stellar, the project aims to reduce fraud, simplify audits, and let graduates carry a portable, verifiable proof of their academic milestones across institutions and borders.

## Key Features
- Proposal registration: students commit a thesis_id and title hash on-chain, creating a canonical record of the work submitted for defense.
- Committee voting: every committee member authenticates with their Stellar address and casts a single approve/reject vote; duplicate votes are rejected.
- Chair-gated finalization: only the registered chair can tally the votes and lock the result, preventing premature or unauthorized verdicts.
- Public verifiability: vote count, approval count, rejection count, and the final result are readable by anyone, enabling post-defense audits.
- Storage-and-logic focused: no XLM transfers are involved, keeping the contract lightweight and easy to integrate with a future frontend or backend.

## Contract

- **Network:** Stellar Testnet (Public)
- **Scope:** education dApp — see `contracts/thesis_oracle/src/lib.rs` for the full thesis_oracle business logic.
- **Functions exposed:** see `Key Features` above and the `pub fn` list in `lib.rs`.
- **Contract ID:** `CBNQ4KY7ZWGD3JKWVLCHJW5ZU4CVVON5FY4SATOLVPUH5GAXZFIXFHK3`
- **Explorer template:** `https://stellar.expert/explorer/testnet/tx/e340a0ef32d313f8954c7ae0265310885ce913ad6bc46d02dce70aa657891427`


## Future Scope
- Multi-committee support: allow several distinct committees to manage defenses in parallel under the same contract instance.
- Weighted voting: let the chair assign different vote weights to internal vs. external reviewers.
- Frontend dApp: build a React/TypeScript client that lets students submit proposals and committee members vote from a Stellar wallet (Freighter).
- Appeal and revision flows: add a path for candidates to submit a revised thesis after a rejection and re-enter the defense cycle.
- Off-chain title storage with on-chain proof: store the full thesis PDF on IPFS and keep only its content hash on-chain, while preserving the same verification guarantees.

## Profile

- **Name:** <!-- Fill github name -->
- **Project:** `thesis_oracle` (education)
- **Built with:** Soroban SDK 25, Rust, Stellar Testnet
