# AI-Built Blockchain: Full Build + Launch Requirements

This document lists **everything required** for me (as your AI engineering agent) to build a production-ready blockchain framework and hand it off for your wallet deployment and Vercel-connected GitHub workflow.

## 1) Product Decisions You Must Confirm First

Before writing code, I need these exact decisions:

1. **Chain type**
   - L1 (new independent blockchain)
   - L2/rollup (on Ethereum, Bitcoin sidechain, etc.)
   - App-chain (Cosmos SDK/Substrate/OP Stack/CDK style)
2. **Primary use case**
   - Payments, DeFi, gaming, identity, RWAs, AI-agent economy, etc.
3. **Performance targets**
   - TPS goal, block time, finality target, max gas per block.
4. **Trust/security model**
   - Permissionless vs permissioned validators, slashing, governance controls.
5. **Token economics**
   - Native token supply model, emissions, fees, burn/mint policy, treasury.
6. **Compliance posture**
   - Jurisdictions, KYC/AML needs, sanctions controls, data retention policies.

## 2) Technical Architecture Inputs I Need From You

## 2.1 Protocol & Consensus
- Consensus mechanism (PoS, PoA, BFT variant, etc.).
- Validator set size at genesis and growth plan.
- Fork/upgrade strategy (hard fork cadence, governance process).
- Chain ID, address format, transaction format.

## 2.2 Smart Contract Runtime
- EVM-compatible or custom VM.
- Solidity/Foundry/Hardhat preference if EVM.
- Precompiles / native modules required.
- Standards required (ERC-20, ERC-721, ERC-1155, ERC-4337, etc.).

## 2.3 Data & State
- Archival requirements and expected chain growth.
- RPC indexer requirements (events, historical queries).
- Off-chain storage needs (IPFS/Arweave/S3 for metadata).

## 2.4 Wallet + Deployment Scope
- Wallets you will use for deployment/signing (e.g., Ledger + MetaMask).
- Multisig requirement for admin keys (recommended: Safe-like setup).
- Hardware security for keys (HSM/Ledger policy).

## 2.5 Website/API Integration Contract
Even if another agent handles frontend, I need:
- API schema (REST/GraphQL), auth model, expected endpoints.
- Contract ABIs and event spec expected by frontend.
- Environment-variable naming convention for Vercel.

## 3) Infrastructure & DevOps Requirements

## 3.1 Cloud/Hosting
- Preferred providers (AWS/GCP/Azure/Hetzner/Bare metal).
- Regions, HA requirements, latency priorities.
- Budget ceiling for infra and monitoring.

## 3.2 Node Topology
- Seed nodes, validator nodes, sentry nodes, public RPC nodes.
- Load balancer and DDoS protection strategy.
- Backup/restore RPO-RTO requirements.

## 3.3 CI/CD + Repos
- GitHub org/repo names.
- Branch protection requirements.
- Required checks (unit, integration, fuzz, lint, SAST, dependency scans).
- Release strategy (tags, changelog, semantic versioning).

## 3.4 Vercel Connection Inputs
- GitHub repo that Vercel should track.
- Build command/output directory expectations.
- Domain and DNS ownership/access.
- Secrets to inject in Vercel (RPC URLs, chain IDs, contract addresses).

## 4) Security Requirements (Mandatory)

1. **Threat model document** (assets, adversaries, trust boundaries).
2. **Key management policy** (who controls deployer, pause, upgrade, treasury keys).
3. **Multisig governance** for privileged operations.
4. **Audit plan**
   - Internal review checklist
   - External audit vendor scope
   - Critical fix SLA
5. **Testing depth**
   - Unit + integration + invariant + fuzz + fork testing.
6. **Runtime monitoring**
   - On-chain anomaly detection
   - Node health checks
   - Alerting (PagerDuty/Slack)
7. **Incident response runbook**
   - Pause/kill-switch policy (if applicable)
   - Public communications plan
   - Postmortem template

## 5) Legal/Policy Inputs (You provide counsel)

I can implement controls, but I cannot be your lawyer. You need:
- Entity setup and legal counsel sign-off.
- Terms of service + privacy policy + risk disclosures.
- Token issuance legal memo for target jurisdictions.
- Sanctions and restricted-region policy.
- Consumer protection/disclaimer language.

## 6) Deliverables I Can Produce End-to-End

Given the above inputs, I can deliver:

1. **Protocol repository**
   - Chain config, genesis tooling, localnet/devnet scripts.
2. **Smart contracts repository**
   - Core token/contracts, tests, deployment scripts.
3. **Infrastructure-as-code repository**
   - Terraform/Ansible/K8s for nodes + observability.
4. **Ops repository/docs**
   - Runbooks, incident playbooks, upgrade guides.
5. **Integration package for frontend agent**
   - ABI bundle, API schema, typed SDK, env templates.
6. **Launch kit**
   - Mainnet readiness checklist, rollback plan, go/no-go criteria.

## 7) Exact Access/Secrets Needed From You

Provide via secure channel (never plain chat):

- GitHub org/repo admin access (or maintainers).
- Vercel project access (or service token).
- Domain registrar/DNS access for production domain.
- Cloud account roles for infra provisioning.
- Multisig member addresses and key policy.
- Optional: testnet funds and faucet credentials.

## 8) Suggested Build Plan (Phased)

1. **Phase 0: Discovery (3-7 days)**
   - Finalize requirements + threat model + chain architecture.
2. **Phase 1: Prototype (1-3 weeks)**
   - Localnet chain + basic contracts + minimal RPC.
3. **Phase 2: Testnet (2-6 weeks)**
   - Public testnet, explorer/indexer, wallet integrations.
4. **Phase 3: Security hardening (2-6 weeks)**
   - Audits, fuzzing, invariants, infra resilience tests.
5. **Phase 4: Mainnet launch readiness (1-2 weeks)**
   - Governance setup, incident drills, final release candidates.

## 9) What I Need From You Right Now (Checklist)

Reply with:

1. Chain choice (L1 / L2 / app-chain) and why.
2. EVM-compatible? (yes/no)
3. Consensus choice.
4. Expected TPS + block time + finality.
5. Token model summary.
6. Target launch date and budget range.
7. Jurisdictions and compliance constraints.
8. Preferred cloud provider.
9. GitHub org + repo naming.
10. Wallet/security setup (hardware wallet + multisig addresses).

Once you provide these 10 items, I can produce a concrete technical blueprint and implementation backlog ready for GitHub + Vercel-connected deployment.
