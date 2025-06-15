<p align="center">
  <img
    src="https://github.com/aaryasoni/aaryasoni/raw/output/github-contribution-grid-snake.svg"
    alt="GitHub contribution grid"
    width="70%"
  />
</p>

<h1 align="center">Hello, I’m Aarya! 👋</h1>

<p align="center">
  <em>“I don’t do magic—but I <strong>do</strong> full‑stack.”</em><br>
  <em>From front‑end spells to back‑end levitation.</em>
</p>

<p align="center">
  <a href="mailto:your.email@example.com">
    <img src="https://img.shields.io/badge/📧-Email-black?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://www.linkedin.com/in/aarya-soni" target="_blank">
    <img src="https://img.shields.io/badge/🔗-LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=aaryasoni&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views" />
</p>

---

## 🧰 Tech Stack
<p align="center">
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Tailwind-38B2AC?style=flat&logo=tailwindcss&logoColor=white" alt="TailwindCSS" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white" alt="Node.js" />
</p>

---

## ⚡ Projects

- **[EcoWiz](https://github.com/aaryasoni/ecowiz)** – A green-living dashboard built with Next.js and TailwindCSS.
- **[Portfolio‑AI](https://github.com/aaryasoni/portfolio-ai)** – AI‑driven stock portfolio optimizer using Python & React.
- **[Parkinson’s Detector](https://github.com/aaryasoni/parkinsons-detector)** – A neural‑network based early detection tool.

---

## 📊 GitHub Stats
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=aaryasoni&show_icons=true&theme=dark" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=aaryasoni&theme=dark" alt="GitHub Streak" />
</p>

---

### 🛠️ Contribution Grid Snake Setup

Set up GitHub Actions to generate your Snake daily:

```yaml
# .github/workflows/snake.yml
name: github contribution snake

on:
  schedule:
    - cron: '0 0 * * *' 
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Generate contribution grid snake
        uses: tanpatil27/github-contribution-grid-snake@main
        with:
          width: 700
          color: teal
          background: "00000000"

      - name: Commit snake image
        run: |
          git config user.name 'github-actions[bot]'
          git config user.email '41898282+github-actions[bot]@users.noreply.github.com'
          git add output/github-contribution-grid-snake.svg
          git commit -m 'Update contribution grid snake' || echo "No changes"
          git push
