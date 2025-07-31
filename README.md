# Como Eu Criei Meu Projeto React + TypeScript com Vite

Vou compartilhar aqui os passos que segui para criar meu projeto usando Vite, React e TypeScript. Se você quiser reproduzir, é só seguir meu passo a passo.

---

## 1. Pré-requisitos

Antes de começar, precisei instalar o **Node.js** no meu computador, porque ele é essencial para rodar o npm e executar os comandos do projeto.

- Para isso, acessei o site oficial:  
  https://nodejs.org/

- Escolhi instalar a versão **LTS (Long Term Support)**, que é mais estável.

- Depois de instalar, confirmei se tudo estava ok rodando no terminal:

  node -v  
  npm -v

  Se aparecerem as versões, está tudo certo.

---

## 2. Criando o projeto com npm

Para criar o projeto, usei o npm, que é simples e funciona bem, principalmente no Windows:

  npm create vite@latest

Durante a criação, respondi às perguntas:

- Dei um nome para meu projeto
- Escolhi o framework React  
- Optei pelo template com TypeScript

Depois, entrei na pasta do projeto e instalei as dependências:

  cd meu-projeto  
  npm install  
  npm run dev

Isso iniciou o servidor de desenvolvimento e pude ver meu projeto rodando no navegador.



#### 2.1 Tentativa com Yarn

Alem do npm, há também a opção Yarn com o comando:

  yarn create vite

Mas tive problema porque meu usuário do Windows tinha espaços e acentos no nome de usuário (`JOÃO PAULO`), e o Yarn não conseguiu lidar com o caminho, dando erro tipo:

  'C:\Users\JOÃO' não é reconhecido como um comando interno ou externo...

Então, para evitar esse tipo de problema, usei o npm. Outra opção é criar os projetos em pastas sem espaços ou caracteres especiais.

---
## 3. Instalações adicionais

Após criação do projeto, abri o mesmo com o Visual Studio Code e executei o comando a seguir no terminal:

yarn

Ele lê o arquivo `package.json` do seu projeto e:

- Verifica todas as dependências listadas ali (bibliotecas que o projeto precisa).
- Baixa e instala essas dependências na pasta `node_modules`.
- Prepara o ambiente para que você consiga rodar e desenvolver o projeto.

---

## 4. Instalação do TypeScript

Usei TypeScript para adicionar tipagem estática ao código JavaScript. Isso ajuda a detectar erros em tempo de desenvolvimento e melhora a produtividade com sugestões e autocompletes.

Após criar o projeto com Vite, é preciso instalar o TypeScript (caso o template escolhido tenha sido o `vanilla` ou outro sem suporte embutido).

Para isso, basta executar um dos seguintes comandos no terminal, dentro da raiz do projeto:

```bash
# Usando npm
npm install --save-dev typescript

# Ou, se preferir usar yarn
yarn add --dev typescript
```

Cheque a instalação utilizando:

tsc -v

O Vite já reconhece o TypeScript automaticamente quando ele é instalado, então não preciso fazer configurações adicionais no `vite.config.js` neste momento. Após a instalação, posso começar a escrever arquivos com a extensão `.tsx` (React com TypeScript).

Caso tenha criado o projeto já com o template `react-ts`, o TypeScript já está configurado e essa etapa pode ser ignorada.


## 4. Onde buscar mais informações

Se quiser conferir a documentação oficial, onde tem bastantes informações para aprender e personalizar seu projeto, visite:

  https://vitejs.dev/

---

## Resumo dos comandos que usei

Passo                      | Comando                        | Observação
-------------------------- | ----------------------------- | ------------------------------
Instalar Node.js           | Baixar no site e instalar     | https://nodejs.org/
Criar projeto com npm      | npm create vite@latest         | Minha escolha principal
Criar projeto com yarn     | yarn create vite              | Cuidado com espaços/acento no caminho
Instalar dependências      | npm install ou yarn install    | 
Rodar servidor de desenvolvimento | npm run dev ou yarn dev  | 

---
