# Projeto Galleria

[Galleria Mobile](/img/version-mobile.jpg)

[Galleria Desktop](/img/version-desktop.jpg)

## Menu

- [Projeto Galleria](#projeto-galleria)
  - [Menu](#menu)
    - [Apresentação](#apresentação)
    - [Objetivo](#objetivo)
    - [Deploy](#deploy)
    - [Techs utilizadas](#techs-utilizadas)
    - [O que aprendeu](#o-que-aprendeu)
    - [Status do projeto](#status-do-projeto)

### Apresentação

Galeria de fotos e imagens diversos, landing page com links de navegação e cards de fotos.
Aplicação para ser usada em diversas áreas.

### Objetivo

Aprender utilizar os conceitos e propriedades basicas do SASS. Pra saber mais Acesse o menu [O que aprendeu](#o-que-aprendeu).

### Deploy

- Link : <a href="https://jose-carlos-gallery-photos.netlify.app/" target="_blank">Gallery Photos</a>

### Techs utilizadas

<img src='https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white'/>
<img src='https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white'/>
<img src='https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white'/>

### O que aprendeu

- #### Pré-processando

  CSS por si só pode ser divertido, mas as folhas de estilo estão ficando maiores, mais complexas e mais difíceis de manter. É aqui que um pré-processador pode ajudar. O Sass possui recursos que ainda não existem em CSS , como aninhamento, mixins, herança e outros recursos interessantes que ajudam você a escrever CSS ROBUSTO E DE FÁCIL MANUTENÇÃO.

  Assim que você começar a mexer no Sass, ele pegará seu arquivo Sass pré-processado e o salvará como um arquivo CSS normal que você pode usar em seu site.

  A maneira mais direta de fazer isso acontecer é no seu terminal. Uma vez que o Sass esteja instalado, você pode compilar seu Sass para CSS usando o sass comando. Você precisará informar ao Sass de qual arquivo compilar e para onde enviar o CSS . Por exemplo, a execução sass input.scss output.cssde seu terminal levaria um único arquivo Sass, input.scss, e compilaria esse arquivo para output.css.

  Você também pode assistir a arquivos ou diretórios individuais com o --watchsinalizador. O sinalizador de observação diz ao Sass para observar seus arquivos de origem quanto a alterações e recompilar o CSS toda vez que você salvar seu Sass. Se você quiser assistir (em vez de compilar manualmente) seu input.scssarquivo, basta adicionar o sinalizador de observação ao seu comando, assim:

  ```cmd
  sass --watch input.scss output.css
  ```

  Você pode observar e enviar para diretórios usando caminhos de pasta como entrada e saída e separando-os com dois pontos. Neste exemplo:

  ```cmd
  sass --watch app/sass:public/stylesheets
  ```

  O Sass observaria todos os arquivos na app/sasspasta em busca de alterações e compilaria o CSS para a public/stylesheets pasta.

- #### Váriaveis

  Pense nas variáveis ​​como uma forma de armazenar informações que você deseja reutilizar em toda a sua folha de estilo. Você pode armazenar coisas como cores, pilhas de fontes ou qualquer valor CSS que você acha que deseja reutilizar. Sass usa o $ símbolo para tornar algo uma variável. Aqui está um exemplo:

  ```sass
    $font-stack: Helvetica, sans-serif
    $primary-color: #333

    body
      font: 100% $font-stack
      color: $primary-color
  ```

  Quando o Sass é processado, ele pega as variáveis ​​que definimos para o `sass$font-stacke` e gera o `CSS $primary-color` normal com nossos valores de variáveis ​​colocados no CSS. Isso pode ser extremamente poderoso ao trabalhar com cores de marca e mantê-las consistentes em todo o site.

### Status do projeto

<img src="http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge"/>
