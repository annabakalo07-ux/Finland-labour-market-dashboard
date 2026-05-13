# 🇫🇮 Finland Labour Market Dashboard
### Suomen työmarkkinat — Työnhakijat & avoimet työpaikat

An interactive HTML dashboard visualising unemployment and job vacancy dynamics in Finland by occupation, region, and age group — based on official data from Tilastokeskus (Statistics Finland).

---

## 📊 About the Project

This dashboard was built as a **portfolio project** to demonstrate skills in:
- Data sourcing from official Finnish statistical databases
- Data analysis and interpretation
- Interactive data visualisation (no frameworks — pure HTML/CSS/JS + Chart.js)
- Bilingual presentation (English / Finnish)
- Analytical thinking: identifying trends, mismatches, and problem areas

**Author note:** This dashboard covers a **selected sample of occupations** from the Tilastokeskus dataset, not the full list of all professions available on the source website.

---

## 📁 Data Sources

| File | Source | Coverage |
|------|--------|----------|
| `Unemployed_jobseekers_and_vacantiens_by_occupation.xlsx` | [stat.fi — työnvälitystilasto](https://stat.fi/en/statistics/tyonv) | Unemployed jobseekers & vacancies by occupation, region (March 2021–2026) |
| `Jobseekers_by_occupation_and_level_of_education_in_each_province.xlsx` | [stat.fi — työnvälitystilasto](https://stat.fi/en/statistics/tyonv) | Jobseekers by occupation category, age group & education (March 2021–2026) |

- **Provider:** KEHA Centre, Employment Service Statistics
- **Last data update:** 22.04.2026
- **Reference month:** March each year (2021–2026)
- **Regions:** Whole Country / Uusimaa

> ⚠️ Cells marked `"..."` in the source data indicate values subject to statistical secrecy (too few observations). These are excluded from ratio calculations.

---

## 📌 Dashboard Features

| Feature | Description |
|---------|-------------|
| 🌐 **Bilingual toggle** | Switch between English and Finnish (EN/FI) |
| 📅 **Year filter** | Compare any March year from 2021 to 2026 |
| 📍 **Region filter** | Whole Country or Uusimaa |
| 📈 **Trend chart** | Unemployed vs vacancies over 6 years |
| 📊 **Ratio chart** | Seekers-per-vacancy by occupation (pressure index) |
| 📋 **Occupation table** | Only occupations with full data for the selected year (both unemployed & vacancies available) |
| 👥 **Age group chart** | Stacked bar: unemployed by age & occupation category (2026) |
| 💡 **Insight panel** | Key findings and problem areas highlighted |

---

## 🔍 Key Findings (from the data)

1. **Total unemployment increased** from 2021 lows after post-COVID recovery — Whole Country went from 331,526 (Mar 2021) to 342,759 (Mar 2026).
2. **Vacancies collapsed**: from 132,680 (peak 2022) to just 39,711 in March 2026 — a 70% drop in 4 years.
3. **IT sector mismatch**: Systems analysts (2511) grew from 989 to 1,530 unemployed nationally; vacancies fell from 136 to 49. Supply clearly exceeds demand.
4. **Managers under pressure**: Sales & marketing managers (1221) tripled in unemployment (582 → 1,469); R&D managers (1223) nearly 6x (67 → 396). Few vacancies available.
5. **Cleaners and trades**: Building structure cleaners (7133) maintain the most balanced ratio (~2.7:1) with active vacancies.
6. **Accountants & clerks**: Nearly no vacancies left (15 in 2026 vs. 167 in 2021) — possible automation pressure on routine accounting tasks.
7. **Age group 30–34 Professionals** form the largest unemployed segment in 2026 (8,242 nationally).

---

## 🛠️ Technical Stack

- **HTML5 / CSS3 / Vanilla JavaScript** — no build tools required
- **[Chart.js 4.4](https://www.chartjs.org/)** — loaded via CDN
- **[Google Fonts](https://fonts.google.com/)** — Syne + DM Sans
- Data embedded directly in the HTML file (no backend needed)

### How to run locally
Simply open `finland_unemployment_dashboard.html` in any modern web browser. No installation required.

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/finland-labour-dashboard.git
cd finland-labour-dashboard

# Open in browser
open finland_unemployment_dashboard.html   # macOS
start finland_unemployment_dashboard.html  # Windows
xdg-open finland_unemployment_dashboard.html  # Linux
```

---

## 📂 Repository Structure

```
finland-labour-dashboard/
├── finland_unemployment_dashboard.html   # Main dashboard (self-contained)
├── README.md                             # This file
└── data/
    ├── Unemployed_jobseekers_and_vacantiens_by_occupation.xlsx
    └── Jobseekers_by_occupation_and_level_of_education_in_each_province.xlsx
```

---

## ⚠️ Limitations & Caveats

- Data covers **March only** for each year — seasonal effects not visible
- **Selected occupations only** — not a complete picture of the Finnish labour market
- Vacancy data represents positions **posted to TE Offices** only; other channels not included
- Figures marked `"..."` in the source are suppressed for confidentiality. Occupations with suppressed data in the **selected year** are automatically excluded from the table and charts — switch to a different year to see if data becomes available
- Uusimaa breakdown is less complete due to more suppressed values at regional level

---

## 📜 License

Data is sourced from Tilastokeskus (Statistics Finland) and KEHA Centre under their open data terms.  
Dashboard code: MIT License.

---

*Portfolio project · Anna Bakalo · [LinkedIn](https://www.linkedin.com/in/anna-bakalo) · Data analysis · Finland labour market · 2026*
