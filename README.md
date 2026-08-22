# Hi there, I'm Sandhya 👋
### Aspiring Data Scientist | B.Tech Computer Science Student

<p align="left">
  <img src="https://komarev.com/ghpvc/?username=your-github-username&label=Profile%20views&color=0e75b6&style=flat" alt="Profile Views" />
</p>

## 💫 About Me:
* 🎓 B.Tech Computer Science student at Future University (Class of 2028).
* 🔭 I’m currently working on: Exploring complex data concepts for academic thesis work and building practical Python scripts.
* 🌱 I’m currently learning: Advanced AI models, exploratory data analysis, and expanding my object-oriented programming logic in Java.
* 💼 Portfolio Highlights: Developed automated tools like a sleep reminder and a news-fetching script, alongside interactive Python applications (KBC simulation, logic games).
* 🏆 Hackathon Participant: Competed and collaborated at the RBMI Institute hackathon in Bareilly.
* 💬 Ask me about: **Python, SQL, Power BI, and Artificial Intelligence fundamentals.**
*
## 💻 My Tech Stack
<p align="left">
  <!-- Core Languages & DB -->
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" alt="Java" />
  
  <!-- Data & AI Tools -->
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/Artificial_Intelligence-FF6F00?style=for-the-badge&logo=openai&logoColor=white" alt="AI" />
</p>


## 📊 GitHub Analytics
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=your-github-username&show_icons=true&theme=tokyonight" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=your-github-username&layout=compact&theme=tokyonight" alt="Top Languages" />
</p>

## 📈 Contribution Graph
<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=your-github-username&theme=tokyonight" alt="Activity Graph" />
</p>

name: Generate Profile Stats and Snake

on:
  schedule:
    - cron: "0 0 * * *" # Runs automatically every 24 hours
  workflow_dispatch: # Allows you to run it manually

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      contents: write

    steps:
      # 1. Checkout the repository
      - uses: actions/checkout@v3

      # 2. Generate Top Contributed Repos & Language Cards
      - uses: vn7n24fzkq/github-profile-summary-cards@release
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          USERNAME: ${{ github.repository_owner }}

      # 3. Generate the Contribution Snake
      - name: Generate github-contribution-grid-snake.svg
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
      # 4. Push the generated snake images to the 'output' branch
      - name: Push Snake to Output Branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

          ## 🐍 Contribution Snake
<p align="center">
  <img src="https://raw.githubusercontent.com/your-github-username/your-github-username/output/github-contribution-grid-snake.svg" alt="Snake Animation" />
</p>

## 🏆 Top Contributed Repos
<p align="center">
  <img src="https://raw.githubusercontent.com/your-github-username/your-github-username/main/profile-summary-card-output/default/0-profile-details.svg" alt="Profile Details" />
</p>

## 💻 Top Languages
<p align="center">
  <img src="https://raw.githubusercontent.com/your-github-username/your-github-username/main/profile-summary-card-output/default/1-repos-per-language.svg" alt="Repos per Language" width="45%" />
  <img src="https://raw.githubusercontent.com/your-github-username/your-github-username/main/profile-summary-card-output/default/2-most-commit-language.svg" alt="Most Commit Language" width="45%" />
</p>
