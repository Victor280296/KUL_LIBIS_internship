# Access to social media data for research

**Which data access method best fits a given research question on social media?**
This repository contains two web tools that help researchers answer that question, developed alongside a master's thesis. They take into account technical, legal, ethical and scientific constraints, with a focus on the EU Digital Services Act (DSA).

▶ **[Open the decision matrix](https://victor280296.github.io/KUL_LIBIS_internship/decision_matrix.html)** · **[Open the DSA Article 40 framework](https://victor280296.github.io/KUL_LIBIS_internship/DSA_Procedure.html)**

> [!NOTE]
> This work was carried out during an internship at **LIBIS (KU Leuven)** and is the basis of the master's thesis *Access to social media data for research: legal, ethical and technical guidelines* (supervisor: Roxanne Wyns), Master of Science in Digital Humanities, KU Leuven, 2025–2026.

---

## Contents

| File | What it is |
|---|---|
| [`decision_matrix.html`](decision_matrix.html) | Interactive decision matrix (web application) |
| [`decision_matrix.css`](decision_matrix.css) | Stylesheet of the decision matrix |
| [`Decision matrix.xlsx`](Decision%20matrix.xlsx) | Source spreadsheet: structure (*Schema*), scoring grid (*Scores*) and definitions (*Description*) |
| [`DSA_Procedure.html`](DSA_Procedure.html) | Interactive overview of a data access request under DSA Article 40 |

## The thesis

Platforms keep restricting access to their data, and the rules on access keep changing, so researchers now face many technical, legal and ethical constraints at once. The thesis first defines social media data and the DSA's notion of *systemic risks*. It then examines three families of access methods:

1. **Platform APIs**: closed data access for vetted researchers under DSA Article 40, and public research APIs.
2. **Scraping**: crawling, sock puppet accounts, scraping and AI-driven scraping.
3. **Third-party access**: data donation, tracking and existing data repositories.

Each method is evaluated on four dimensions: **technical feasibility, legal grounding, ethical implications and scientific limitations**. The results are brought together in the decision matrix and in a set of practical guidelines. These cover how to frame the research question, how to collect the data and how to evaluate it, including four types of bias: observer, moderation, platform overrepresentation and sociological.

### Main findings

- **APIs** have the strongest legal basis but give the weakest results in practice. Platforms decide what data to release, the administrative burden is heavy, and the most relevant content is underrepresented.
- **The DSA Article 40 procedure is slow.** It can take up to 175 working days. It is also **retrospective**: requesting data on systemic risks assumes those risks are already known. It therefore suits the study of past failures better than that of unfolding events, such as elections.
- **Scraping** gives more independence and more context, but it raises legal and ethical issues.
- **Third-party methods** give access to data that is otherwise out of reach. In return, they involve recruiting participants and come with uncertain quality or unclear provenance.
- With every method, researchers depend on someone else: the platforms' cooperation, users' willingness or the integrity of earlier data collections. The data that is available also shapes which questions can be studied.

## The tools

### Research Access Decision Matrix

The decision matrix is a selector that shows which of **ten access methods** are possible for a given research context, and ranks them.

**1. Describe the project.** Select at least one option in each of the four required categories:

| Category | Options |
|---|---|
| Social media | VLOP (Facebook, Instagram, LinkedIn, Pinterest, Snapchat, TikTok, X, YouTube) · Non-VLOP (Bluesky, Reddit, Telegram, other) |
| Data type | Content · User · Engagement · Moderation · Temporal · Network · Algorithmic · Geospatial |
| Privacy | Public · Private |
| Content type | Systemic risks · General content · Advertisements |

**2. Set priorities (optional).** Seven filters reflect what matters to the researcher: *Ethical, Legal, Contextual, Cost, Technically easy, Administratively easy, Short timeframes*.

**3. Read the results.** Each method gets a status and a score:

| Status | Meaning |
|---|---|
| ✓ **Open** | Every selected criterion is compatible with the method |
| ~ **Uncertain** | No criterion blocks the method, but compatibility is not established for at least one (`?`) |
| ✗ **Closed** | At least one selected criterion is incompatible with the method |

The **score** is used to rank the methods. It adds up the values of the selected filters, on a scale from −1 (*No*) to +1 (*Yes*), plus two **hidden filters** that always apply:
- **Data quality** penalises data that is not representative or is biased;
- **Cross-platform access** applies only when two or more platforms are selected.

The required categories decide whether a path is open, uncertain or closed. They do not count in the score.

**Methods evaluated:** Closed data API · Public data API · Commercial API · Ads library · Statements of reason · Logged-in scraping · Logged-out scraping · Tracking · Data donation · Third-party repository.

> [!IMPORTANT]
> The scores come from the analysis in the thesis and have no independent mathematical meaning. Their purpose is to show quickly the relative strengths and weaknesses of each method, not to give a definitive ranking. The matrix is calibrated for small-scale research on **algorithmic recommendation**. For large-scale **discourse analysis**, treat its rankings as indicative and give API access more weight.

### DSA Article 40 — Data access framework for vetted researchers

This reference page sets out what a request for non-public data under DSA Article 40 involves. It is organised as eight expandable cards, each linked to its legal basis:

| # | Card | Legal basis |
|---|---|---|
| 1 | Description of data requested | Delegated Act on data access (DADSA), Art. 8(c) |
| 2 | Data security | DADSA, Art. 9(4) |
| 3 | Researcher conditions | DSA, Art. 40(8)(a)–(g) |
| 4 | GDPR legal framework | GDPR, Art. 5(1)(f), 9(2), 32, 35(7), 89 |
| 5 | Research purposes | DSA, Art. 40(4) |
| 6 | Systemic risks | DSA, Art. 34(1) |
| 7 | Risk mitigation | DSA, Art. 35 |
| 8 | Fundamental rights | Charter of Fundamental Rights of the EU, Art. 1, 7, 8, 11, 21, 24, 38 |

## Running and adapting the tools

Both pages are static HTML, CSS and JavaScript files and need no external library or build step. To use them offline, clone the repository and open the HTML files in a browser:

```bash
git clone https://github.com/Victor280296/KUL_LIBIS_internship.git
```

To adapt the matrix to another research context, edit the values in `ACCESS_MATRIX` in `decision_matrix.html`. They mirror the *Scores* sheet of `Decision matrix.xlsx`. The comments at the top of the file explain the scoring rules. Contributions that update the scores as the field evolves are welcome.

## Use of generative AI

The code of both web pages was written with the help of Claude (Anthropic). The content of the tools comes from the analysis in the thesis: the criteria, the scores, the definitions and the legal references.

## Citation

> Close, V. (2026). *Access to social media data for research: Legal, ethical and technical guidelines* [Master's thesis, KU Leuven].

## Author

Victor Close · [GitHub](https://github.com/Victor280296)
