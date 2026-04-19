# GitGitGadget workflows

This repository contains GitHub workflows, i.e. automated tasks, that keep [GitGitGadget](https://gitgitgadget.github.io/) running.

## Keeping the mirror of the Git mailing list up to date

The `sync-mailing-list-mirror.yml` workflow keeps the mirror at https://github.com/gitgitgadget/git-mailing-list of the Git mailing list mirror at https://lore.kernel.org/git up to date. Since that mirror chunks the archive by epochs, this mirror fetches each epoch into its own branch: the oldest epoch into `lore-0`, the next one into `lore-1`, etc.

Previously, this workflow lived in the `git-mailing-list` repository in the `sync` branch, which was the default branch because scheduled workflows _must_ live in the default branch.
