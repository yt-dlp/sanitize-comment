# sanitize-comment
GitHub Action to sanitize suspicious comments

## Usage
```yml
name: Sanitize comment

on:
  issue_comment:
    types:
      - created
      - edited

permissions:
  issues: write

jobs:
  sanitize-comment:
    name: Sanitize comment
    runs-on: ubuntu-latest
    steps:
      - name: Sanitize comment
        uses: yt-dlp/sanitize-comment@v1
```
