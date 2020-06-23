Uses the branch name to identify the JIRA ticket and adds a link to the ticket in the PR as a comment.

# Configuration

Filename: `.github/workflows/jira_assignment.yml`

Example config:

```yml
name: 'Jira Ticket Assignment'
on: pull_request

jobs:
  add-jira-ticket:
    runs-on: ubuntu-latest
    steps:
      - uses: smasala/jira-ticket-assigner@v1.0.1
        with:
          repo-token: "${{ secrets.GITHUB_TOKEN }}"
          jira-url: https://my.jira-server.com
          project-prefix: MYPROJ
```
