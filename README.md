# Jiyuan-Wong.github.io

## Jiyuan Wang's Personal Website

This repository contains the source files for my personal website created
as part of DSCI 521 in the UBC Master of Data Science program.

The website includes:

- A home page with a self-introduction
- An about page with more information about my background and interests
- A blog containing posts about my experience in the MDS program
- A computational blog post using Python and the Iris dataset
- A computational blog post using R and the Palmer Penguins dataset

The website is built using [Quarto](https://quarto.org/) and published
using GitHub Pages.

## Website

The live website is available at:

https://Jiyuan-Wong.github.io

## Requirements

To reproduce this website locally, the following software is required:

- Git
- Quarto
- uv
- Python 3.14
- R 4.6.1

The Python dependencies are managed using `uv`.

The R dependencies are managed using `renv`.

## Clone the Repository

Clone the repository and move into the project directory:

```bash
git clone https://github.com/Jiyuan-Wong/Jiyuan-Wong.github.io.git
cd Jiyuan-Wong.github.io
```

## Set Up the Python Environment

Install the Python dependencies using:

```bash
uv sync
```

This creates the local `.venv` environment using the dependencies recorded
in `pyproject.toml` and `uv.lock`.

## Set Up the R Environment

Start R from the root directory of the repository:

```bash
R
```

Then restore the R environment:

```r
renv::restore()
```

After the packages have been restored, exit R:

```r
q()
```

If prompted to save the workspace image, choose `n`.

## Render the Website

From the root directory of the repository, run:

```bash
uv run quarto render
```

The rendered website will be written to the `docs/` directory.

## Preview the Website Locally

To preview the website locally, run:

```bash
uv run quarto preview
```

## Reproducible Environments

### Python

The Python environment is defined by:

- `.python-version`
- `pyproject.toml`
- `uv.lock`

The local `.venv/` directory is not tracked by Git.

### R

The R environment is defined by:

- `.Rprofile`
- `renv.lock`
- `renv/activate.R`
- `renv/settings.json`

The local `renv/library/` directory is not tracked by Git.

## Data Sources

The Python computational post uses the Iris dataset provided through
scikit-learn:

https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html

The R computational post uses the Palmer Penguins dataset:

https://allisonhorst.github.io/palmerpenguins/

## Repository Structure

```text
Jiyuan-Wong.github.io/
├── docs/
├── images/
├── posts/
│   ├── first-week/
│   ├── iris-python/
│   └── penguins-r/
├── renv/
├── .gitignore
├── .python-version
├── .Rprofile
├── _quarto.yml
├── about.qmd
├── blog.qmd
├── index.qmd
├── pyproject.toml
├── README.md
├── renv.lock
├── styles.css
└── uv.lock
```