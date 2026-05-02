# 🤖 Claude PR Review

Automated AI-powered code review for Pull Requests using **Claude (Anthropic)** and **GitHub Actions**.

## How it works

1. A developer opens a PR targeting `main`
2. GitHub Action triggers automatically
3. Claude analyzes the diff and generates a detailed Markdown report
4. The report is uploaded as a downloadable artifact
5. You review the report and decide to merge or reject manually

## Setup

### 1. Add your Anthropic API Key as a GitHub Secret

```
Settings → Secrets and variables → Actions → New repository secret
Name: ANTHROPIC_API_KEY
Value: sk-ant-xxxxxxxxxx
```

### 2. That's it!

Every PR to `main` will now be automatically reviewed by Claude.

## Downloading the Report

```
GitHub → PR → Checks → review → Summary → Artifacts → claude-review-{PR_NUMBER}.md
```

## Report Structure

- 📋 Summary of Changes
- 🐛 Potential Bugs
- 🔒 Security
- ⚡ Performance
- 🧹 Code Quality
- ✅ Positives
- 💡 Improvement Suggestions
