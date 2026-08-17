# abide-bunn

Code for the ABIDE-I BuNN operator comparison. Identity, GCN, trivial-bundle,
learned-local, and learned BuNN on functional connectomes, plus the baseline
and follow-up experiments.

This repo is just the code. Papers and the longer study notes are in
[bunn-abide](https://github.com/aditnotfound/bunn-abide).

## Setup

```powershell
python -m venv .venv
.\.venv\Scripts\python -m pip install -e ".[dev]"
```

On Linux or macOS: `source .venv/bin/activate`.

## Tests

```powershell
python -m pytest -q
```

These checks use synthetic or tiny fixtures. They do not download ABIDE or
repeat the full training runs.

## Layout

- `src/` — operators, models, training
- `scripts/` — data prep, runners, audits, analysis
- `configs/` — the settings those scripts expect
- `tests/` — unit tests for the above

Raw ABIDE files and run outputs stay local (`data/`, `outputs/`). They are not
in git.

## License

All rights reserved. See `LICENSE`.
