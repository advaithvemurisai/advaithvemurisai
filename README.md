# Hi, I'm Advaith

**Data scientist building forecasting, optimisation and LLM systems that planners actually use.**

I have 3+ years across data science and analytics, with a background in demand planning, retail experimentation and data governance. I care about interpretable models, honest evaluation, and getting results into the hands of analysts and planners.

- Currently a **Data Scientist at Worldlink US**, working on AI-driven supply chain planning and trade compliance.
- **MS in Business Analytics and AI**, UT Dallas.
- [LinkedIn](https://www.linkedin.com/in/advaith-vs)

## Featured projects

Every project below is live, and each answers one business question.

### [Demand Planning Platform](https://github.com/advaithvemurisai/demand-forecast-platform) · [live app](https://demand-forecast-platform.vercel.app)
**How much should each Walmart store stock, and who gets it when supply is short?** It forecasts daily demand for 3,049 products × 4 stores (M5 data) and reconciles the plan so every level adds up. It then sets safety stock from calibrated ranges, allocates scarce stock with a linear program, and stress-tests policies in an inventory simulator of one warehouse and four stores that runs in the browser.
- Calibrated safety stock lifts fill rate from 87% to 97% and cuts lost sales by $188k over four weeks.
- Smarter allocation is worth about $91k a year.
- When a review caught an unfair baseline, I corrected my own headline: forecast-based reordering adds only 0.2 pts of fill rate at equal stock.

`Python · LightGBM · MinT reconciliation · conformal prediction · PuLP · React · Pyodide · FastAPI`

### [WikiWatch](https://github.com/advaithvemurisai/wikiwatch) · [live dashboard](https://wikiwatch-kappa.vercel.app)
**Did someone just make a risky edit to our brand's Wikipedia page?** A streaming lakehouse that reads every Wikimedia edit (about 42 a second), checks it against a watchlist of 60 brand, product and competitor pages, and raises alerts for removals, page moves, protection changes, unregistered editors and edit bursts. A three-page dashboard covers alerts, a platform baseline and pipeline health.
- No lost or duplicated edits across restarts: a live producer kill and resume missed 0 events, and Silver removes the repeats with an insert-only MERGE.
- Per-edit alerts reached Gold in about 61 seconds at p95 in a scripted scenario, against a 5-minute target.
- Every pull request replays about 5,000 recorded events through the real pipeline and checks the exact alerts; an independent SQL reconciliation and `EXPLAIN`-verified partition pruning back it up.
- Runs on AWS in short sessions created and destroyed by GitHub Actions, with no stored keys (OIDC), a $50 budget stop and a nightly destroy.

`Redpanda (Kafka) · Spark Structured Streaming · Apache Iceberg · dbt · Athena · Airflow · Terraform · Next.js · GitHub Actions`

### [Pursue](https://github.com/advaithvemurisai/gtm-sales-agent) · [live demo](https://gtm-sales-agent.vercel.app)
**Should your sales team go after this account?** Enter what you sell and a target company. It researches the company across the public web (company facts, technology, hiring and news), then returns a Pursue / Watch / Deprioritize verdict with cited evidence and a next step, in under a minute.
- A 15-case eval: 73% agreement with expected verdicts, 87% stable across reruns, 100% of claims cited, p50 latency 24s at about $0.22 a run.
- Confidence is capped in code by how much evidence is missing.

`React · FastAPI · Anthropic API · structured outputs`

### [RetailLab](https://github.com/advaithvemurisai/retail-ab-lab) · [live app](https://retail-ab-lab.vercel.app)
**Should a retailer keep sending its marketing e-mail?** It prices a randomized experiment on 64,000 customers (the Hillstrom e-mail test) at real sector margins and the cost of each send, then returns Ship, Don't Ship, Keep Testing or Don't Trust. Margin, cost and the return hurdle are adjustable, and the verdict updates live.
- Ship: revenue per customer rose 91% against the 48% needed to break even, for $6.8k contribution with a 1% chance of loss. The men's e-mail beats the women's head to head.
- 52% of the revenue credited to the e-mail would have come in anyway, so click-through attribution overstates its return about 2×.
- Before any verdict it checks for a broken split, peeking and segment-slicing, each measured on the data: 10 interim looks at a test with no effect declare a winner 20% of the time.
- The decision rules exist once, in Python: a FastAPI function on Vercel prices precomputed statistics per request, tested to match the full analysis.

`Python · SciPy · statsmodels · DuckDB · SQL · FastAPI · React · Vercel`

### [CinematicLink](https://github.com/advaithvemurisai/filmi-link) · [play it](https://cinematic-link.vercel.app)
**A passion project:** Wordle for Indian cinema, inspired by [FilmLink](https://www.filmlink.io/). Each day you link two films through the actors, directors and composers who made them.
- It runs on a graph of about 18,900 films and 17,000 people across 11 languages.
- A generator scores candidate pairs on familiarity, route count and star dependence using sparse-matrix graph maths, with daily puzzles for five home industries.
- Accounts run on a serverless function and Redis, and a weekly GitHub Action refreshes the data without changing published puzzles.

`React · TypeScript · NumPy/SciPy · Vercel · Upstash Redis · GitHub Actions`

### [LiftLab](https://github.com/advaithvemurisai/ab-test-simulator) · [live app](https://ab-test-simulator-gbefknskbhqc9fgythgzks.streamlit.app/)
**Should a neobank ship instant bank linking?** An A/B testing decision workspace that weighs the lift against revenue and fraud guardrails. It checks test validity (power, sample-ratio mismatch, novelty effects) before recommending Ship, Don't Ship, Keep Testing or Don't Trust.

`Python · Streamlit · Bayesian and frequentist testing`

### More
- [Rideshare Pricing Analysis](https://github.com/advaithvemurisai/Analysis-of-Dynamic-Pricing-Methods-employed-by-Rideshare-Companies): a group course project comparing dynamic pricing across Uber and Lyft and its effect on demand. `Python · Jupyter`

## What I work with

| | |
|---|---|
| **ML & statistics** | scikit-learn, Spark MLlib, LightGBM, time series (ARIMA, Prophet), forecast reconciliation, conformal prediction, SHAP, experimentation and incrementality testing, segmentation |
| **Optimisation & simulation** | linear programming (PuLP, HiGHS), inventory policy and safety stock, Monte Carlo simulation |
| **GenAI & NLP** | LLMs, AI agents, RAG, LangGraph, prompt engineering, embeddings, vector search (pgvector), Neo4j, Amazon Bedrock, Anthropic API |
| **Programming & data** | Python (pandas, NumPy, PySpark), SQL (PostgreSQL, SQL Server, Snowflake), SparkSQL, DAX, TypeScript/React |
| **Cloud & engineering** | AWS (S3, Athena, Glue, EC2), Azure, Databricks, Delta Lake, Snowflake, FastAPI, REST APIs, dimensional modeling, Vercel, GitHub Actions |
| **Data engineering** | Kafka/Redpanda, Spark Structured Streaming, Apache Iceberg, dbt, Airflow, Terraform, Docker |
| **BI & reporting** | Power BI, Tableau, Excel, Alteryx, SSRS |
| **Certifications** | Databricks Certified Data Engineer Associate · AWS Certified Cloud Practitioner · Microsoft Azure Data Fundamentals |
