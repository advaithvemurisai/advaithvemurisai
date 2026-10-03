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

### [Pursue](https://github.com/advaithvemurisai/gtm-sales-agent) · [live demo](https://gtm-sales-agent.vercel.app)
**Should your sales team go after this account?** Enter what you sell and a target company. It researches the company across the public web (company facts, technology, hiring and news), then returns a Pursue / Watch / Deprioritize verdict with cited evidence and a next step, in under a minute.
- A 15-case eval: 73% agreement with expected verdicts, 87% stable across reruns, 100% of claims cited, p50 latency 24s at about $0.22 a run.
- Confidence is capped in code by how much evidence is missing.

`React · FastAPI · Anthropic API · structured outputs`

### [RetailLab](https://github.com/advaithvemurisai/retail-ab-lab) · [live app](https://retail-ab-lab-bnwnskexpoqbajnhzqgnkh.streamlit.app/)
**Should a retailer keep sending its marketing e-mail?** It prices a 64,000-customer randomized experiment at real sector margins and returns Ship, Don't Ship, Keep Testing or Don't Trust. Verdict: the e-mail pays, $6.8k contribution against a 48% break-even lift, with the men's e-mail driving most of it.

`Python · DuckDB · SQL · Streamlit · statistics`

### [LiftLab](https://github.com/advaithvemurisai/ab-test-simulator) · [live app](https://ab-test-simulator-gbefknskbhqc9fgythgzks.streamlit.app/)
**Should a neobank ship instant bank linking?** An A/B testing decision workspace that weighs the lift against revenue and fraud guardrails. It checks test validity (power, sample-ratio mismatch, novelty effects) before recommending Ship, Don't Ship, Keep Testing or Don't Trust.

`Python · Streamlit · Bayesian and frequentist testing`

### [CinematicLink](https://github.com/advaithvemurisai/filmi-link) · [play it](https://cinematic-link.vercel.app)
**A passion project:** Wordle for Indian cinema, inspired by [FilmLink](https://www.filmlink.io/). Each day you link two films through the actors, directors and composers who made them.
- It runs on a graph of about 18,900 films and 17,000 people across 11 languages.
- A generator scores candidate pairs on familiarity, route count and star dependence using sparse-matrix graph maths, with daily puzzles for five home industries.
- Accounts run on a serverless function and Redis, and a weekly GitHub Action refreshes the data without changing published puzzles.

`React · TypeScript · NumPy/SciPy · Vercel · Upstash Redis · GitHub Actions`

### More
- [Rideshare Pricing Analysis](https://github.com/advaithvemurisai/Analysis-of-Dynamic-Pricing-Methods-employed-by-Rideshare-Companies): a group course project comparing dynamic pricing across Uber and Lyft and its effect on demand. `Python · Jupyter`

## What I work with

| | |
|---|---|
| **ML & statistics** | scikit-learn, Spark MLlib, LightGBM, time series (ARIMA, Prophet), forecast reconciliation, conformal prediction, SHAP, experimentation and incrementality testing, segmentation |
| **Optimisation & simulation** | linear programming (PuLP, HiGHS), inventory policy and safety stock, Monte Carlo simulation |
| **GenAI & NLP** | LLMs, AI agents, RAG, LangGraph, prompt engineering, embeddings, vector search (pgvector), Neo4j, Amazon Bedrock, Anthropic API |
| **Programming & data** | Python (pandas, NumPy, PySpark), SQL (PostgreSQL, SQL Server, Snowflake), SparkSQL, DAX, TypeScript/React |
| **Cloud & engineering** | AWS, Azure, Databricks, Delta Lake, Snowflake, FastAPI, REST APIs, dimensional modeling, Vercel, GitHub Actions |
| **BI & reporting** | Power BI, Tableau, Excel, Alteryx, SSRS |
| **Certifications** | Databricks Certified Data Engineer Associate · AWS Certified Cloud Practitioner · Microsoft Azure Data Fundamentals |
