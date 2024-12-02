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

# Aula 02 - Overview do Projeto e Instalando o Angular Material
Descrição dos arquivos gerados:
- package.json - contém as dependências do projeto JavaScript que serão instaladas.. Inclui as dependências de ambiente de produção (`dependencies`) e as de ambiente de desenvolvimento (`devDependencies`);
- package-lock.json - lista as dependências instaladas de fato no projeto;
- tsconfig.json - configurações do Type Script do projeto;
- angular.json - configurações específicas do projeto Angular;
    - sourceRoot: diretório onde a CLI vai gerar os seus objetos;
    - prefix: prefixo dos componentes gerados pela Angular CLI;
    - outputPath: diretório de saída do build da aplicação;
    - index: arquivo HTML inicial;
    - main: arquivo TypeScript inicial;
    - polyfills: arquivo que contém instruções para portabilidade da aplicação para browsers antigos;
    - assets: arquivos estáticos (imagens e ícones são exemplos: arquivos CSS e JavaScript não são necessários aqui);
    - styles: folhas de estilo globais;
    - scripts: importação de Java Scripts globais;
    - budgets: limites de tamanho para os diferentes tipos de projeto;
> Estou usando a versão 18.2.11, portanto os seguintes arquivos não foram gerados:
> - `karma.conf.js` - usado para testes;
> - `.browserlistrc` - lista de browsers;
> - o diretório `environments`.

Para servir a aplicação use:
```bash
ng serve
```

Vamos modificar o conteúdo HTML do componente principal `app.component.html`:
```HTML
<!-- src\app\app.component.html -->
<h2>Olá Mundo - Angular</h2>
```

Vamos adicionar a dependência do Angular Material ao projeto (https://material.angular.io):
```bash
ng add @angular/material
# Saída
The package @angular/material@18.2.11 will be installed and executed.
Would you like to proceed? (Y/n)
# Resto do output
? Choose a prebuilt theme name, or "custom" for a custom theme: Indigo/Pink        [ 
Preview: https://material.angular.io?theme=indigo-pink ]
# Uso das fontes padrão do Angular:
? Set up global Angular Material typography styles? Yes
# Inclusão das animações do Angular:
? Include the Angular animations module? Include and enable animations
# Resto do output
UPDATE package.json (1114 bytes)
✔ Packages installed successfully.
UPDATE src/app/app.config.ts (430 bytes)
UPDATE angular.json (3066 bytes)
UPDATE src/index.html (533 bytes)
UPDATE src/styles.scss (182 bytes)
```
> Note os arquivos modificados no fim do output.
> - `package.json`: as dependências `@angular/cdk` e `@angular/material` foram acrescentadas;
> - `app.config.ts`: acréscimo do "módulo" de `provideAnimationsAsync` para animações (em versões antigas a mudança seria em `app.module.ts`);
> - `angular.json`: acréscimo do estilo CSS referente ao tema escolhido (aqui no caso foi `azure-blue.css`);
> - `index.html`: acréscimo dos estilos CSS das fontes (_note que esses CSS não ficam salvos localmente no projeto_);
> - `styles.scss`: mudanças do estilo CSS global.
