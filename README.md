<!-- BEGIN_ACTION_DOCS -->

# github-actions-releaser
Release GitHub actions versions

# inputs
| Title | Required | Type | Description |
|-----|-----|-----|-----|
| PROJECT_NAME | True |  | The name of the project to be released |
| GITHUB_TOKEN | True |  | The file that the output report will be written to |
| RELEASE_BRANCH | True |  | The branch to release from |
<!-- END_ACTION_DOCS -->

# Example usage

```yaml
      - name: Release with semantic-release
        uses: tjtharrison/github-actions-releaser
        with:
          PROJECT_NAME: github-actions-releaser
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
