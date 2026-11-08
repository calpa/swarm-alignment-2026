<div align="center">

<img src="project-image.png" alt="Refusal and Invitation Acceptance in a Four-Agent Liar's Bar Sandbox" width="640">

# Refusal and Invitation Acceptance in a Four-Agent Liar's Bar Sandbox

**An Exploratory Audit**

*Team EIRAKU · Swarm Alignment Hackathon 2026 · Track 4: Multi-Agent Oversight and Control*

![Status](https://img.shields.io/badge/status-final_v2.5-2ea44f) ![Track](https://img.shields.io/badge/Apart_2026-Track_4-blue) ![License](https://img.shields.io/badge/license-MIT-green)

</div>

## Abstract

Behavioral baselines for detecting coordination among LLM agents remain scarce: after the 2026 METR covert-communication investigation, oversight teams still lack measurement tools exercised against attempted collusion in a controlled setting. We present a refusal-conditioned, opportunity-normalized challenge-rate measure and an exploratory, refusal-aware audit protocol for a four-agent Liar's Bar sandbox, together with a complete replication package. Across 40 episodes in two batches, all 40 secret-channel invitations were refused; per-episode challenge rates ranged 0.071–0.183 (batch pooled 0.121 / 0.115). A positive control (Gemma-4-26B, single-model configuration) accepted the invitation and established secret channels with hand-disclosure and coordinated-play language in four terminal-state episodes, demonstrating that refusal in the main configuration is model-dependent rather than a harness artifact. All episodes are exploratory (deviation-ledger governed); no detector is evaluated or validated.

## Contents

| File | Description |
|---|---|
| `swarm_report_en.pdf` | Final report — 7 pages (4-page body + references/appendices), v2.5 |
| `swarm_report_en.typ` | Typst source (single source of truth) |
| `fig_pairs.svg` | Figure 1 — per-ordered-pair challenge rates with Clopper–Pearson intervals |
| `project-image.png` | Project cover (Midori) |
| `sha256.txt` | Checksums |

## Reproduce

```bash
# Rebuild the PDF
typst compile swarm_report_en.typ

# Analysis commands (per-batch, never pooled — see Appendix B)
python3 analyze_g3.py runs/m1_d*/record.json
python3 analyze_g3.py runs/rep*/record.json
```

Per-episode manifests, record SHA-256 hashes, and the deviation ledger (D1–D15) are documented in the report appendix; full experiment records are available to organizers on request.

## Notes

- Preregistration was approved after data collection began; all episodes are classified as exploratory.
- This repository is private during review and will be made public after the sprint ends.

## License

[MIT](LICENSE) — © 2026 Calpa Liu (Team EIRAKU)
