# actions

[![official JetBrains project](https://jb.gg/badges/official.svg)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub)

A centralized repository for reusable GitHub Actions and Workflows.

## Status

Work in progress.

## How to use

The workflows that can be reused are located in the `.github/workflows` folder. To use them in your repository, you can
call them from your own workflows. As a side note, it is not possible to import all workflows from this repository
at once. Each workflow must be called individually, such that to use it.

### Mandatory

Adding a workflow to `.github/workflows` folder such that it can be reusable is not enough. It is also necessary to
add the event: `workflow_call:` to the `on:` section of the workflow. This is necessary to make the workflow reusable.

Example: [terraform.ci.yaml](.github/workflows/terraform.ci.yaml).
