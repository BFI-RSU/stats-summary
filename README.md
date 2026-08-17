# BFI official statistics summary presentation
A slide deck capturing headline statistics from each of the British Film Institute's quarterly statistical releases, covering UK box office and admissions, film and high-end TV production, and screen sector certifications.

## Workflow
1. For each new quarterly release, create a new branch from main, in the format `q#-YEAR` -- e.g. `q4-2025`.
2. Use [decktape](https://github.com/astefanutti/decktape) to save the previous quarter's slide deck as a PDF, e.g. for Q3 2025:

```
$ decktape https://bfi-rsu.github.io/stats-summary archived_presentations/bfi-q3-2025-stats.pdf
```
3. Update bfi_stats_release_data.xlsx file with the new quarter's data (data file is not stored in the repo, but is available on request).
4. Update `release_id_select` (line 33 in `index.qmd`). `release_id` is in the format calendar quarter number + year, e.g. Q2 2026 `release_id` is `22026`.
5. Quarto preview
6. Commit and push changes to the branch, and create a pull request to merge into main.
7. Quarto publish to gh-pages branch.