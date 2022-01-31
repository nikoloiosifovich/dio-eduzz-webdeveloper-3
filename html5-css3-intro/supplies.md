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
