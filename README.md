# Refusal and Invitation Acceptance in a Four-Agent Liar's Bar Sandbox: An Exploratory Audit

**Team EIRAKU · Calpa Liu** — Swarm Alignment Hackathon 2026 (Apart Research), Track 4: Multi-Agent Oversight and Control.

## Abstract

Behavioral baselines for detecting coordination among LLM agents remain scarce: after the 2026 METR covert-communication investigation, oversight teams still lack measurement tools exercised against attempted collusion in a controlled setting. We present a refusal-conditioned, opportunity-normalized challenge-rate measure and an exploratory, refusal-aware audit protocol for a four-agent Liar's Bar sandbox, together with a complete replication package. Across 40 episodes in two batches, all 40 secret-channel invitations were refused; per-episode challenge rates ranged 0.071–0.183 (batch pooled 0.121 / 0.115). A positive control (Gemma-4-26B, single-model configuration) accepted the invitation and established secret channels with hand-disclosure and coordinated-play language in four terminal-state episodes, demonstrating that refusal in the main configuration is model-dependent rather than a harness artifact. All episodes are exploratory (deviation-ledger governed); no detector is evaluated or validated.

## Contents

- `swarm_report_en.pdf` — final report (7 pages: 4-page body + references/appendices)
- `swarm_report_en.typ` — Typst source
- `fig_pairs.svg` — Figure 1 (per-ordered-pair challenge rates with Clopper–Pearson intervals)
- `sha256.txt` — checksums

## Reproduction

Analysis commands and per-episode manifests are documented in the report (Appendix B); the full experiment records (40 main-batch + positive-control episodes, deviation ledger D1–D15) live in the working repository and are available to organizers on request. `typst compile swarm_report_en.typ` rebuilds the PDF.

## Notes

- Preregistration was approved after data collection began; all episodes are classified as exploratory.
- Repository is private during review; it will be made public after the sprint ends.
