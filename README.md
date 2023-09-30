# Download the latest artifacts Action

This GitHub Action allows you to download the latest artifacts from a GitHub repository using the GitHub API.

## Inputs

| Name   | Description                                 | Default           | Required |
|--------|---------------------------------------------|-------------------|----------|
| owner  | Your repository owner                      | ancient-blog      | No       |
| repo   | Your repository name                       | hugo.github.io    | No       |
| name   | Your artifact name                         | voicevox-data     | No       |
| token  | A personal access token from the workflow  |                   | Yes      |
| path   | Path to save the downloaded artifact files | `${{ github.workspace }}/artifact` | No       |

## Outputs

This action doesn't produce any outputs.

## Example Usage

```yaml
- name: Download Artifacts
  uses: ancient-blog/download-artifacts-action@v1
  with:
    owner: your-repository-owner
    repo: your-repository-name
    name: your-artifact-name
    token: ${{ secrets.GITHUB_TOKEN }}
    path: ${{ github.workspace }}/my-artifacts
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE.md)