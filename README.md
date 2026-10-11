# India Education, School Transition & Youth Risk Analytics

A portfolio-grade Data Analytics / Data Science project covering:

1. Government vs private school transition
2. Education dropout and expenditure
3. Child labour and education participation
4. Youth crime / juvenile justice
5. India vs selected international indicators

## Important data-integrity note

This repository deliberately does **not** invent a 10–15 year official dataset where no such continuous series exists.

- `data/processed/education_demo.csv` and `youth_crime_demo.csv` are synthetic demo data for testing the pipeline and dashboard prototype.
- `data/processed/child_labour_india_2011.csv` contains a cited official aggregate from Census 2011 as reported by the ILO.
- Official source links and methodology are in `docs/DATA_SOURCES.md`.
- Replace the demo files with downloaded official data before presenting quantitative findings as real results.

## Official backbone

UDISE+ is the Ministry of Education's school education information system. Its archive provides historical reports, and its recent reporting includes enrolment, dropout, transition, pupil-teacher ratio and infrastructure indicators.

The 2025 Comprehensive Modular Survey: Education from MoSPI provides household education expenditure estimates and is useful for the cost component, but it is not a 15-year annual fee series.

Child-labour historical data is anchored to Census 2011 / ILO. A continuous annual state-level child-labour series should not be fabricated.

Youth crime analysis should use NCRB releases and must distinguish juvenile-justice age definitions from broader youth age bands.

## Project structure

- `src/` reusable Python ETL and analysis code
- `sql/` database schema and analytical queries
- `powerbi/` dashboard blueprint, DAX measures and data model
- `docs/` data sources, methodology and limitations
- `reports/` report template
- `tests/` basic pipeline tests
- `data/` raw and processed data

## Run

```bash
pip install -r requirements.txt
python src/run_pipeline.py
pytest
```

## Suggested Power BI pages

1. Executive Overview
2. Government vs Private Transition
3. Education Cost
4. Dropout & Retention
5. Child Labour
6. Youth Crime
7. India vs World
8. Data Quality & Methodology

## Portfolio claim

Do not claim causal relationships from observational data. Use terms such as:
- associated with
- correlated with
- trend
- difference
- relationship

instead of "causes", unless a valid causal design is used.
