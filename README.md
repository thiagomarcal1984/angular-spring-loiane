> Link para as aulas do curso de Angular + Spring da Loiane Groner: https://www.youtube.com/playlist?list=PLGxZ4Rq3BOBpwaVgAPxTxhdX_TfSVlTcY
> 
> Repositório no GitHub: https://github.com/loiane/crud-angular-spring

# Aula 01 - Introdução
https://www.youtube.com/watch?v=qJnjz8FIs6Q&list=PLGxZ4Rq3BOBpwaVgAPxTxhdX_TfSVlTcY&ab_channel=LoianeGroner

É necessário instalar:
- a última versão LTS do NodeJS (https://nodejs.org/);
- a Angular Command Line Interface (https://angular.dev/cli)
- a IDE Visual Studio Code (https://code.visualstudio.com)

## Checando a versão do node:
```bash
node --version
# ou
node -v
```

## Instalando a Angular CLI:
```bash
npm install -g @angular/cli
# Instalando uma versão anterior à 17:
npm install -g @angular/cli@16.2.14
```
> O parâmetro `-g` indica que a instalação vai ser globao, ou seja, não vai depender do diretório onde o projeto estiver localizado.

## Checando a versão da Angular CLI:
```bash
ng --version
# Em algumas versões não usamos os hífens
ng version
```

## Criando o projeto com a Angular CLI
```bash
ng new crud-angular
? Would you like to add Angular routing? Yes
? Which stylesheet format would you like to use? SCSS   [ https://sass-lang.com/documentation/syntax#scss                ]
# Resto do output do código de criação do projeto.
```

## Instalando as extensões do Visual Studio Code para desenvolver em Angular
Pesquise por `loiane` na busca de extensões do Visual Studio Code. Lá você vai encontrar a extensão `Angular Extension Pack`, que facilita os imports do Angular.
