# SOS-Fraldas
#Template

Instalação TailwindCSS

- Criar pasta com projeto
- Para criar arquivo de package.json rode o comando na pasta do projeto: npm init -y
- Instalação do TailwindCSS execute o comando: npm install tailwindcss postcss-cli autoprefixer
- Inicie o TailwindCSS com o comando: npx tailwind init
- Na pasta do projeto crie os arquivos: postcss.config.js

// postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  }
}

- Na pasta do projeto crie o arquivo na pasta como segue a seguir: css/tailwind.css. Em seguida insira o código: 

@tailwind base;
@tailwind components;
@tailwind utilities;

- No arquivo: package.json acrescente a informação abaixo logo antes da chave-valor: 

  "scripts": {
    "build": "postcss css/tailwind.css -o public/build/tailwind.css",
    "test": "echo \"Error: no test specified\" && exit 1"
  },

logo em seguida, no seu terminal digite o comando para atualizar o arquivo: npm run build

- Após ter concluído todos os passos anteriores você irá criar dentro da pasta /public o arquivo index.html. 
- Acrescente o link de style criado. Ele irá referenciar ao css da pasta build.
<link rel="stylesheet" href="build/tailwind.css">
- Acrescente um <h1> ao body. Em seguida execute o comando: live-server public. Irá direcionar para o seu navegador de internet. Pronto, seu TailwindCSS está configurado. Agora só aproveitar da documentação no site oficial. ;)
