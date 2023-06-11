- 👋 Hi, I’m @vixxhesh
- 👀 I’m interested in Web Development and competetive coding
- 🌱 I’m currently learning Javascript
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me vishesh.verma1@s.amity.edu

<img align="center" src="https://github-readme-stats.vercel.app/api?username=vixxhesh&include_all_commits=true&count_private=true&show_icons=true&line_height=20&title_color=2B5BBD&icon_color=1124BB&text_color=A1A1A1&bg_color=0,000000,130F40" alt="my Github Stats"/>
<!---
vixxhesh/vixxhesh is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
name: Contribution snake

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update snake grid
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: madushadhanushka
          svg_out_path: dist/github-contribution-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
