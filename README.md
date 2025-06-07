# ⚽ Fantasy Premier League Assistant Tool

A Python-based tactical assistant for Fantasy Premier League (FPL) players. Built to help managers make smarter, more strategic decisions through curated stats, team analysis, and planning tools — all without relying heavily on machine learning.

---

## 🎯 Project Objectives

- 🧠 Improve decision-making through custom insights.
- 📊 Provide advanced statistics like player vs. opponent scoring likelihood.
- 🏟 Analyze team form and fixture strength more meaningfully.
- 🧰 Offer tools for strategy-building, draft creation, and performance comparison.
- 🤖 Deliver a recommendation system — logic-based, with optional ML enhancements.

---

## 🛠 Tech Stack

| Layer             | Tech Used                           |
|------------------|-------------------------------------|
| Language          | Python 3.10+                        |
| Core Logic        | Standard Python, `pydantic`, `math`|
| Data Fetching     | `requests`, `aiohttp`               |
| Planning Engine   | Custom algorithms, no ML by default|
| Caching/Storage   | `redis` via Docker                  |
| Interface         | CLI via `typer` or `argparse`       |
| Data Analysis     | `pandas` (optional)                 |
| Future-Ready ML   | `scikit-learn`, `xgboost` (optional)|

---

## 📁 Folder Structure

```
fpl_tool/
├── data/               # Cached & raw data (fixtures, players, teams)
├── engine/             # Core processing logic
│   ├── suggestor.py    # Transfer suggestions
│   ├── analyzer.py     # Team + player evaluation
│   └── planner.py      # Strategy/draft builder
├── fetcher/            # Data retrieval from APIs
│   ├── fpl_api.py
│   └── redis_cache.py
├── models/             # Pydantic models for validation
├── strategies/         # Draft building and chip logic
├── utils/              # Fixture difficulty, config, logger
├── main.py             # CLI entry point
└── tests/              # Unit tests
```

---

## ⚙️ Installation

> Clone the repository and set up dependencies

```bash
git clone https://github.com/your-username/fpl-tool.git
cd fpl-tool
pip install -r requirements.txt
```

> Optional: Run Redis via Docker

```bash
docker run -d -p 6379:6379 --name fpl-redis redis
```

---

## 🚀 Usage

```bash
python main.py suggest --team data/my_team.json
python main.py draft --budget 100.0 --formation 3-4-3
python main.py compare --teams data/team_a.json data/team_b.json
```

---

## ✅ Features

- **Player vs. Team Likelihoods**  
  Understand how likely a player is to perform vs a specific opponent.

- **Form & Fixture Evaluation**  
  Quantify team momentum and schedule difficulty.

- **Draft Strategy Tools**  
  Create optimal lineups based on budget and formation rules.

- **Performance Comparison Engine**  
  Compare team variants over projected gameweeks.

- **Custom Recommendations**  
  Logic-driven suggestions to optimize points and value.

---

## 🔭 Roadmap

- [ ] Frontend dashboard (Streamlit / FastAPI)
- [ ] Gameweek simulator
- [ ] Telegram or Discord bot integration
- [ ] Machine-learning boost for recommendations (optional)
- [ ] Player watchlist system

---

## 🧪 Tests

Run unit tests with:

```bash
pytest
```
