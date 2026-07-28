


<h2 align="center">👨‍💻 Ives Cezar</h2>
<p align="center">
Aluno em desenvolvimento de sistemas
</p>

---

### 🚀 Tech Stack
<p align="center">
  <img src="https://skillicons.dev/icons?i=html,css,js,python" />
</p>

---

### 📊 Estatísticas
<p align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=felipecsousa2000&show_icons=true&theme=radical&count_private=true" />
  <img height="180em" src="https://github-readme-streak-stats.herokuapp.com/?user=felipecsousa2000&theme=radical" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=felipecsousa2000&layout=compact&theme=radical" />
</p>

---

### 📫 Vamos nos conectar!
<p align="center">
  <a href="https://www.linkedin.com/in/ives-cezar-520a4917b/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:ivesao@gmail.com?subject=Vi+seu+perfil+no+GIThub"><img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

name: Generate GitHub contribution snake

on:
  schedule:
    - cron: '0 0 * * *' # diário à meia-noite UTC
  workflow_dispatch:
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4
        with:
          fetch-depth: 0

      - name: Generate contribution snake
        uses: Platane/snk@v3
        with:
          # Use seu nome de usuário GitHub para agendamentos; github.actor será 'github-actions' em runs agendados
          github_user_name: IvesCezar
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Commit generated SVGs
        uses: EndBug/add-and-commit@v9
        with:
          author_name: github-actions
          author_email: github-actions@github.com
          message: "chore(snake): update contribution snake"
          add: "dist/*.svg"
          push: true



<!--
**IvesCezar/IvesCezar** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

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
