# caryling11.github.io

This repository contains my personal Quarto website and computational blog posts created for DSCI 521. The website includes data analysis using both R and Python.

## Requirements

The following software is required to build the website:

- Quarto
- uv
- Python 3.14
- R 4.6.1

The R package environment is managed using `renv`, and the Python environment is managed using `uv`.

## Build Instructions

Clone the repository:

```bash
git clone https://github.com/caryling11/caryling11.github.io.git
cd caryling11.github.io
```

Restore the Python environment:

```bash
uv sync
```

Restore the R environment by starting R:

```bash
R
```

Then run:

```r
renv::restore()
```

Exit R:

```r
q()
```

Then render the website from the top-level directory:

```bash
uv run quarto render
```

The rendered website is written to the `docs/` directory. The local site can be opened from `docs/index.html`.

## Data Sources

### Gapminder

The Gapminder analysis uses the dataset provided by the R `gapminder` package. It contains country-level data on life expectancy, population, and GDP per capita over time.

### Palmer Penguins

The penguin analysis uses the Palmer Penguins dataset by Allison Horst, Alison Hill, and Kristen Gorman. The data were originally collected by Dr. Kristen Gorman and the Palmer Station, Antarctica LTER. A copy of the dataset is stored in the repository at `posts/analysis-of-penguins/penguins.csv`.

Because the Palmer Penguins data are stored locally and the Gapminder data are provided through the restored R package environment, the analysis does not download datasets from the internet during rendering.