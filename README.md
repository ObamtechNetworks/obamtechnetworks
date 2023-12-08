<div align="center">
  <img height="150" src="https://media1.tenor.com/m/2nKSTDDekOgAAAAC/coding-kira.gif"  />
</div>

###

<div align="center">
  <a href="https://twitter.com/_obamidele" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Twitter&logo=twitter&label=&color=1DA1F2&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="twitter logo"  />
  </a>
  <a href="https://linkedin.com/in/https://www.linkedin.com/in/ipadeola-bamidele/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="linkedin logo"  />
  </a>
  <a href="https://www.youtube.com/channel/UCMq--s_nBomuZ2v1n9-H-OA" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Youtube&logo=youtube&label=&color=FF0000&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="youtube logo"  />
  </a>
</div>

###

<div align="center">
  <img src="https://visitor-badge.laobi.icu/badge?page_id=obamtechnetworks.obamtechnetworks&left_text=TL-%3EView"  />
</div>

###

<h3 align="center">Hey there 👋<br>Welcome to my Github page<br>I'm  a passionate tech enthusiast and openminded learner</h3>

###

<h3 align="left">👩‍💻  About Me</h3>

###

<p align="left">My name is Bamidele Michael<br>- 📚 I'm currently a software engineering student @ALX_SE<br>- ⚡ In my free time I code and explore new concepts</p>

###

<h3 align="left">🛠 Language and tools</h3>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="40" alt="c logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" height="40" alt="bash logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="40" alt="git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="40" alt="github logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flask/flask-original.svg" height="40" alt="flask logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="40" alt="mysql logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jquery/jquery-original.svg" height="40" alt="jquery logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/apache/apache-original.svg" height="40" alt="apache logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg" height="40" alt="django logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vagrant/vagrant-original.svg" height="40" alt="vagrant logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" height="40" alt="jupyter logo"  />
</div>

###

<h3 align="left">🔥   My Stats :</h3>

###

<div align="center">
  <img src="https://streak-stats.demolab.com?user=obamtechnetworks&locale=en&mode=daily&theme=dark&hide_border=false&border_radius=5&order=3" height="220" alt="streak graph"  />
</div>

###

<br clear="both">

<img src="https://raw.githubusercontent.com/obamtechnetworks/obamtechnetworks/output/snake.svg" alt="Snake animation" />
name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

###
