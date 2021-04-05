# A imagem base de onde vamos partir
FROM node:latest

# Autor
LABEL maintainer="jonathan633.jl@gmail.com"

# Variavel de ambiente. Porta a ser utilizada
ENV PORT=3000

# Colocar nosso código fonte dentro da imagem
# O . serve para copiar tudo tudo que tem na pasta do Dockerfile para o /var/www
COPY . /var/www

# Assim que copiarmos o projeto, dizemos em qual diretório iremos trabalhar
WORKDIR /var/www

# Não iremos copiar a pasta node_modules para dentro da nossa imagem
# então usamos o comando abaixo para que a própria imagem instale essas dependências para nós
RUN npm install

# Toda imagem possui um comando que é executado ao iniciar
ENTRYPOINT npm start

# Aqui a porta onde a execução rodará. Detalhe para o uso da variável de ambiente sendo usada aqui
EXPOSE $PORT

# Criar imagem
# docker build -t jonathanslima/node .

# Criar container a partir dessa imagem
# docker run -d -p 8080:3000 jonathanslima/node