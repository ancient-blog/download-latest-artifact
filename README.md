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

To check the list of artifacts, you can navigate to the following URL in your web browser:


[View Artifacts](https://api.github.com/repos/your-repository-owner/your-repository-name/actions/artifacts)

Replace `your-repository-owner` and `your-repository-name` in the URL with your actual repository owner and repository name. This URL will display a list of artifacts associated with the specified repository. Please make sure you have the necessary permissions to access this information.

```json
{
  "total_count": 1,
  "artifacts": [
    {
      "id": 956812721,
      "node_id": "MDg6QXJ0aWZhY3Q5NTY4MTI3MjE=",
      "name": "my-artifact",
      "size_in_bytes": 6,
      "url": "https://api.github.com/repos/ancient-blog/download-latest-artifact/actions/artifacts/956812721",
      "archive_download_url": "https://api.github.com/repos/ancient-blog/download-latest-artifact/actions/artifacts/956812721/zip",
      "expired": false,
      "created_at": "2023-10-01T07:36:11Z",
      "updated_at": "2023-10-01T07:36:12Z",
      "expires_at": "2023-12-30T07:36:00Z",
      "workflow_run": {
        "id": 6368998001,
        "repository_id": 698532264,
        "head_repository_id": 698532264,
        "head_branch": "topic/#1",
        "head_sha": "4b94934b0f83c37e0843368f4decd3ad15e19223"
      }
    }
  ]
}
```


# License

The scripts and documentation in this project are released under the [MIT License](LICENSE.md)