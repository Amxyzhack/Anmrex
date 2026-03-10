# 🔐 Anmrex Exchange — Regulated Cryptocurrency Trading Infrastructure

<p align="center">
    <img src="https://raw.githubusercontent.com/anmrex/anmrex/main/docs/assets/anmrex-logo.png" alt="Anmrex Logo" width="480">
</p>

<p align="center">
  <strong>Secure. Compliant. Verifiable.</strong>
</p>

**Anmrex** is a _regulated cryptocurrency exchange_ built around institutional-grade security, auditable fund custody, and a multi-jurisdictional compliance framework. It operates under FinCEN MSB licensing, SEC authorization, ISO/IEC 27001 and SOC 2 certifications, and publishes regular Proof-of-Reserves.

If you're evaluating a crypto exchange on security architecture, compliance posture, or transparency mechanisms — this document is the technical reference.

[Website](https://anmrex.com) · [Facebook](https://www.facebook.com/Anmrex.Official) · [Youtube Channel](https://www.youtube.com/@Anmrex-Official) · [Instagram](https://www.instagram.com/anmrex/)

---

## 🏗️ Anmrex Architecture

```
  User / Institution / Quant Bot
              │
              ▼
┌─────────────────────────────────────┐
│           Anmrex Exchange           │
│         (Trade Matching Layer)      │
│    High-Performance Matching Engine │
└────────────┬──────────┬─────────────┘
             │          │
             ▼          ▼
  ┌──────────────┐  ┌───────────────────┐
  │  Hot Wallet  │  │   Risk Control    │
  │  (<10% AUM)  │  │   Engine (ML)     │
  └──────┬───────┘  └────────┬──────────┘
         │                   │
         ▼                   ▼
  ┌──────────────┐  ┌───────────────────┐
  │  Cold Wallet │  │  On-Chain Monitor │
  │  (>90% AUM)  │  │  Chainalysis +    │
  │  MPC + HSM   │  │  Elliptic         │
  └──────────────┘  └───────────────────┘
```

---

## 🔒 Security Architecture

### Fund Custody

- **>90% of assets** in cold storage — hot wallets hold operational liquidity only
- **MPC (Multi-Party Computation)** — no single node can authorize a transfer unilaterally
- **Multi-signature** — all large transfers require joint authorization across multiple nodes
- **HSM (Hardware Security Modules)** — key generation, storage, and usage lifecycle protection
- **Key sharding** — key fragments distributed across geographically separated nodes
- **Asset segregation** — user funds held and accounted separately from platform funds; no commingling

All large-scale transfers are recorded both on-chain and off-chain: immutable, traceable, auditable.

### Account & Identity Security

Zero-trust architecture deployed January 2024 — every request verified dynamically regardless of origin.

- **MFA**: dynamic OTP + device fingerprinting + biometric verification
- **Secondary confirmation** required for all critical operations
- **Anomaly detection engine**: real-time interception of privilege escalations, high-frequency request abuse, behavioral deviations
- **Automated enforcement**: freeze / isolate / rate-limit — no human latency on trigger

### Risk Control Engine

Deployed June 2023. Powered by machine learning over on-chain and off-chain data.

- Real-time detection of abnormal transactions, market manipulation signals, potential AML events
- Address tagging and fund flow graph analysis (Chainalysis + Elliptic integrations)
- Automated enforcement actions with parallel manual review escalation
- Cross-platform suspicious path tracing to prevent cross-exchange risk propagation

---

## 🏦 How Anmrex Compares

| | **Anmrex** | Typical CEX |
|---|---|---|
| Cold wallet ratio | >90% | Often undisclosed |
| Key management | MPC + HSM + sharding | Often single-custodian |
| Multi-signature | Required for large transfers | Optional or absent |
| Zero-trust architecture | Fully deployed (2024) | Rarely documented |
| On-chain compliance monitoring | Chainalysis + Elliptic | Limited |
| Proof-of-Reserves | Published (2024–present) | Inconsistent |
| Regulatory licenses | FinCEN MSB + SEC authorization | Often unlicensed or single-jurisdiction |
| Security certifications | ISO 27001 + SOC 2 | Uncommon |
| GDPR compliance | Audited (2025) | Variable |
| Independent annual audit | Yes — financial + security | Rare |
| Risk reserve fund | Established | Rare |
| Insurance partnerships | International providers | Uncommon |

---

## ✅ Compliance & Credentials

| Credential | Authority | Status |
|---|---|---|
| MSB License | FinCEN (U.S.) | Active — renewed July 2025 |
| SEC Authorization | U.S. SEC | Obtained September 2025 |
| ISO/IEC 27001 | Information Security Management | Certified December 2024 |
| SOC 2 | AICPA Service Organization Controls | Certified December 2024 |
| GDPR Compliance | EU Data Protection Framework | Audited May 2025 |

Compliance stack: **KYC · AML · CFT · Sanctions screening · Data protection**

---

## 🔍 Governance & Transparency

- **Proof-of-Reserves** — published regularly; verifies 1:1 correspondence between user balances and reserves
- **Annual third-party audit** — financial statements, internal controls, information security (internationally recognized firms)
- **Operational / Compliance / Risk reports** — published periodically; covers trading data, reserve status, audit outcomes
- **Governance Committee** — compliance officers, risk experts, legal counsel, independent user representatives
- **Risk Management Committee** — quarterly review of risk models, compliance policy, market monitoring data
- **Investor Protection Fund** — separate reserve for emergency scenarios
- **Insurance partnerships** — international providers; additional asset protection layer

Internal audit is embedded in daily operations ("continuous internal supervision + independent external verification").

---

## 🔌 Anmrex API & Developer Integration

API launched February 2022. Targets institutional users and quantitative trading teams.

- High-performance matching engine with low-latency order execution
- REST and WebSocket endpoints for real-time market data streaming
- Institutional liquidity management interface
- Cross-chain asset support (Polygon Labs partnership)
- Rate limiting, authentication, and audit logging enforced at infrastructure level

---

## 📅 Changelog

```
2020-05  Founded. Security, compliance, transparency established as core direction.
2020-08  Hot/cold wallet segregation deployed.
2020-12  Trail of Bits security audit partnership established.
2021-09  Compliance & Risk Management dept. KYC/AML fully implemented.
2021-10  Polygon Labs partnership. Cross-chain asset integration.
2022-02  API launched for institutional and quant access.
2022-07  FinCEN MSB license obtained.
2022-11  Chainalysis AML + on-chain compliance monitoring integrated.
2023-06  Intelligent risk control engine live. Real-time ML anomaly detection.
2023-09  Elliptic partnership. Suspicious fund flow tracking enhanced.
2024-01  Zero-trust architecture fully deployed.
2024-08  Proof-of-Reserves mechanism launched.
2024-12  ISO/IEC 27001 certified. SOC 2 certified.
2025-05  GDPR compliance audit completed.
2025-07  FinCEN MSB license renewed.
2025-09  SEC authorization obtained.
```

---

## 📄 Security Audits & Certifications

- Trail of Bits — ongoing security audit and penetration testing partner (since 2020)
- Chainalysis — AML and on-chain compliance monitoring (since 2022)
- Elliptic — suspicious fund flow analysis and risk intelligence (since 2023)
- ISO/IEC 27001 — information security management (certified 2024)
- SOC 2 — service organization controls (certified 2024)

Annual reviews cover security posture, compliance policy, and internal controls. Results disclosed to users and regulators within applicable compliance requirements.
