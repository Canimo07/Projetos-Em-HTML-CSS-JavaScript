# Projetos em HTML e CSS

 Esses são os projetos em HTML e CSS criados no canal Inteliogia do YouTube

Este repositório contém mini projetos desenvolvidos em HTML, CSS e JavaScript. >
Dockerização dos Projetos HTML/CSS/JavaScript

Este repositório contém vários mini projetos em HTML, CSS e JavaScript que foram dockerizados para facilitar a distribuição e execução. Utilizei o Nginx como servidor web dentro do container Docker para servir os arquivos estáticos.

 COMO USAR: 

1. Baixe a imagem do Docker Hub

docker pull monca07/projetos-git:latest

2. Rode o container

docker run -p 80:80 monca07/projetos-git:latest

3. Abrir no navegador

Acesse http://localhost


🛠️ Processo de criação da imagem Docker

Clonei o repositório original:

git clone https://github.com/brunorodris/Projetos-Em-HTML-CSS-JavaScript.git

Criei um arquivo Dockerfile que usa a imagem oficial do Nginx (alpine) e copia os arquivos do projeto para o diretório padrão do Nginx.
Removi o arquivo padrão index.html do Nginx e criei uma página inicial personalizada com links para os mini projetos.
Adicionei um arquivo .dockerignore para ignorar arquivos desnecessários na build.

Build da imagem localmente:
docker build -t monca07/projetos-git .

Enviei a imagem para o Docker Hub:
docker push monca07/projetos-git

⚠️ Problemas encontrados e soluções

Recebi erro 403 Forbidden ao abrir no navegador, resolvido criando uma página index.html personalizada com links.
Erro no comando docker push devido à tag incorreta. Corrigi usando o meu nome de usuário no Docker Hub na tag.
A imagem não aparecia no Docker Hub porque esqueci de dar o docker push após buildar.

📦 Imagem Docker no Docker Hub

Você pode acessar a imagem no Docker Hub:
https://hub.docker.com/r/monca07/projetos-git

✒️ Autor
Monca07



