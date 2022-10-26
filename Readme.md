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

- #### Aninhamento

  Ao escrever HTML , você provavelmente notou que ele possui uma hierarquia visual e aninhada clara. CSS , por outro lado, não.

  O Sass permitirá que você aninhe seus seletores CSS de uma maneira que siga a mesma hierarquia visual do seu HTML. Esteja ciente de que regras excessivamente aninhadas resultarão em CSS SUPERQUALIFICADO que pode ser difícil de manter e geralmente é considerado uma prática ruim.

  Com isso em mente, aqui está um exemplo de alguns estilos típicos de navegação de um site:

  ```sass
    nav
      ul
        margin: 0
        padding: 0
        list-style: none

      li
        display: inline-block

      a
        display: block
        padding: 6px 12px
        text-decoration: none
  ```

  Você notará que os seletores ul, lie aestão aninhados dentro do navseletor. Esta é uma ótima maneira de organizar seu CSS e torná-lo mais legível.

- #### Parciais

  Você pode criar arquivos Sass parciais que contêm pequenos trechos de CSS que podem ser incluídos em outros arquivos Sass. Esta é uma ótima maneira de modularizar seu CSS e ajudar a manter as coisas mais fáceis de manter. Um parcial é um arquivo Sass nomeado com um sublinhado inicial. Você pode nomear algo como \_partial.scss. O sublinhado permite ao Sass saber que o arquivo é apenas um arquivo parcial e que não deve ser gerado em um arquivo CSS . Parciais Sass são usados ​​com a @use regra.

- #### Módulos

  Compatibilidade: | Dart Sass | desde 1.23.0 | LibSass | ✗ | Ruby Sass | ✗ |

  Você não precisa escrever todos os seus Sass em um único arquivo. Você pode dividir como quiser com a @useregra. Esta regra carrega outro arquivo Sass como um módulo , o que significa que você pode consultar suas variáveis, mixins e funções em seu arquivo Sass com um namespace baseado no nome do arquivo. Usar um arquivo também incluirá o CSS que ele gera em sua saída compilada!

  Arquivo SASS: \_base.sass

  ```sass
    // _base.sass
    $font-stack: Helvetica, sans-serif
    $primary-color: #333

    body
      font: 100% $font-stack
      color: $primary-color
  ```

  Arquivo Sass: styles.sass repare que o arquivo \_base.sass está sendo chamado dentro
  do arquivo styles.sass através do @use

  ```sass
    // styles.sass
    @use 'base'

    .inverse
      background-color: base.$primary-color
      color: white
  ```

  Observe que estamos usando @use 'base';no styles.scssarquivo. Quando você usa um arquivo, não precisa incluir a extensão do arquivo. Sass é inteligente e vai descobrir isso para você.

- #### Mixins

  Algumas coisas em CSS são um pouco tediosas de escrever, especialmente com CSS3 e os muitos prefixos de fornecedores que existem. Um mixin permite criar grupos de declarações CSS que você deseja reutilizar em todo o site. Ajuda a manter seu Sass muito DRY. Você pode até passar valores para tornar seu mixin mais flexível. Aqui está um exemplo para theme.

  ```sass
    @mixin theme($theme: DarkGray)
      background: $theme
      box-shadow: 0 0 1px rgba($theme, .25)
      color: #fff


    .info
      @include theme

    .alert
      @include theme($theme: DarkRed)

    .success
      @include theme($theme: DarkGreen)

  ```

  Para criar um mixin você usa a @mixindiretiva e dá um nome a ela. Nós nomeamos nosso mixin theme. Também estamos usando a variável $themedentro dos parênteses para que possamos passar themeo que quisermos. Depois de criar seu mixin, você pode usá-lo como uma declaração CSS começando com @includeseguido pelo nome do mixin.

### Status do projeto

<img src="http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge"/>
