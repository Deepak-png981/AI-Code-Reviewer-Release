# Review Raccoon

A GitHub Action that automatically performs code reviews on pull requests using LLMs. This action analyzes code and provides helpful feedback, suggestions, and potential issue detection directly as comments on your PRs.

## Features

- Automatic code review on pull request changes
- Configurable file exclusions
- Easy setup with minimal configuration

## Setup

### Prerequisites

- A GitHub repository with Actions enabled
- An OpenAI API key

### Usage

Add the following to your GitHub workflow file (e.g., `.github/workflows/review-    raccoon.yml`):

```yaml
name: Code Review with OpenAI
on:
  pull_request:
    types:
      - opened
      - synchronize
permissions: write-all
jobs:
  code_review:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3
      - name: Review Raccoon
        uses: Deepak-png981/AI-Code-Reviewer-Release@v0.1.3
        with:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          OPENAI_API_KEY: ${{ secrets.OPENAI_API_KEY }}
          OPENAI_API_MODEL: "gpt-4-1106-preview"
          exclude: "yarn.lock,dist/**"
```


