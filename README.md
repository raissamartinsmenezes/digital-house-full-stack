# HTML + CSS

[Aula 28/10](#aula28out)\
[Aula 30/10](#aula30out)\
**[Estudos Extras](#estudosExtras)**
**[Anotações de Aula](#anotacoesAula)**

--- 

#### ATALHOS

* CTRL (segura) + K + O > abre a tela de pastas 
* CTRL + N > abre uma nova aba em branco 
* `ol>li*3` > atalho para a construção do HTML 
* Com o lado direito do mouse, em cima do arquivo > **Copy Path** 
* CTRL + B > esconde e mostra o explorer que mostra os arquivos na lateral esquerda
* `h3{conteúdo da tag}` > atalho para a construção do conteúdo dentro da tag
* Volta o caractere ou `CTRL + espaço` quando a caixinha de autocomplete desaparecer no vscode
* `alt + seta para cima/seta para baixo` para articular a linha de código para cima ou para baixo
* Criando a pasta e o arquivo do css:
	- No HTML enquanto estiver escrevendo a tag `link` ele vai abrir o autocomplete **emmet** com opções, escolher a `link:css + enter`
	- Ele vai criar a tag completa `<link rel="stylesheet" href="style.css">`
	- Adicionar o caminho da pasta `<link rel="stylesheet" href="css/style.css">`
	- Em cima de `href="css/style.css"` clicar `CTRL + enter` > **Create file** e ele vai criar a pasta com o arquivo  
* Seleciona as linhas que você quer copiar + `alt + shift + seta para cima/seta para baixo` e ele vai copiar a linha
* `CRTL + D` seleciona a primeira palavra se apertar de novo ele seleciona a próxima palavra e você pode mudar os nomes das duas ao mesmo tempo 
* `div>input+label` cria div mãe e dentro dela os filhos input e label 

#### LINKS ÚTEIS 

[Full Stack Open 2019 - Curso](https://fullstackopen.com/)\
[Commonmark.org - Jogo para aprender linguagem Markdown](https://commonmark.org/)\
[Badges Github - Site para criar distintivos para a documentação do Github](https://shields.io/)\
[Plug-in JSON Formatter para o Chrome](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=pt-BR)\
[Validador de HTML W3C - Markup Validation Service](https://validator.w3.org/)\
[The Front-end Cheklist](https://frontendchecklist.io/)

#### CAMINHOS RELATIVOS E ABSOLUTOS

*Pesquisar!!!*

---

<div id="aula28out"></div>

## Aula 28/10

### HTML (Hyper Text Markup Language)

Ordem de aula:
1. Analisamos o site da [UOL](https://www.uol.com.br/) através do Chrome [DevTools](https://developers.google.com/web/tools/chrome-devtools?hl=pt-br)
2. Abrimos a aba Elements e inspecionamos os elementos `<html> <head> <body>`
3. Ainda na aba Elements o professor explicou sobre os **atributos** e sua sintaxe
4. Depois disso abrimos o bloco de notas e construimos a seguinte estrutura:

```html
<!DOCTYPE html> <!-- essa tag faz o browser entender que estamos usando o HTML5 -->
<html>
<head>
	<meta charset="UTF-8">
	<title>Meu site</title>
</head>
<body>
	<h1>Título Principal</h1>
	<h2>Subtítulo menos importante</h2>
	<h6>Título que ninguém vai ser lido por ninguém</h6>
	Olá, mundo!
	<p>Mussum Ipsum, cacilds vidis litro abertis. In elementis mé pra quem é amistosis quis leo. Tá deprimidis, eu conheço uma cachacis que pode alegrar sua vidis. Não sou faixa preta cumpadi, sou preto inteiris, inteiris. Todo mundo vê os porris que eu tomo, mas ninguém vê os tombis que eu levo!</p>
	<ol type="a">
		<li>Item 1</li>
		<li>Item 2</li>
		<li>Item 3</li>
	</ol>
</body>
</html>
```

Sempre que for criar a tag no **vscode**, escrever apenas o nome da tag `a + enter` para que ele realize o autocomplete com os atributos obrigatórios, caso o contrário, se escrever com os fechamentos `<a> + enter` ele vai criar apenas a tag sem os atributos.  

#### ELEMENTO HTML

É considerado um **elemento HTML** quando ele é formado por uma tag de abertura e outra de fechamento.

`<body>` tag de abertura\
`</body>` tag de fechamento

#### ATRIBUTOS 

`atributo="valor"` atributo recebe o valor (ref: [Gustavo Guanabara](https://www.youtube.com/watch?v=rsFCVjr5yxc))

Nem todo atributo precisa de valor!

`charset="utf-8"` atributo **conjunto de caracteres** com valor **UTF-8 (8-bit Unicode Transformation Format)**, este valor é um esquema de codificação *(character encoding)* que basicamente mapeia os **bits** (zeros e uns) em **caracteres**.

[Unicode e UTF-8](https://www.ime.usp.br/~pf/algoritmos/apend/unicode.html)

`rel=""` atributo usado apenas quando o `href=""` é referenciado, utilizado principalmente em se trantando de performance de SEO. Usada para atribuir uma relação entre o documento atual e o linkado pelo `href=""`.

[Atributo `rel=""` e seus valores](https://ferramentasseo.club/rel-nofollow-noreferrer-noopener-external)\
[Atributo `rel=""` - W3C](https://www.w3schools.com/TAGS/att_a_rel.asp)

`title=""` atributo que cria uma caixinha de título e pode ser usado com qualquer tag, é uma tag importante para rankeamento de SEO.

#### INDENTAÇÃO

A [indentação](https://pt.wikipedia.org/wiki/Indenta%C3%A7%C3%A3o) de código é empregada na maioria das linguagens de programação com o objetivo de **organizar/estruturar** o **código/algoritmo**, facilitando em consequência disso a **legibilidade do código**, ou seja, tornar a interpretação do código mais fácil. Além disso,é usada para **definir a hierarquia** entre as partes do código.

#### HIERARQUIA

Se o elemento estiver dentro de uma tag de abertura e fechamento, ele estará dentro de seu pai, portanto ele será filho, ele também poderá ter irmão, se outros elementos estiverem no mesmo nível que ele.

```html
<body> <!-- tag de abertura e pai de <h1> e <p> -->
    <h1></h1> <!-- filho de body e irmão de <p> -->
    <p><p> <!-- filho de body e irmão de <h1> -->
</body> <!-- tag de fechamento -->
```

#### HTML SEMÂNTICO 

[Elementos semânticos](https://www.devmedia.com.br/html-semantico-conheca-os-elementos-semanticos-da-html5/38065)

#### TAG `<meta>`

Como suas informações vem por meio de atributos, ela não precisa de fechamento.

[Elemento `<meta>` - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/meta)\
[`<meta>` TAGS](https://www.chiefofdesign.com.br/meta-tags/)

#### TAGS

**Elementos de cabeçalho**

Elementos de cabeçalho são implementados em seis níveis, `<h1>` é o mais importante e `<h6>` é o de menor importância, ou seja elas não definem o tamanho da fonte e sim a **importância**. Posso utilizar apenas **um** `<h1>` no meu `<html>`.

`<p>` tag para construção de parágrafo
`</br>` só pode ser usado para quebra de linhas dentro dos parágrafos

[Lorem Ipsum](https://br.lipsum.com/)

**Elementos de listas**

[`<ol>` - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/ol)\
[`<ul>` - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/ul)

---

<div id="aula30out"></div>

## Aula 30/10

### CSS

[Especificidade, herança e efeito cascata](https://medium.com/emanuelg-blog/entendendo-a-preced%C3%AAncia-de-estilo-em-css-especificidade-heran%C3%A7a-e-efeito-cascata-a437c4929173)

**Estilos: Externo, Interno e Inline**

[Diferença entre estilos CSS](https://www.hostinger.com.br/tutoriais/diferenca-entre-estilos-css/)

Ordem de precedência:\
8 Folha de estilo padrão do navegador do usuário\
7 Folha de estilo do usuário\
6 Folha de estilo do desenvolvedor\
5 Estilo externo (importado ou linkado)\
4 Estilo incorporado (definido na seção head do documento)\
3 Estilo inline (dentro de um elemento HTML)\
2 Declarações do desenvolvedor com !important\
1 Declarações do usuário com !important

**Seletores**
* Básicos: 
	- tipo > `<tag>`
	- classe > `.classe`
	- id > `#id`
	- universal > `*`
	- atibuto > `[attr="value"]`

[Seletores - MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Getting_Started/Seletores)\
[CSS selectors - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Selectors)\
[Pseudo-classes:](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)\
[Pseudo-elementos::](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)\
[Tabela de seletores](https://tableless.com.br/referencia-seletores-css/)\
[Teste de seletores - W3C](https://www.w3schools.com/cssref/trysel.asp)

Especificidade dos seletores:\
7 Seletores universais\
6 Tipos de seletores\
5 Classes seletoras\
4 Atributos seletores\
3 Pseudo-classes\
2 Seletores id\
1 Estilo inline

**Regra de CSS:**
```
seletor {
    propriedade: valor;
    propriedade: valor;
    propriedade: valor;
}
```

*CONTINUAÇÃO DA AULA EM 01/11*

---

<div id="estudosExtras"></div>

#### ESTUDOS EXTRAS

- [ ] Plug-in para retirar o CSS do HTML *perguntar para o professor*
- [x] **Transpila > transforma uma linguagem na outra**
- [x] **Compila > transforma para binário**
- [ ] Como transformar os bullets da `<ul>` *perguntar para o professor*
- [ ] Porque as vezes o caminho `img/imagem.jpg` não funciona e temos que colocar `./img/imagem.jpg`
- [ ] Como usar as propriedades opacity e background-image juntas?
- [ ] Como mudar as bolinhas do input para asteriscos?

---

<div id="anotacoesAula"></div>

#### ANOTAÇÕES DA AULA 01/11

`<a>` links externos e internos\
`<a>` links âncoras, email e telefone\
`<img src="" alt="" width="" height=""/>` **src** > para conteúdo, **alt** para descrição da imagem

`background-position: 100px 100px` a utilização de medidas especificas é só para contornar pequenas movimentações da imagem\
`background-attachment: fixed` a imagem fica fixa no fundo e o conteúdo rola com a barra de rolagem 

`<em>` itálico semântico\
`<strong>` ênfase semântica\
`<mark>`\
`<cite>`\
`<abbr title="Wolrd Wide Web Consortium">W3C (Abreviação)</abbr>` para mostrar o significado das abreviações

#### ANOTAÇÕES DA AULA 04/11

**Formulários**
- form
`action="script.php"` os dados que eu preenchi no formulário vão para este arquivo\ 
`method="post"` get não usamos para informações sensíveis e sim o post, pois esses dados não aparecerão na url\
`method="get"` envia as informações pela url\

- input
`type="email"` tipo de validação (text - nome, email e password)\
`name="usuario` o atributo name liga o front-end com o back-end, se eu não tenho o nome desse campo ele não existe no back-end\
`value=""`\
`required`\
`type="radio"` e `type="checkbox"`\
`placeholder="user@email.com"`\
`<label for=""></label>` é importante conectar o label ao `<input id="">` através do id por questões de acessibilidade, pois sem essa conexão o usuário só poderá clicar na bolinha e com ela, se ele clicar no nome automaticamente a bolinha será selecionada\
`<input type="radio" name=cidade>` quando o input for do tipo radio e estiver relacionado a um bloco específico, por exemplo quando quero capturar uma cidade de opções de cidade, se todos os inputs de opção não estiverem relacionados com o mesmo `name="cidade"`, não será possível selecionar apenas uma opção dentre várias\

* pseudo:seletores 
	- hover
	- active
	- input:focus





