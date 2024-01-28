## Olá 🖖 Seja bem vindo/a ao meu perfil do GitHub 😃

- 🌐 Programção Full Stack;
- 👨‍🎓 Formado como técnico de informática pela ETEC;
- 📚Formado em Gestão da tecnologia da informação pela FATEC.
- ⚡ Cheio de energia 🚀 e pronto para dar o meu melhor!

##


<div style="display: inline_block"><br>
<img align="center" alt="Lucas-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
<img align="center" alt="Lucas-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
<img align="center" alt="Lucas-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
<img align="center" alt="Lucas-java" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg">
<img align="center" alt="Lucas-mysql" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/mysql/mysql-original-wordmark.svg">
<img align="center" alt="Lucas-mysql" height="50" width="60"src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/27/PHP-logo.svg/1200px-PHP-logo.svg.png">
<img align="center" alt="Lucas-git" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/git/git-original-wordmark.svg">


</div>

<a href="https://github.com/Lucas300/"><img align="right" src="https://i.picasion.com/pic92/6ac43cc62d8ba558b3ad177d1efe0d9a.gif" width="150" height="150" border="0" alt="https://picasion.com/" />

##

<div> 
<a href="https://www.linkedin.com/in/lucas-daniel-souza-dias/" target="_blank"><img alt="Linkedin-lucas" src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
<a href="https://www.instagram.com/lucas.kardashiann" target="_blank"><img alt="Instagram-lucas" src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<a href="https://wa.me//5511960943768" target="_blank"><img alt="Whatsapp-lucas" src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"  target="_blank"></a> 
<a href = "mailto:ludaniel.sd@gmail.com"><img alt="gmail-lucas" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>

 # Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:


    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: lucas300 #lucas300
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
 
</div>  
  
