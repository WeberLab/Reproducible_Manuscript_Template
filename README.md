# Reproducible quarto manuscript for "Title"

This is a repo for generating our manuscript.

# Steps to reproduce:

## Clone this repo

`gh repo clone WeberLab/Reproducible_Manuscript_Template`

## rv package manager for r

You will find an `rproject.toml` file in the main directory and the `notebooks` directory. These define the R version and the package to install.

You will need to install `rv`

Then run:

```bash
rv init .
rv sync
```

And do the same in `Notebooks/RStats`:

```bash
cd notebooks/RStats
rv init .
rv sync
```

## uv for Figures.ipynb

```bash
cd notebooks/PythonFigures
uv sync
uv run --with jupyter jupyter lab
```

add packages with `uv add <packagename>`

## Quarto

Now you can first preview, then render

```bash
quarto preview --no-browser
quarto render
```
