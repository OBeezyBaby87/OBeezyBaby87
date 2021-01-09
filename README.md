### Hi there 👋

<!--
**OBeezyBaby87/OBeezyBaby87** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
     # Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: OBeezyBaby87
on:
  # Schedule updates
  schedule: [{cron: "0 * * * *"}]
  push: {branches: "master"}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # You'll need to setup a personal token in your secrets.
          token: ${{ secrets.METRICS_TOKEN }}
          # GITHUB_TOKEN is a special auto-generated token used for commits
          committer_token: ${{ secrets.GITHUB_TOKEN }}

          # Options
          user: OBeezyBaby87
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: America/New_York
          plugin_languages: yes
          plugin_pagespeed: yes
          plugin_pagespeed_detailed: yes
          plugin_pagespeed_screenshot: yes
          plugin_posts: yes
          plugin_posts_limit: 4
          plugin_posts_source: dev.to
          plugin_projects: yes
          plugin_projects_limit: 4
          plugin_tweets: yes
          plugin_tweets_limit: 2
