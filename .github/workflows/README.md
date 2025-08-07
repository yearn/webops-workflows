Reuse workflows here for regular devops. For example,

```

name: your repo's pr flow

on:
  pull_request:
    branches: [ main ]

jobs:
  shared-pr-workflow:
    uses: yearn/webops-workflows/.github/workflows/pull-request.yml@main
    secrets:
      TELEGRAM_BOT_TOKEN: ${{ secrets.WEBOPS_TG_TOKEN  }}
      CHAT_ID: ${{ secrets.WEBOPS_TG_CHAT_ID }}
      TOPIC_ID: ${{ secrets.WEBOPS_TG_PR_MESSAGE_THREAD_ID }}

```
