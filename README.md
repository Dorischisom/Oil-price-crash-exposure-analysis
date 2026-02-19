# 🌍 Oil Price Crash Exposure by Country (2010–2023)

## 📌 Business Problem
Oil price crashes can severely impact countries that depend heavily on oil exports and petroleum revenues. 

When global oil prices decline sharply (e.g., 2014–2016 crash, 2020 COVID shock), oil-dependent economies often experience:
- Revenue shortfalls
- Fiscal pressure
- Currency depreciation
- Economic contraction

This project answers the key question:

**Which countries are most exposed to oil price crashes between 2010 and 2023?**


## 🎯 Objective

To identify and rank countries based on structural exposure to oil price volatility using economic dependence indicators.

The analysis focuses on:
- Oil rents as % of GDP
- Fuel exports as % of merchandise exports
- Exposure score trends over time
- Sensitivity during major oil price crash periods


# 📂 Data Sources

Data was obtained via the World Bank API, including:

1. Oil rents (% of GDP)
`Indicator: NY.GDP.PETR.RT.ZS`

2. Fuel exports (% of merchandise exports)
`Indicator: TX.VAL.FUEL.ZS.UN`

3. Historical Brent oil price data (for contextual crash analysis)

**Time period analyzed:**
2010–2023

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- World Bank API

##🧹 Data Cleaning & Preparation (Python)

##### Steps performed:

- Pulled data using World Bank API (JSON format)
- Converted JSON to Pandas DataFrame
- Removed regional aggregates:
  - World
  - Income groups
  - Regional codes (e.g., AFE, EUU)
- Filtered years: 2010–2023
- Removed missing values
- Merged oil rent and fuel export datasets (inner join)


## 📊 Exposure Score Construction
To measure vulnerability, an Exposure Score was constructed by combining:
- Oil rents (% of GDP)
- Fuel exports (% of merchandise exports)

The exposure score was normalized to range between 0 and 1.

Conceptually:

```Exposure Score = f(Oil Rent Dependency + Export Dependency)```

Higher scores indicate greater vulnerability to oil price crashes.


## 📈 Analysis & Visualizations

#### 1️⃣ Top 10 Most Exposed Countries (Average 2010–2023)

This visualization ranks countries by average exposure score.

### Key Findings
- Angola and Congo (Rep.) consistently rank among the most exposed.
- Saudi Arabia and Oman show structurally high dependence.
- Exposure in these economies is persistent, not temporary.
- Oil dependence appears embedded in fiscal and export structures.


## 2️⃣ Exposure Score Trend Over Time

Time-series analysis shows how vulnerability evolved between 2010 and 2023.

#### Observations
- Some countries show declining exposure (e.g., diversification efforts).
- Others show volatility linked to production changes.
- High-exposure countries remain sensitive across multiple price cycles.

## 3️⃣ Exposure During Major Oil Price Shocks

Two major oil price crash periods examined:
- 2014–2016 Oil Price Collapse
- 2020 COVID-19 Oil Shock

#### Insights
- Countries with higher structural exposure experienced larger fiscal stress during crash periods.
- Economies with lower exposure scores demonstrated better resilience.
- Diversification efforts correlate with reduced volatility impact.

## Overall Findings

Oil exposure remains structurally embedded in several exporting economies.

Export dependency amplifies vulnerability beyond domestic production reliance.

Exposure varies significantly across oil-producing countries.

Diversification reduces long-term vulnerability.

Oil price crashes disproportionately impact fiscally dependent economies.


## Limitations
1. Exposure score is based on two indicators and does not capture:
- Sovereign wealth fund buffers
- Debt levels
- Exchange rate regimes
- Fiscal policy responses

2. Oil rents as % of GDP may fluctuate due to:
- Price effects
- Production changes

3. Data availability varies across countries and years.
   
4. 2023 data may be provisional.
   
5. The analysis does not model macroeconomic outcomes (e.g., GDP contraction), only structural exposure.


## Conclusion
Between 2010 and 2023, oil price crash exposure remains highly concentrated in a group of structurally oil-dependent economies.
Countries such as Angola, Congo (Rep.), Saudi Arabia, and Oman display sustained vulnerability due to high fiscal and export reliance on oil.
While some economies show modest diversification trends, structural dependence remains a defining characteristic of several exporters.

Understanding exposure levels is critical for:
- Risk assessment
- Fiscal planning
- Sovereign credit analysis
- Energy transition strategy

As global energy markets evolve and transition dynamics accelerate, oil-dependent economies face increasing structural risk unless diversification efforts intensify.

