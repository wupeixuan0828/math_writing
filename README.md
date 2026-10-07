# Math Writing — Lecture Notes

A one-hour lecture on mathematical writing, based on D. E. Knuth,
T. Larrabee, and P. M. Roberts, *Mathematical Writing* (Stanford, 1989).

The compiled handout is `math_writing.pdf`.

## Requirements

- A TeX distribution (TeX Live or MiKTeX) with `latexmk` and `pdflatex`.

## Build Locally

From the repository root:

    latexmk

This produces `math_writing.pdf`. To clean auxiliary files:

    latexmk -c

## Continuous Integration

Every push triggers two GitHub Actions workflows:

1. Build - compiles `math_writing.pdf` and uploads it as an artifact named `math-writing-pdf`.
2. Spell Check - runs `codespell` over the repository to catch typos.

Download the compiled handout from the Actions tab.

## Repository Layout

    .
    ├── .github/workflows/build.yml
    ├── latexmkrc
    ├── math_writing.tex
    └── README.md

## Reference

D. E. Knuth, T. Larrabee, P. M. Roberts. *Mathematical Writing*. Stanford, 1989.
