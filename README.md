# 18 November 2026 — The World in One Image

A deterministic program that draws a 1024×1024 PNG infographic summarising
six major world-news stories from Wednesday 18 November 2026. Built for the
make.fun bounty **"Sum up 18 November's world news in one image"** (USDC 250).

## The six stories

1. **Diplomacy** — Xi and Putin meet in Shenzhen, a day before the first-ever
   Trump–Xi–Putin trilateral summit.
2. **Middle East** — Iran strikes Kuwait and Bahrain after the US hit a
   missile site on Qeshm Island.
3. **Ukraine** — Kerch Bridge hit for a second day; Ukraine claims major damage.
4. **United States** — Peltola wins the Alaska Senate seat; Democrats projected
   to a 56–44 Senate majority.
5. **India** — Cyclone Akvan forces mass evacuations in Odisha (47,000+ people).
6. **Tech** — Nvidia board rejects Jensen Huang's return as CEO, despite a
   record $115.8B quarter.

Full sourcing is in [NOTES.md](NOTES.md). Headlines are worded within what
the cited reporting actually said (e.g. "claims" where damage was claimed
but not independently verified).

## How to run

```bash
pip install pillow        # only dependency
python3 main.py           # writes output.png in this directory
python3 main.py out.png   # or a custom output path
```

Requires Python 3.12+ (also runs on Python 3.13). Uses only the standard
library plus Pillow. No network access at runtime.

## Determinism

Every input is a literal in `main.py` — fixed text, colours and layout, no
randomness, no timestamps, no external data. Running the program twice
produces a byte-identical PNG (verified: identical SHA-256 hashes).

## Output

- `output.png` — 1024×1024 PNG, ~118 KB (limit: ≤1 MiB, ≤1024×1024).

## News sources

Reuters, AP, AFP, Al Jazeera, France 24, CNN — see NOTES.md for the
per-story source list and URLs.

## License

MIT — see [LICENSE](LICENSE).
