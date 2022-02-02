## HTML5

# Definição e estrutura básica

Em 1991, Tim Berners-lee criou essa _linguagem de marcação_ para melhorar a comunicação entre ele e seus colegas de trabalho no CERN, desde então já surgiram 5 versões e o HTML se tornou a _base da web_.

Com o HTML, definimos o significado e a estrutura do conteúdo da web, além de texto, nossas páginas precisam de imagens, vídeos e vários outros formatos; para isso temos os _elementos HTML_.

Um elemento HTML é formado pela **tag de abertura e seus atributos, o conteúdo e uma tag de fechamento**. E mais a frente veremos que existem elementos que não possuem tag de fechamento.

Com esses elementos podemos agrupar tipos de conteúdo, alterar tamanho e forma de fontes e adicionar diferentes mídias a nossa página web.

E agora podemos ver como é a estrutura básica de um arquivo HTML.

A primeira linha do documento deve ser o **< !DOCTYPE html >** ou **< !doctype html >**, apesar de parecer um elemento HTML ela apenas diz ao navegador que ele está lidando com um _arquivo do tipo HTML5_. Os elementos HTML vem logo abaixo.

**< html >** : A tag **html** é a raiz do seu documento, _todos os elementos HTML devem estar dentro dela_. E nela nós informamos ao navegador qual é o idioma desse nosso documento, através do atributo **lang**, para o português brasileiro usamos **pt-BR**.

**< head >** : A tag **head** contém elementos que serão lidos pelo navegador, como os metadados ( um exemplo é o **chatset**, que é a codificação de caracteres e a mais comum é a _UTF-8_ ), o _JavaScript_ com a tag **script**, o _CSS_ através das tags **style** e **link** ( veremos a diferença quando falarmos sobre CSS ) e o título da página com a tag **title**.

**< body >** : A tag **body** é onde colocamos todo o conteúdo visível ao usuário ( textos, imagens, vídeos, etc... ).

# Semântica

Durante muitos anos o elemento padrão no HTML era a **div**, construíamos nosso conteúdo todo baseado nela, e assim nascia a _sopa de divs_.

Mas em 2014 saiu a quinta versão do HTML e com ela vieram varias mudanças importantes, como performance e acessibilidade, mas nesse curso introdutório vamos focar na semântica.

A semântica nos permite _descrever mais precisamente o nosso conteúdo_, agora um bloco de texto não é apenas uma div, agora é um **article** e tem mais significado assim. E temos vários elementos para ressignificar as dics.

**< section >** : Representa uma _seção genérica de conteúdo_ quando não houver um elemento mais específico para isso.

**< header >** : É o _cabeçalho_ da página ou de uma seção e normalmente contém _logotipos, menus, campos de busca, etc_ .

**< article >** : Representa um _conteúdo independente_ e de _maior relevância_ dentro de uma página, como um post de blog, uma notícia em uma barra lateral ou um bloco de comentários. Um article _pode conter outros elementos_, como header, cabeçalhos, parágrafos e imagens.

**< aside >** : É uma seção que _engloba conteúdos relacionados ao conteúdo principal_, como artigos relacionados, biogradia do autor e publicidade. Normalmente são representados como _barras laterais_.

**< footer >** : Esse elemento _representa o rodapé do conteúdo ou de parte dele_, pois ele é aceito dentro de vários elementos, como article, section e até o body. Exemplos de conteúdo de um **footer** são _informações de autor e links relacionados_.

**< h1...h6 >** : Eles não foram criados na versão 5 do HTML e nem são específicos para semântica, mas servem para esse propósito. São utilizados para marcar a importância dos títulos, sendo **h1** o _mais importante_ e **h6** o _menos importante_.
Uma dica: use apenas um <h1> por página, pois ele _representa o objetivo da sua página_.

# Textos e Links

A criação do HTML foi motivada pela necessidade de _compartilhar textos e documentos_, e mesmo depois de quase 30 anos, com toda a evolução da web, isso ainda representa uma boa parte do conteúdo da web.

Já falamos anteriormente sobre os elementos h1-h6 e eles são essenciais para nos _indicar visualmente a importância e localização de seções de texto na página_, mas para textos maiores e mais densos usamos o elemento **p**.

O **p** representa um parágrafo, mas ele não suporta apenas texto, podemos adicionar imagens, código, vídeos e vários outros tipos de conteúdo dentro dele.

Um outro elemento interessante e extremamente necessário na web é o **a** ( que significa anchor/âncora ), ele representa um hyperlink e interliga vários conteúdos e páginas web.

O elemento **a** tem vários atributos, mas vamos focar em dois, o **href** e o **target**.

**href** : Representa o _hyperlink_ para onde sua âncora aponta, pode ser uma página do seu ou de outro site, um e-mail e até mesmo um telefone, os dois últimos precisam dos prefixos _mailto:_ e _tel:_, respectivamente.
**target** : Serve para ajudar a abrir links em _outra aba do navegador_ usando o valor _\_blank_.

# Imagens

A web também é feita de imagens e para representá-las temos o elemento **img**, ele é um daqueles elementos _sem tag de fechamento_.

O elemento **img** é bem simples, contendo apeans 2 atributos própios, o _src_ e o _alt_.

O _src_ é obrigatório e guarda o caminho para a imagem que você quer mostrar na página.

O _alt_ não é obrigatório mas é _altamente recomandado por melhorar a acessibilidade_, ele mostra a descrição da imagem caso ela não carregue e os leitores de tela usam esse atributo para _descrever a imagem_ para o usuário saber o que ela _significa_.

# Listas

Os últimos elementos que veremos neste módulo são os relacionados a listas: **< ul >**, **< ol >** e **< li >**.

Listas servem para _agrupar uma coleção de itens_, como uma lista de ingredientes ou, como será no nosso caso, uma lista com contatos.

O elemento **ul** cria uma lista _não ordenada_, onde a ordem dos elementos não é importante, e é representada com pontos, círculos ou quadrados.

O elemento **ol** cria uma lista _ordenada_, nessa a ordem importa, portanto ela é representada com números, algarismos romanos e letras.

O elemento **li** é _um item dentro de uma lista_, pode conter vários tipos de conteúdos, como parágrafos, imagens e até outras listas.

## CSS3

# Definição e seletores

Após a criação do HTML a _necessidade de formatar as páginas_ ficou evidente, assim, em 1996, foi criada a linguagem de estilo que conhecemos por **CSS**.

A sintaxe é bem simples e pode ser explicada com a frase: _"você cria regras de estilo para elementos ou grupos de elementos"_.

Vamos usar um elemento HTML que vimos anteriormente, a âncora **< a >**, para exemplificar.

```css
a {
  color: blue;
  font-size: 14px;
}
```

Uma regra CSS é representada por um **seletor** ou um **grupo de seletors**, no nosso caso é o **< a >**, então dentro de um _par de chaves_ adicionamos as declarações, no exemplo acima estamos alterando cor e tamanho da fonte dessa âncora, as declarações são formadas por uma **propriedade** e um **valor**.

Percebam que _podemos colocar vários seletores em uma regra separando-os por vírgula_.

E há um último detalhe nesse exemplo: a pseudo-classe. Elementos HTMl sofrem alterações causadas pela interação do usuário, como mover o mouse por cima ou clicar nesse elemento.

O **a:hover** do exemplo significa que a âncora _também terá essa aparência_ quando o usuário passar o mouse por cima de um hyperlink.

# ID x Classe

```html
<header id="header" class="header"></header>
<header class="header"></header>
```

No exemplo anterior criamos uma regra que altera um elemento HTML diretamente, mas isso significa que todos os elementos **a** _ficarão com aquela aparência e normalmente temos sites mais complexos que precisam de várias regras diferentes para elementos iguais_.

Para ficar mais tangível vamos relembrar um pouco o site que começamos a fazer no módulo passado, ele tinha vários elementos header, mas _não vamos querer que o header principal tenha a mesma formatação que o header de uma outra postagem, é ai que entram os IDs e Classes_.

**ID** : É representado pelo símbolo # ( hash ) seguido de um nomee para esse ID.

**Classe** : É representada de forma parecida do ID, mas é precedida por um ponto em vez do hash.

E a diferença mais importante entre eles é a forma como devem ser usados: **o ID só pode ser usado uma vez em uma página HTML equanto a classe não tem restrições**.

# Box-model

Quando estamos criando o layout de um site o navegador representa cada elemento HTML como uma _caixa retangular, isso é o box-model_ e com CSS nós alteramos a aparência dessa caixa ( largura, altura, cor de fundo, etc... ). Essa caixa é composta por 4 áreas: _o conteúdo, o padding, a borda e a margem_.

- As margens ( margin ) são espaçamentos entre elementos;
- As bordas ( border );
- O padding é um espaçamento entre as bordas e o conteúdo, a diferença para as margens é que declarações de imagem de fundo funcionam nele;
- O conteúdo ( content ) é o que o seu bloco representa, um texto, uma imagem, um vídeo;

## Estilizando elementos

Agora que entendemos o box-model podemos focar em deixar nosso site mais bonito, então vamos repassar pelas propriedades já citadas:

# Padding e Margin

```css
.post {
  padding: 10px;
}
```

Anteriormente usamos o padding e o margin da forma mais básica, com apenas um valor, mas eles são mais poderosos que isso. Se quisermos atribuir tamanhos diferentes para cada lado do box nós podemos, e vamos ver _três formas_ de fazer isso.

A primeira é colocando _um valor para as partes superior e inferior e depois para os lados esquerdo e direito_.

```css
.post {
  padding: 10px 5px;
}
```

O valor de 10 pixels refere ao eixo Y, ou partes superior e inferior, e os 5 pixels se referem aos lados esquerdo e direito.

A segunda forma é dando _valores para cada lado do box_.

```css
.post {
  padding: 15px 10px 5px 0;
}
```

Então começamos pelo topo com 15 pixels, passamos o lado direito com 10 pixels, depois para a parte inferior com 5 pixels e por último o lador esquerdo com 0 pixels, e sempre nessa ordem.

Uma boa dica também é que quando o _valor for 0 não precisamos colocar a unidade_.

A terceira forma é com as _propriedades específicas_ para cada lado, até agora tinhamos visto atalhos para essas propriedades.

```css
.post {
  padding-top: 15px;
  padding-right: 10px;
  padding-bottom: 5px;
  padding-left: 0;
}
```

Essa opção é mais usada quando temos o mesmo valor para 3 lados, e o quarto precisa ter um valor diferente, então usamos o padding com apenas um valor e uma dessas opções para representar o lado diferente.

# Background

```css
.post {
  background-color: green;
  background-image: url("bg.png");
  background-position: top;
}
```

A propriedade **background** também é um atalho para várias propriedades, mas isso vocês podem absorver aos poucos, e uma boa opção de leitura é a documentação do MDN.

Por enquanto veremos apenas como mudar a cor de fundo.

E aqui temos 3 formas de colocar uma cor de fundo, e ainda existem outras.

A primeria é pelo nome da _cor em inglês_, a segunda é pelo _código hexadecimal_ e a terceira é usando apenas o _atalho background_.

# Border

```css
.post {
  border: 3px solid blue;
  border-top: 2px dotted green;
  border-right: 4px dashed pink;
}
```

Vimos que a propriedade border pode ter 3 valores: _a largura, a cor e o estilo_, mas existem algumas particularidades nisso.

A largura pode ser usada com várias unidades, como **px**, **em** e **mm**. A cor pode ser atribuída pelo nome ou por um código hexadecimal, assim como fizemos com o background, e o estilo é representado por palavras-chave, vamos ver algumas delas:

**solid** : Mostra uma borda simples e reta;

**dotted** : São bolinhas com um pequeno espaçamento entre elas;

**dashed**: Forma uma linha tracejada.

E aproveitando que mostrei esse código temos que falar sobre como separar a estilização dos lados de uma borda.

E se você não quiser usar a propriedade border existem as propriedades epecíficas para cada aspecto de uma borda, são elas _border-width para largura, border-color para a cor e border-style para o estilo_.

Aqui temos o mesmo código anterior de duas formas diferentes, a primeira com o atalho border e a segunda com cada propriedade específica.

```css
.post {
  border: 3px solid black;
}

.post {
  border-width: 3px;
  border-style: solid;
  border-color: black;
}
```

E depois disso podemos juntar os lados com os aspectos de uma borda e criar uma regra mais específica ainda.

```css
.post {
  border-top-width: 3px;
  border-top-color: blue;
  border-top-style: solid;
}
```

E a última propriedade é o border-radius, ele _permite arredondar os cantos de um elemento_. Podemos usar várias unidades, mas as _mais comuns são os pixels e a porcentagem_.

```css
.post {
  border-radius: 10px;
  border-radius: 50%;
  border-radius: 10% 20%;
  border-radius: 10% 20% 15% 22%;
}
```

Colocando apenas um valor mudamos todos os cantos do elemento, mas seguindo aquela mesma ordem que vimos no padding e margin ( topo, direita, inferior e esquerda ) conseguimos alterar cada canto separadamente.

## Estilizando textos

Já sabemos que podemos mudar cor e tamanho de algumas fontes, e agora vamos nos aprofundar nisso.

# font-family

```css
#title {
  font-family: Verdana;
}

.post_title {
  font-family: Verdana, Arial;
}
```

Com o **font-family** podemos alterar a fonte dos nossos textos, como uma fonte da internet ou uma que esteja instalada no nosso computador, mas vamos nos ater às _fontes seguras_, chamadas de _web safe fonts_.

Essas fontes são chamadas assim pois são _encontradas em quase todos os sistemas_ e podem ser usadas sem preocupação.

# font-size

```css
#title {
  font-size: 30px;
}

.post_title {
  font-size: 18px;
}
```

O **font-size** nos ajuda a mudar o _tamanho do texto_, existem algumas unidades de medida para ele mas por enquanto os _pixels são suficientes_ para nós.

# font-style

```css
#title {
  font-style: normal;
}

.subtitle {
  font-style: italic;
}
```

Usamos o **font-style** para tornar um texto _itálico_, na maioria das vezes usará apenas o valor italic para ele, mas se precisar tirar o itálico de um texto você pode usar o valor normal.

# font-weight

```css
#title {
  font-weight: normal;
}

.subtitle {
  font-weight: bold;
}
```

O **font-weight** altera o peso do texto, existem várias palavras chave para o valor e alguns valores numéricos. São mais usados em fontes complexas com vários pesos, em fontes simples o valor normal e bold são satisfatórios.

# text-transform

```css
#title {
  text-transform: uppercase;
}

.subtitle {
  text-transform: lowercase;
}

.post_title {
  text-transform: capitalize;
}
```

O **text-transform** altera o texto entre maiúsculo e minúsculo.

**uppercase** : Coloca todo o texto em caixa alta;

**lowercase** : Coloca todo o texto em caixa baixa;

**capitaliza** : Coloca todas as primieras letras de cada palavra em maiúsculo.

# text-decoration

```css
#title {
  text-decoration: underline;
}

.subtitle {
  text-decoration: overline;
}

.post_title {
  text-decoration: line-through;
}
```

O **text-decoration** é muito usado para dar destaque a algum texto, pois ele coloca linhas neste.

**underline** : Coloca uma linha abaixo do texto;

**overline** : Coloca uma linha acima do texto;

**line-through** : Coloca uma linha ao centro do texto.

# list-style-type

```css
ul {
  list-style-type: square;
}

ol {
  list-style-type: upper-roman;
}

ul {
  list-style-type: "\1F44D";
}
```

O **list-style-type** é utilizado para alterar o marcador das listas ( ordenadas ou não ).

# list-style-image

```css
ul {
  list-style-image: url("rocket.png");
}
```

O **list-style-image** é utilizado para alterar o marcador das listas para uma imagem.

# Dimensão e alinhamento

**width, height** : Ajustar largura e altura respectivamente, unidades em px ou %;

**max-width, max-height** : Define largura e altura máxima, o elemento irá se ajustar dependendo da situação;

**margin** : Serve alinhar elementos automaticamente e colocar espaçamento entre os elementos;

**text-align** : Serve para alinhar texto.
