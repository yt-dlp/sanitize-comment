# sanitize-comment
GitHub Action to sanitize suspicious comments

## Usage
```yml
name: Sanitize comment

on:
  issue_comment:
    types: [created, edited]

permissions:
  issues: write

jobs:
  sanitize-comment:
    name: Sanitize comment
    if: vars.SANITIZE_COMMENT && !github.event.issue.pull_request
    runs-on: ubuntu-latest
    steps:
      - name: Sanitize comment
        uses: yt-dlp/sanitize-comment@v1
```
In the above example, the sanitize-comment action is only triggered if the repository has a `SANITIZE_COMMENT` variable set.
Additionally, the second condition restricts it to run on issues only. It can be removed if you want to sanitize pull request comments as well.
