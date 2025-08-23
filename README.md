# Clona o seu repo
git clone https://github.com/pauloFrancisconi/mkdocs-example.git
cd mkdocs-example

# Remove o vínculo com o seu remoto
git remote remove origin

# Instala as dependencias do projeto
poetry install

# Cria um repo novo no GitHub (ex: "meu-mkdocs")
# Depois adiciona esse novo repo como remoto
git remote add origin https://github.com/AMIGO-USERNAME/meu-mkdocs.git


# Faz o primeiro push pro repo dele
git push -u origin main

# Instala a dependencia de deploy do gh-pages
poetry add mkdocs-gh-deploy --group dev
poetry run mkdocs serve -- gera site local
poetry run mkdocs build -- gera os arquivos em html no projeto
poetry run mkdocs gh-deploy -- faz a publicação no github pages




