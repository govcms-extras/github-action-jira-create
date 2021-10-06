# Jira Create

This project is forked from https://github.com/atlassian/gajira-create

Please use the offical project if possible

## What this project can do

* Create new Jira issue

## Usage

```
- name: Jira issue:create
  uses: uses: govcms-extras/github-action-jira-create@main
  with:
    project: EXAMPLE
    issuetype: Task
    summary: |
      Build completed for ${{ github.repository }}
    description: |
      Compare branch
    fields: '{"customfield_10171": "test"}'

- name: Log created issue
  run: echo "Issue ${{ steps.create.outputs.issue }} was created"
```