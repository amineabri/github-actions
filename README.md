# GitHub Actions

Repository is to be used as a centrilized place for storing any reusable functionality for the GitHub Actions workflows.

Example of usage:
```
jobs:
  start-alert:
    uses: amineabri/github-actions/.github/workflows/slack-alerts.yml@main
    with:
      env_name: 'prod'
      slack_channel: '#test-notif-gautier'
      alert_type: "start"
    secrets:
      slack_webhook_url: ${{ secrets.CI_SLACK_WEBHOOK_URL }}
```
![image](https://user-images.githubusercontent.com/104840137/175294635-76b59667-48b3-4a8f-b240-ee843d7e5bd5.png)
