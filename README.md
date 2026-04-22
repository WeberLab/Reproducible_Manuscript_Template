# Reproducible quarto manuscript for "Title"

This is a template for generating a reproducible quarto manuscript.

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
```

add packages with `uv add <packagename>`

Then you can create/edit your `.ipynb` file with `uv run --with jupyter jupyter lab`

## Quarto

Now you can first preview, then render

```bash
quarto preview --no-browser #You don't need this flag; it just suppresses the browser from opening
quarto render
```

If you get some broken figure links, run `quarto preview` again

For publishing to github, your `.github/workflow` will fail until you run `quarto publish gh-pages`

## Snippets

<!-- TODO: upload snippets file -->

# Reminders

When your paper is published, edit the `index.qmd` front matter:

```
citation:
  container-title: Unpublished # change when published
```
