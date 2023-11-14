# actions-workflow-npm

Shared workflows for npm packages

## npm publish

```yaml
# .github/workflows/comment-npm-publish.yml
name: npm publish
on:
  issue_comment:
    types: [created]

jobs:
  npm-publish:
    uses: kapetacom/actions-workflow-npm/.github/workflows/comment-npm-publish.yml@v1
    secrets:
      github-token: ${{ secrets.GITHUB_TOKEN }}
      npm-token: ${{ secrets.NPM_TOKEN }}
```
