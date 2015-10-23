##### Unoesc Chapecó
##### Pós-Graduação em Desenvolvimento Web, Cloud e Dispositivos Móveis - WebMob
##### Disciplina: Desenvolvimento com HTML5 e CSS3
##### Professor: Jean Carlo Nascimento
##### Acadêmico: Charles Busatta Cunico {charlesbc@unochapeco.edu.br}
## Artigo de revisão de CSS3
#### 1. Funcionalidade: gradients
##### O que é?
Gradients é um novo tipo de representação de imagem 2D, adicionado ao módulo de imagem do CSS3. Com gradients é possível exibir transições suaves entre duas ou mais cores especificadas, sem precisar utilizar arquivos de imagem para este efeito, diminuindo o consumo de banda e o tempo de download. Também apresenta maior flexibilidade para ajustes e melhor qualidade ao ampliar o zoom.
##### Onde usar:
É possível utilizar gradients em qualquer elemento com a propriedade background.
##### Como usar:
Existem dois tipos de gradients: linear e radial. O tipo linear é criado utilizando a função linear-gradient, definindo um ponto inicial ou uma direção (específica ou ângulo), e as cores de parada. Será renderizada a transição entre cada cor de parada, por isso é necessário informar ao menos duas cores.
```css
linear-gradient([ <ângulo> | to <direção> ,]? <cor-de-parada> [, <cor-de-parada>]+)
               \----------------------------/ \-----------------------------------/
              Definição da linha de gradiente         Lista de cores de parada 

onde <direção> = [left | right] || [top | bottom]
   e <cor-de-parada> = <color> [ <percentage> | <length> ]?
```
O tipo radial é criado utilizando a função radial-gradient com sintaxe semelhante a linear-gradient, exceto por poder especificar a forma final do gradiente (círculo ou elípse) bem como o seu tamanho. A seguir a sintaxe para radial-gradient.
```css
radial-gradient(  [ circle || <length> ] [ at <position> ]? ,
                | [ ellipse || [<length> | <percentage> ]{2}] [ at <position> ]? ,
                | [ [ circle | ellipse ] || <extent-keyword> ] [ at <position> ]? ,
                | at <position> ,
               <color-stop> [ , <color-stop> ]+ )
onde <extent-keyword> = closest-corner | closest-side | farthest-corner | farthest-side
   e <color-stop> = <color> [ <percentage> | <length> ]?
```
##### Exemplo de uso:
Exemplo com a função linear-gradient:
```css
.gradient {
   background: linear-gradient(to right, blue, white);
   height: 50px;
}
```
Exemplo com a função radial-gradient:
```css
.gradient {
   background: radial-gradient(red, yellow, rgb(30, 144, 255));
   height: 100px;
   width: 100px
}
```
##### Referencias:
[http://www.webreference.com/authoring/css3/2.html](http://www.webreference.com/authoring/css3/2.html)</br>
[https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient](https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient)</br>
[https://developer.mozilla.org/en/docs/Web/CSS/radial-gradient](https://developer.mozilla.org/en/docs/Web/CSS/radial-gradient)</br>

#### 2. Funcionalidade: columns
##### O que é?
A propriedade CSS3 columns permite facilmente formatar um texto separando-o em diversas colunas. Possibilita que as colunas do texto sejam montadas de duas maneiras: definindo a largura para cada coluna ou definindo o número de colunas.
##### Onde usar:
Em qualquer elemento que contenha o texto a ser dividido em colunas.
##### Como usar:
```css
seletor {
   columns : <'column-width'> || <'column-count'>;
}
```
##### Exemplo de uso:
Definindo o número de colunas:
```css
.texto {
   -webkit-column-count: 4; /* Chrome, Safari, Opera */
   -moz-column-count: 4; /* Firefox */
   column-count: 4;
}
```
Definindo o tamanho:
```css
.texto {
    -webkit-column-width: 150px; /* Chrome, Safari, Opera */
    column-width: 150px;
}
```
##### Referencias:
[http://www.css3.info/preview/multi-column-layout/](http://www.css3.info/preview/multi-column-layout/)</br>
[http://www.w3schools.com/css/css3_multiple_columns.asp](http://www.w3schools.com/css/css3_multiple_columns.asp)</br>

#### 3. Funcionalidade: text-shadow
##### O que é?
Text-shadow é uma nova propriedade CSS3 que adiciona sombras ao texto em uma página web. Aceita uma lista de definições de sombras separadas por vírgula e text-decorators do elemento.
##### Onde usar:
Em qualquer elemento que contenha o texto a ser aplicada a sombra.
##### Como usar:
A sintaxe para text-shadow é seguinte
```css
seletor {
   text-shadow: [ <length>{2,3} && <color>? ]#
}
onde <length> = offset-x | offset-y | blur-radius
   e <color> = color|none|initial|inherit
```
##### Exemplo de uso:
```css
h2 {
   text-shadow: red 3px -2px 3px;
}
```
##### Referencias:
[http://www.w3schools.com/cssref/css3_pr_text-shadow.asp](http://www.w3schools.com/cssref/css3_pr_text-shadow.asp)</br>
[https://developer.mozilla.org/en/docs/Web/CSS/text-shadow](https://developer.mozilla.org/en/docs/Web/CSS/text-shadow)</br>

#### 4. Funcionalidade: box-shadow
##### O que é?
A propriedade box-shadow envolve um ou mais efeitos de sombra de um elemento, representados em uma lista separada por vírgula. Diferente da propriedade text-shadow que a sombra é aplicada no texto, em box-shadow é projetada uma sombra a partir do frame de qualquer elemento.
Se é aplicada a propriedade box-shadow em um elemento com border-radius, a sombra assumirá os mesmos cantos arredondados do elemento.
##### Onde usar:
Em qualquer elemento HTML.
##### Como usar:
A sintaxe para box-shadow é a seguinte.
```css
seletor {
   box-shadow: [ inset? && <length>{2,4} && <color>? ]#
}
onde <length> = offset-x | offset-y | blur-radius | spread-radius | color
   e <color> = color |inset|initial|inherit
```
##### Exemplo de uso:
```css
.shadow {
   box-shadow: -5px 10px 5px black;
   background-color: gray;
   height: 100px;
   width: 100px;
}
```
##### Referencias:
[http://www.w3schools.com/cssref/css3_pr_box-shadow.asp](http://www.w3schools.com/cssref/css3_pr_box-shadow.asp)</br>
[https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)</br>

#### 5. Funcionalidade: word-wrap
##### O que é?
É uma propriedade inventada pela Microsoft e adicionada ao CSS3. Word-wrap possibilita que palavras muito extensas sejam quebradas para as próximas linhas, o que resolve problemas como quando um texto possui uma palavra tão grande que extrapola o seu recipiente.
##### Onde usar:
Pode ser aplicado em qualquer elemento que contenha texto o qual deseje aplicar a quebra de palavra em nova linha.
##### Como usar:
A sintaxe para word-wrap é a seguinte
```css
seletor {
   word-wrap: normal | break-word | inherit | initial;
}
```
##### Exemplo de uso:
```css
p {
   width: 13em;
   background: gold;
   word-wrap: break-word;
}
```
##### Referencias:
[http://www.css3.info/preview/word-wrap/](http://www.css3.info/preview/word-wrap/)</br>
[http://www.w3schools.com/cssref/css3_pr_word-wrap.asp](http://www.w3schools.com/cssref/css3_pr_word-wrap.asp)</br>

#### 6. Funcionalidade: text-overflow
##### O que é?
A propriedade text-overflow do CSS3 determina de que forma será sinalizado um conteúdo que ultrapassou o limite de seu contêiner e que não está sendo exibido para o usuário. O conteúdo pode ser cortado, exibir reticências ou apresentar uma sequência personalizada.
##### Onde usar:
Pode ser utilizado nos elementos de bloco de conteúdo.
##### Como usar:
A sintaxe para utilização de text-overflow é a seguinte:
```css
seletor {
   text-overflow: [ clip | ellipsis | <string> ]{1,2};
}
```
##### Exemplo de uso:
```css
p {
   white-space: nowrap;
   width: 100%;                   
   overflow: hidden; /* valor de "overflow" deve ser diferente de "visible" */ 
   text-overflow: ellipsis;
}
```
##### Referencias:
[https://developer.mozilla.org/en/docs/Web/CSS/text-overflow](https://developer.mozilla.org/en/docs/Web/CSS/text-overflow)</br>
[https://css-tricks.com/almanac/properties/t/text-overflow/](https://css-tricks.com/almanac/properties/t/text-overflow/)</br>

#### 7. Funcionalidade: web fonts
##### O que é?
Web fonts permite que o autor especifique fontes online para serem utilizadas em sua página web. As regras de @font-face eliminam a necessidade de possuir a fonte instalada no computador, podendo o autor definir suas próprias fontes.
##### Onde usar:
Em qualquer elemento que contenha o texto a ser formatado com a fonte desejada.
##### Como usar:
Deve ser definido o nome da fonte e em seguida especificar o arquivo da fonte. A sintaxe utilizada é apresentada a seguir.
```css
@font-face {
   [ font-family: <family-name>; ] ||
   [ src: [ <uri> [format(<string>#)]? | <font-face-name> ]#; ]
}
```
##### Exemplo de uso:
```css
@font-face {
   font-family: myFirstFont;
   src: url(sansation_light.woff);
}

div {
   font-family: myFirstFont;
}
```
##### Referencias:
[http://www.w3schools.com/css/css3_fonts.asp](http://www.w3schools.com/css/css3_fonts.asp)</br>
[https://developer.mozilla.org/en/docs/Web/CSS/@font-face](https://developer.mozilla.org/en/docs/Web/CSS/@font-face)</br>

#### 8. Funcionalidade: transform
##### O que é?
A propriedade transform permite aplicar transformações 2D e 3D em um elemento, tais como rotação, escala, movimento, inclinação, entre outros.
##### Onde usar:
Pode ser aplicado somente em elementos transformáveis.
##### Como usar:
A sintaxe para aplicar uma rotação 2D com transform é mostrada a seguir.
```css
seletor {
   transform: [ rotate(angle) ];
}
```
##### Exemplo de uso:
```css
div {
   width: 220px;
   height: 120px;
   background-color: red;
   /* Rotate div */
   -webkit-transform: rotate(7deg); /* Chrome, Safari, Opera */
   transform: rotate(7deg);
```
##### Referencias:
[https://developer.mozilla.org/en-US/docs/Web/CSS/transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)</br>
[http://www.w3schools.com/cssref/css3_pr_transform.asp](http://www.w3schools.com/cssref/css3_pr_transform.asp)</br>

#### 9. Funcionalidade: border-image
##### O que é?
A propriedade border-image permite que, ao invés de utilizar bordas normais em volta do elemento, que sejam imagens para isso.
##### Onde usar:
É possível utilizar border-imagem em qualquer elemento que suporte a aplicação de propriedades border.
##### Como usar:
A sintaxe para a propriedade border-image é a seguinte.
```css
seletor {
   border-image: source slice width outset repeat|initial|inherit;
}
```
##### Exemplo de uso:
```css
#elemento {
   border: 12px solid transparent;
   padding: 14px;
   -webkit-border-image: url(border.png) 20% round; /* Safari */
   -o-border-image: url(border.png) 20% round; /* Opera */
   border-image: url(border.png) 20% round;
}
```
##### Referencias:
[http://www.w3schools.com/cssref/css3_pr_border-radius.asp](http://www.w3schools.com/cssref/css3_pr_border-radius.asp)</br>

#### 10. Funcionalidade: border-radius
##### O que é?
A propriedade border-radius permite que seja definido qual será o tipo de arredondamento dos cantos da borda. Existem dois tipos de curva que podem ser aplicados em cada canto borda: círculo e elípse.
##### Onde usar:
Pode ser utilizado em qualquer elemento HTML que aceite a propriedade border.
##### Como usar:
```css
seletor {
   border-radius: 1-4 length|% / 1-4 length|%|initial|inherit;
}
```
##### Exemplo de uso:
```css
.elemento {
   border: 2px solid #a1a1a1;
   border-radius: 25px;
   background: #dddddd;
   width: 200px;
}
```
##### Referencias:
[http://www.w3schools.com/cssref/css3_pr_border-radius.asp](http://www.w3schools.com/cssref/css3_pr_border-radius.asp)</br>
[https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)</br>
