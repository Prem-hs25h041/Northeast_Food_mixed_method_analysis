# Migration and Food: Ethnic Food, Food Stores, and Consumption Among Northeast India's Migrant Communities in Metropolitan Cities

A mixed-methods study examining why Northeast Indian ethnic food remains central to migrants' lives in Delhi, Chennai, and Bangalore, and what role ethnic food stores and restaurants play in identity, community, and daily life.

## Research questions

1. Why is the consumption of ethnic food so crucial for Northeast migrants, despite the fact that its preparation and consumption can sometimes lead to conflict or hostility from neighbors?
2. What role do ethnic food stores and restaurants play in facilitating social interaction and community cohesion, both within the Northeast community and with the broader urban population?
3. What are the economic impacts of ethnic food restaurants on Northeast migrants and the local economy — employment, entrepreneurship, and income?
4. How do ethnic food stores contribute to Sustainable Development Goals, particularly cultural diversity, local economies, and food security/nutrition?

## Design

The study combines a structured survey with open-ended qualitative responses, collected from the same respondent pool.

| | Quantitative | Qualitative |
|---|---|---|
| **Data** | 237 responses × 44 variables | Open-ended responses from the same 237-person sample |
| **Method** | Univariate and bivariate analysis, frequency/percentage breakdowns, cross-tabulation by RQ | Open coding → codebook → categories → themes (thematic analysis) |
| **Tools** | Python, Pandas, NumPy, Matplotlib, Seaborn | Manual coding, consolidated into a codebook and pattern matrix |

Each research question is answered twice — once from the survey statistics, once from the coded themes — and the two are then checked against each other in [`08_Quan_Qual_Integration`](qualitative-analysis/) to see where they agree, and where they don't.

## Sample

- 237 respondents across Delhi (61.6%), Chennai (27.0%), and Bangalore (6.3%)
- 64.1% aged 18–25; 52.7% students
- 43.9% identify Manipur as their native state, with the remainder drawn from across the Northeast region

This skew means findings describe this specific sample well, but shouldn't be generalized to all Northeast migrants nationally — see Limitations.

## Key findings

**Ethnic food is a vehicle for cultural identity, not just sustenance.** 87.8% agree ethnic food keeps them connected to their culture, and 91.6% call it important during festivals and celebrations. This holds even where tension exists: among the 41.8% who perceive discrimination linked to ethnic food stores in their neighborhood, 91.9% still say the food connects them to their culture and 84.9% say it gives them pride in their heritage. The qualitative theme *"ethnic food as a source of cultural and emotional connection"* tracks this closely — respondents described things like getting food parcels from home and maintaining ethnic food practices despite the friction it can cause.

**Ethnic food stores function as community infrastructure.** 84.4% say these stores create a sense of belonging, and 73.8% say they contribute to social cohesion — rising to 81.1% among people who frequently attend food-centered gatherings. Word of mouth (64.6%) is by far the dominant way people discover stores, well ahead of social media (28.7%). The qualitative coding backs this up directly: themes around *"ethnic food spaces as sites of social interaction"* and *"community belonging"* recur across the open-ended responses.

**Access is a real constraint, but doesn't stop consumption.** 71.7% face at least occasional difficulty sourcing ingredients — mainly high prices (39.2%) and availability (36.7%) — yet people adapt: importing ingredients from home, cooking at home instead of eating out, or consuming ethnic food occasionally rather than regularly. This constraint-and-adaptation pattern is one of the clearer places where the qualitative theme (*"maintaining ethnic food practices despite consumption constraints"*) explains the mechanism behind a quantitative number.

**Economic and sustainability dimensions diverge.** Respondents perceive strong economic value — 83.1% say these stores contribute to the local economy, and 79.3% see them as supporting women entrepreneurs — but only 14.4% believe the stores follow environmentally sustainable practices, with over half unsure. This is the one place where the qualitative and quantitative pictures pull apart: a handful of coded responses describe sustainable habits (banana-leaf packaging, jute bags), but most respondents simply don't know either way.

Full RQ-by-RQ statistics and quotes are in the notebook and workbook linked below.

## Repository structure

```
northeast-food-data-analysis/
│
├── README.md
│
├── quantitative-analysis/
│   ├── notebooks/
│   │   └── Northeast_Food_analysis.ipynb
│   └── figures/
│
├── qualitative-analysis/
│   ├── codebook.xlsx              # 04_CodeBook — initial code → final code → category
│   ├── pattern_matrix.xlsx        # 05_Pattern_Matrix — category presence across questions/RQs
│   ├── themes.xlsx                # 06_Themes — category → theme, by RQ
│   ├── rq_findings.xlsx           # 07_RQ_Findings — themes with illustrative (non-identifying) response excerpts
│   └── quan_qual_integration.xlsx # 08_Quan_Qual_Integration — where survey stats and themes agree/diverge
│
└── documentation/
    └── methodology.md
```

Raw survey responses, the response-level coding sheet, and any respondent-identifying fields are intentionally not included in this repository — see **Note on participant privacy** below.

## Limitations

- The sample skews heavily toward Delhi, students, and the 18–25 age group, and toward Manipur as native state — findings shouldn't be read as representative of all Northeast migrants.
- The quantitative analysis uses frequencies, percentages, and cross-tabulations only; no significance testing (e.g. chi-square, regression) has been run yet, so relationships are described as associations, not causal effects.
- RQ1 asks about violence and conflict, but the survey variable measures *perceived discrimination/hatred*, not confirmed incidents — the conclusions are worded accordingly.
- RQ3 measures respondents' *perceptions* of economic contribution, not verified employment, business, or income figures.

## Note on participant privacy

The original dataset includes free-text responses and, at earlier stages of analysis, identifying information (names, exact demographic combinations). Before anything was published here:

- All raw responses, the row-level coding sheet, and any name/identifier fields were removed.
- What remains public is the *analytical trail* — the codebook, category structure, themes, and aggregated findings — plus a small number of short, non-identifying response excerpts used as illustrative evidence for each theme.
- The full response-level dataset is retained privately as the authoritative research record and is available on request where appropriate, subject to the original consent given by participants.

## Tools

Python · Pandas · NumPy · Matplotlib · Seaborn · manual qualitative coding (Excel)
