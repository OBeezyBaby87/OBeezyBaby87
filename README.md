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
      name:OBeezyBaby87
    on:
  # Schedule updates
  schedule: [{cron: "0 * * * *"}]
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      # See action.yml for all options
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          token: ${{ secrets.METRICS_TOKEN }}
          # GITHUB_TOKEN is a special auto-generated token restricted to current repository, which is used to push files in it
          committer_token: ${{ secrets.GITHUB_TOKEN }}
