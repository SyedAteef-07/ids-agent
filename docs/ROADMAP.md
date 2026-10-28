# Project Roadmap

Deadline: second week of November 2026. Target finish: Sun 8 Nov.

## Goal
Build an agent that detects network attacks and responds automatically.
It acts only when confident, every action is reversible, and legitimate
traffic is not wrongly blocked.

## Research question
Can a confidence-gated, reversible response layer stop most attacks while
almost never blocking legitimate traffic, across different detectors and datasets?

## Team roles
| Member | Role | Deliverables |
|---|---|---|
| 1 | Data | Clean datasets, data report, replay streams |
| 2 | Models | Trained detectors, calibration, cross-dataset results |
| 3 | Agent | Action table, safety gate, simulator, experiment runner |
| 4 | Dashboard and paper | Streamlit dashboard, figures, report, repo upkeep |

## Scope (to fit the deadline)
- Main dataset: UNSW-NB15. Second dataset: one or two CICIDS2018 day files.
- Detectors: Random Forest, XGBoost, small DNN.
- 3 random seeds. Replay dataset rows as a stream; no live capture.
- If behind, cut in this order: pre-trained baseline, CICIDS2018 test, DNN, ablations.

## Schedule
| Date | Goal | Key tasks |
|---|---|---|
| Wed 28 Oct | Setup | Repo, shared Drive, download UNSW-NB15, action table and simulator with dummy data |
| Thu 29 Oct | First baseline | Clean data, Random Forest, safety gate, dashboard skeleton |
| Fri 30 Oct | More models | XGBoost, DNN, block expiry, review queue, result plots |
| Sat 31 Oct | Cross-dataset | Clean CICIDS2018, cross-dataset test, related-work draft |
| Sun 1 Nov | Checkpoint 1 | Calibration, agent runs end to end on UNSW-NB15 |
| Mon 2 Nov | Experiments | Run 4 setups: no response, always act, fixed gate, calibrated gate |
| Tue 3 Nov | Experiments | Threshold sweep, figures |
| Wed 4 Nov | Ablations | Ablation runs, methods and results text |
| Thu 5 Nov | Writing | Merge paper draft |
| Fri 6 Nov | Checkpoint 2 | Full report draft, code cleanup |
| Sat 7 Nov | Reproduce | Run everything from a fresh Colab, finish README |
| Sun 8 Nov | Rehearse | Demo practice, slides |
| 9 to 11 Nov | Buffer | Fixes and submission |

## Metrics
- Attack mitigation rate
- Collateral block rate (legitimate flows wrongly blocked)
- Human alert load
- Time to mitigate

## Team rules
- One branch per member; no pushing directly to main.
- Commit code and small results only. Never commit datasets, model files,
  kaggle.json or tokens.
- Keep real logic in src/; notebooks stay thin.
  
