# AI Network Security Agent

Detects network attacks with machine learning and responds through a
confidence-gated, reversible action layer. Actions run on a simulated
firewall, not a real network.

## Datasets
- UNSW-NB15 (main)
- CICIDS2018 (cross-dataset test)

## Team
- Member 1: Data
- Member 2: Models
- Member 3: Agent (decision layer and simulator)
- Member 4: Dashboard and paper

## How it works
Sense (model predicts attack type and confidence) -> Decide (action table)
-> Safety gate (act only if confident, otherwise alert a human) -> Act and log.

## Folders
- docs/ : roadmap and notes
- notebooks/ : Colab notebooks
- src/ : all real code
- app/ : Streamlit dashboard
- results/ : small tables and figures only

## Plan
See docs/ROADMAP.md

## Data
Datasets are not stored here. They live in the shared Google Drive.
