<!-- BEGIN_ACTION_DOCS -->

# github-actions-releaser
Release GitHub actions versions, including rolling major versions.

# inputs
| Title | Required | Type | Default| Description |
|-----|-----|-----|-----|-----|
| PROJECT_NAME | True |  |  | The name of the project to be released |
| GITHUB_TOKEN | True |  |  | The file that the output report will be written to |
| RELEASE_BRANCH | True |  | `main` | The branch to release from |

# outputs
| Title | Description | Value |
|-----|-----|-----|
|NEW_RELEASE | The new release version |  `${{ steps.release.outputs.NEW_RELEASE }}` | 
|NEW_MAJOR_RELEASE | The new major release version |  `${{ steps.release.outputs.NEW_MAJOR_RELEASE }}` | 
<!-- END_ACTION_DOCS -->

# Example usage

```yaml
      - name: Release with semantic-release
        uses: tjtharrison/github-actions-releaser
        with:
          PROJECT_NAME: github-actions-releaser
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
