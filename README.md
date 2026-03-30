# The Ripple Effects of the 2008 Financial Crisis on the U.S. Economy

This project explores how the 2008 financial crisis affected the U.S. economy through a small set of public macroeconomic and banking datasets. The analysis focuses on bank failures, unemployment, household debt burden, and residential loan charge-off rates, combining short written interpretation with Quarto-based visualizations.

## What this project does

- **Bank failures**: Counts failed banks by year using the FDIC failed-bank list and plots the trend.
- **Unemployment**: Plots the U.S. unemployment rate over time (monthly series).
- **Household debt**: Uses household debt service ratios and related series to show stress around the crisis.
- **Bank charge-offs** (where included in the report): Shows credit losses at banks over time.

## Key question

How did the 2008 financial crisis spread from the banking system into employment conditions and household financial stress?

The goal is not to introduce a new statistical method, but to present a clear and readable story about how several economic indicators moved before, during, and after the crisis.

## Project outputs

- `HW7.html`: full HTML report
- `HW7_ppt.html`: slide presentation built with Reveal.js
- `HW7.qmd`: source file for the main report
- `HW7_ppt.qmd`: source file for the slide deck

## Repository layout

| Item | Role |
|------|------|
| `HW7.qmd` | Main Quarto document (long **HTML** report). |
| `HW7_ppt.qmd` | Quarto **slides** (Reveal.js HTML presentation). |
| `*.csv` | Input data (kept next to the `.qmd` files so paths stay simple). |
| `HW7.html`, `HW7_files/` | Rendered report (optional to commit; you can rebuild from `HW7.qmd`). |
| `HW7_ppt.html`, `HW7_ppt_files/` | Rendered slides (optional to commit). |
| `HW7.Rproj` | RStudio project file. |

## Workflow

1. **Input data**  
   CSV files are stored in the project root, and the Quarto documents read them with simple relative paths.

2. **Analysis**  
   The `.qmd` files combine Markdown narrative with R code using packages such as `readr`, `dplyr`, `ggplot2`, `tidyr`, `knitr`, and `patchwork`.

3. **Rendering**  
   Quarto executes the R code and produces:
   - `HW7.qmd` → **HTML report**
   - `HW7_ppt.qmd` → **Reveal.js slide deck** (still HTML, not a `.pptx` file)

4. **Viewing**  
   Open the generated `.html` files in a browser, or render them directly from RStudio or VS Code with Quarto support.

You can revise the narrative, adjust the plots, or replace the input data and then render the project again without editing the HTML manually.

## How to run it on your machine

### Requirements

- [R](https://www.r-project.org/) (recent version)
- [Quarto](https://quarto.org/docs/get-started/)
- R packages used in the documents, for example: `readr`, `dplyr`, `ggplot2`, `tidyr`, `knitr`, `patchwork` (install any missing package with `install.packages("...")`)

### Commands

From this folder in a terminal:

```bash
quarto render HW7.qmd
quarto render HW7_ppt.qmd
```

Or use the **Render** button in RStudio after opening the `.qmd` file.

## Data sources

The CSVs in this repository are analysis inputs collected from public sources, including FDIC, FRED, and Federal Reserve releases. File names are kept stable so the Quarto documents can run with relative paths.

## License

This project is open source under the **MIT License**. See the [`LICENSE`](LICENSE) file for details.
