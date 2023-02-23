# Reagir Fundamentos

#### Curso de React

[Meu curso React](https://www.udemy.com/course/react-tutorial-and-projects-course/?referralCode=FEE6A921AF07E2563CEF)

#### Apoiar

Achou o conteúdo útil? [Você sempre pode me pagar um café](https://www.buymeacoffee.com/johnsmilga)

#### Estrutura de pastas

- node_modules
  Contém todas as dependências exigidas pelo aplicativo. Dependências principais também listadas em package.json

- público
  Contém recursos estáticos, incluindo index.html (modelo de página)
- index.html
- título
- fontes
- css
- ícone de favicon
- id="root" - todo o nosso aplicativo
  -src
  Na forma mais simples, é o cérebro do nosso aplicativo. É aqui que faremos todo o nosso trabalho. src/index.js é o ponto de entrada do JavaScript.
- .gitignore
  Especifica quais arquivos o controle de origem (Git) deve ignorar

- pacote.json
  Todo projeto Node.js tem um package.json e contém informações sobre nosso projeto, por exemplo, lista de dependências e scripts

- pacote-lock.json
  Um instantâneo de toda a árvore de dependências

- LEIA-ME
  O arquivo markdown onde você pode compartilhar mais informações sobre o projeto, por exemplo, instruções de construção e resumo

- zoom 175%

#### Remover Boilerplate

- remover pasta src
- criar pasta src

- criar index.js dentro de src

- alternar barra lateral CMD + B
- configurações de atalhos/atalhos de teclado

#### Primeiro Componente

```js
função Saudação() {
return <h2>Meu primeiro componente</h2>
}

// a função de seta também funciona

const Saudação = () => {
return <h2>Meu primeiro componente</h2>
}
```

- começa com letra maiúscula
- deve retornar JSX (html)
- sempre feche a tag <Saudação/>

##### Componente Típico

```js
// importa ou lógica

const Saudação = () => {
return <h2>Meu primeiro componente</h2>
}
exportar saudação padrão
```

##### Componente raiz (apenas um)

index.js

```js
importar Reagir de 'reagir'
importar ReactDOM de 'react-dom/client'

função Saudação() {
return <h2>Meu primeiro componente</h2>
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<Saudação />)
```

#### Possível Bug

Se por algum motivo você ainda tiver esse erro no terminal

```
Módulo não encontrado: Erro: não é possível resolver 'path/index.js'
```

Basta reiniciar o servidor

- CTRL + C (parar o servidor)
- "npm start" (inicie o servidor de desenvolvimento)

#### Extensões e settings.json

- Marca de renomeação automática
- Marca de correspondência de destaque
- personalize em settings.json
- mais bonita
- formatar ao salvar
- formatar na pasta
- Formatador padrão (Prettier - Formatador de código)

settings.json

```json
"editor.formatOnPaste": verdadeiro,
"editor.formatOnSave": verdadeiro,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"prettier.singleQuote": verdadeiro,
"mais bonito.semi": falso,
```

-Emmet

settings.json

```json
"emmet.includeLanguages": {
"javascript": "javascriptreact"
},
```

- Fragmentos ES7
- rafce (função de seta com exportação)
- rfce (função regular com exportação)
- igual ao nome do arquivo
- reagir importação automática
- desmarque
- React Snippets › Configurações: Importar React On Top

#### Primeiro Componente em Detalhe

- letra maiúscula
- deve retornar algo
- Sintaxe JSX (retorno html)
- para facilitar a nossa vida
- função de chamada sob o capô

index.js

```js
const Saudação = () => {
  return React.createElement("h2", {}, "olá mundo");
};
```

```js
função Saudação() {
retornar (
<div>
<h2>olá mundo</h2>
</div>
)
}

const Saudação = () => {
return React.createElement(
'div',
{},
React.createElement('h2', {}, 'olá mundo')
)
}
```

#### Regras JSX

- retornar um único elemento (um elemento pai)

- seção/artigo de semântica
- Fragmento - vamos agrupar elementos sem adicionar nós extras

```js
return <React.Fragment>...resto do return</React.Fragment>

// forma abreviada

retorno <>...resto do retorno</>
```

- convenção de nomenclatura da propriedade camelCase

```js
retornar (
<div tabIndex={1}>
<button onClick={myFunction}>clique em mim</button>
<label htmlFor='name'>Nome</label>
<input readOnly={true} id='nome' />
</div>
)
// em html
<div tabindex="1">
<button onclick="myFunction()">clique em mim</button>
<label for='name'>Nome</label>
<input readonly id='nome' />
</div>
```

- className em vez de classe

```js
return <div className="someValue">olá</div>;
```

- feche todos os elementos

```js
voltar <img />
// ou
return <entrada />
```

- formatação
- tag de abertura na mesma linha que return ou ()

```js
função Saudação() {
retornar (
<>
<div className="someValue">
<h3>olá pessoal</h3>
<ul>
<li>
<a href="#">olá mundo</a>
</li>
</ul>
</div>
<h2>olá mundo</h2>
<input type="text" name="" id="" />
</>
)
}
```

#### Componentes do ninho

```js
função Saudação() {
retornar (
<div>
<Pessoa />
<Mensagem />
</div>
)
}

const Pessoa = () => <h2>joão doe</h2>
const Mensagem = () => {
return <p>esta é minha mensagem</p>
}
```

#### Ferramentas do Desenvolvedor React

- canto superior direito
- mais ferramentas/extensões
- abra a loja virtual do Chrome

#### Lista de livros

- estrutura de configuração

```js
importar Reagir de 'reagir'
importar ReactDOM de 'react-dom/client'

function ListaLivro() {
retornar (
<seção>
<Livro />
<Livro />
<Livro />
<Livro />
</section>
)
}

const Livro = () => {
retornar (
<artigo>
<Imagem />
<Título />
<Autor />
</artigo>
)
}

const Image = () => <h2>espaço reservado para imagem</h2>
const Título = () => {
return <h2>Título do livro</h2>
}
const Autor = () => <h4>Autor</h4>

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<BookList />)
```

- no tipo de mecanismo de pesquisa - 'livros mais vendidos da amazon'
  [Amazon Best Sellers](https://www.amazon.com/Best-Sellers-Books/zgbs/books/)
- NÃO PRECISA COMPRAR NADA!!!
- NÃO É UM LINK DE AFILIADO!!!!
- escolha um livro
- copiar imagem, título e autor

```js
importar Reagir de 'reagir'
importar ReactDOM de 'react-dom/client'

function ListaLivro() {
retornar (
<seção>
<Livro />
<Livro />
<Livro />
<Livro />
</section>
)
}

const Livro = () => {
retornar (
<article className="livro">
<Imagem />
<Título />
<Autor />
</artigo>
)
}

const Imagem = () => (
<img
src="https://images-na.ssl-images-amazon.com/images/I/71m+Qtq+HrL._AC_UL900_SR900,600_.jpg"
alt="Fatos interessantes para mentes curiosas"
/>
)
const Título = () => {
voltar <h2>Fatos interessantes para mentes curiosas</h2>
}
const Autor = () => <h4>Jordan Moore </h4>

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<BookList />)
```

####CSS

- criar index.css em src

```css
* {
margem: 0;
preenchimento: 0;
box-sizing: border-box;
}

corpo {
font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
plano de fundo: #f1f5f8;
cor: #222;
}
```

- importar arquivo e adicionar classes

```js
importar './index.css'

function ListaLivro() {
retornar (
<section className="lista de livros">
<Livro />
<Livro />
<Livro />
<Livro />
</section>
)
}

const Livro = () => {
retornar (
<article className="livro">
<Imagem />
<Título />
<Autor />
</artigo>
)
}
```

- CSS completo

```css
.lista de livros {
largura: 90vw;
largura máxima: 1170px;
margem: 5rem automático;
exibição: grade;
lacuna: 2rem;
}

@tela de mídia e (largura mínima: 768px) {
.lista de livros {
grid-template-columns: repeat(3, 1fr);
}
}
.livro {
plano de fundo: #fff;
raio da borda: 1rem;
enchimento: 2rem;
alinhamento de texto: centro;
}
.book img {
largura: 100%;
ajuste do objeto: capa;
}
.livro h2 {
margem superior: 1rem;
tamanho da fonte: 1rem;
}
```

#### Imagens Locais (Pasta Pública)

- Vídeo opcional !!!

- imagens externas (hospedadas em servidores diferentes) - só precisam de um url
- imagens locais (pasta pública) - menos desempenho
- imagens locais (pasta src) - melhor solução para ativos,
  já que sob o capô eles são otimizados.

- salvar imagem (Salvar imagem como ....)
- criar pasta de imagens em público
- copiar/colar imagem
- renomear (opcional)
- substitua url no src - './images/imageName.extension'
- './' porque os recursos estão no mesmo servidor

```js
const Imagem = () => (
  <img
    src="./images/book-1.jpg"
    alt="Fatos interessantes para mentes curiosas"
  />
);
```

- quaisquer ativos que colocamos em público - disponíveis instantaneamente
- domínio(localhost)/asset

#### JSX - CSS (estilos embutidos)

- acessório de estilo
- {} em JSX significa voltar para JS Land
- value é um objeto com pares chave/valor - em maiúsculas e com ''

```js
const Autor = () => (
  <h4 style={{ color: "#617d98", fontSize: "0.75rem", marginTop: "0.5rem" }}>
    Jordan Moore
  </h4>
);
```

- regras css ainda se aplicam (inline vs css externo)

```css
.livro h4 {
/* não vai funcionar */
cor vermelha;
/* vai funcionar */
espaçamento entre letras: 2px;
}
```

- bibliotecas externas usam CSS inline,
  então, se você quiser fazer algumas alterações,
  consulte a guia de documentos e elementos da biblioteca

- opção alternativa

```js
const Autor = () => {
const inlineHeadingStyles = {
cor: '#617d98',
tamanho da fonte: '0.75rem',
marginTop: '0.5rem',
}
retornar <h4 style={inlineHeadingStyles}>Jordan Moore </h4>
}
```

- NA MAIOR PARTE, MÚLTIPLAS ABORDAGENS DISPONÍVEIS !!!
- DESDE QUE O RESULTADO SEJA O MESMO, REALMENTE SE RESTA A PREFERÊNCIA!!!!

#### JSX - Javascript

- refatorar para um único componente de livro (preferência pessoal)
- remover css embutido

```js
const Livro = () => {
retornar (
<article className="livro">
<img
src="./images/book-1.jpg"
alt="Fatos interessantes para mentes curiosas"
/>
<h2>Fatos interessantes para mentes curiosas</h2>
<h4>Jordan Moore</h4>
</artigo>
)
}
```

```css
.livro h4 {
cor: #617d98;
tamanho da fonte: 0,75 rem;
margem superior: 0,5rem;
espaçamento entre letras: 2px;
}
```

- {} em JSX significa voltar para JS Land
- o valor dentro deve ser uma expressão (valor de retorno),
  não pode ser uma declaração

```js
autor const = 'Jordan Moore'
const Livro = () => {
const title = 'Fatos interessantes para mentes curiosasssssss'
retornar (
<article className="livro">
<img
src="./images/book-1.jpg"
alt="Fatos interessantes para mentes curiosas"
/>
<h2>{title}</h2>

<h4>{autor.toUpperCase()} </h4>
{/* <p>{let x = 6}</p> */}
<p>{6 + 6}</p>
</artigo>
)
}
```

- alternar comentário de linha Editar/Alternar comentário de linha

#### Adereços - Configuração inicial

- refatorar/limpar

```js
autor const = 'Jordan Moore'
const title = 'Fatos interessantes para mentes curiosas'
const img = './imagens/livro-1.jpg'

function ListaLivro() {
retornar (
<section className="lista de livros">
<Livro />
<Livro />
</section>
)
}
const Livro = () => {
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
</artigo>
)
}
```

```js
// parâmetros
const someFunc = (param1, param2) => {
  console.log(param1, param2);
};
// argumentos
someFunc("trabalho", "desenvolvedor");
```

```js
const Livro = (props) => {
console.log(props)
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
{console.log(props)}
</artigo>
)
}
```

- props object, convenção para chamar props, 'shakeAndBake' é uma excelente alternativa

- passar como pares chave/valor
- se o prop existir, ele retornará valor, caso contrário, nenhum valor

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
<Livro de trabalho="desenvolvedor" />
<Título do livro="título aleatório" número={22} />
</section>
)
}
const Livro = (props) => {
console.log(props)
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
<p>{props.job}</p>
<p>{props.title}</p>
<p>{props.number}</p>
</artigo>
)
}
```

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
<Autor do livro={autor} título={título} img={img} />
<Título do livro={title} img={img} />
</section>
)
}
const Livro = (props) => {
console.log(props)
retornar (
<article className="livro">
<img src={props.img} alt={props.title} />
<h2>{props.title}</h2>
<h4>{props.autor} </h4>
</artigo>
)
}
```

#### Adereços - configuração um tanto dinâmica

- configurar um objeto
- refatorar vars para propriedades
- copiar/colar e renomear
- obter valores para o segundo livro
- adereços de configuração

```js
const primeiroLivro = {
autor: 'Jordan Moore',
título: 'Fatos interessantes para mentes curiosas',
img: './images/livro-1.jpg',
}
const segundoLivro = {
autor: 'James Clear',
título: 'Hábitos atômicos',
img: 'https://images-na.ssl-images-amazon.com/images/I/81wgcld4wxL._AC_UL900_SR900,600_.jpg',
}

function ListaLivro() {
retornar (
<section className="lista de livros">
<Livro
autor={primeiroLivro.autor}
título={firstBook.title}
img={firstBook.img}
/>
<Livro
autor={segundoLivro.autor}
título={segundoLivro.título}
img={secondBook.img}
/>
</section>
)
}
const Livro = (props) => {
console.log(props)
retornar (
<article className="livro">
<img src={props.img} alt={props.title} />
<h2>{props.title}</h2>
<h4>{props.autor} </h4>
</artigo>
)
}
```

#### Access Props - Múltiplas Abordagens

- não existe certo ou errado - novamente preferência!!!

- Desestruturação (objeto)
  [JS Nuggets - Destruindo (objeto)](https://www.youtube.com/watch?v=i4vhNKihfto&list=PLnHJACx3NwAfRUcuKaYhZ6T5NRIpzgNGJ&index=8&t=1s)

- desestruturação em Vanilla JS
- economiza tempo/digitação
- retire as propriedades
- não precisa mais referenciar o objeto

```js
const algumObjeto = {
  nome: "joão",
  trabalho: "desenvolvedor",
  localização: "florida",
};

console.log(someObject.name);
const { nome, trabalho } = someObject;
console.log(trabalho);
```

- não há necessidade de todos os props.propName
- desestruturar dentro do componente

```js
const Livro = (props) => {
const { img, titulo, autor } = props
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
</artigo>
)
}
```

- desestruturar em parâmetros de função (no nosso caso props)
- se você tiver console.log(props) - não será definido

```js
const Livro = ({ img, titulo, autor }) => {
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
</artigo>
)
}
```

#### Acessórios para crianças

- tudo o que renderizamos entre tags de componentes
- durante o curso, usaremos principalmente a API de contexto
- adereço especial, tem que ser "crianças"
- pode colocar em qualquer lugar no JSX

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
<Livro
autor={primeiroLivro.autor}
título={firstBook.title}
img={firstBook.img}
>
<p>
Lorem ipsum dolor, sit amet consectetur adipisicing elit. itaque
repudiandae inventore eos qui animi sed iusto alias eius e sapiente.
</p>
<button>clique em mim</button>
</Livro>
<Livro
autor={segundoLivro.autor}
título={segundoLivro.título}
img={secondBook.img}
/>
</section>
)
}

const Livro = ({ img, titulo, autor, filhos }) => {
// resto da logica
}
const Livro = (props) => {
const { img, título, autor, filhos } = adereços
console.log(props)
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
{crianças}
</artigo>
)
}
```

- opcional

```css
@tela de mídia e (largura mínima: 768px) {
.lista de livros {
grid-template-columns: repeat(3, 1fr);
itens de alinhamento: início;
}
}
.livro p {
margem: 1rem 0 0,5rem;
}
```

#### Lista Simples

- [Javascript Nuggets - Mapa](https://www.youtube.com/watch?v=80KX6aD9R7M&list=PLnHJACx3NwAfRUcuKaYhZ6T5NRIpzgNGJ&index=1)

- refatorar

```js
const livros = [
{
autor: 'Jordan Moore',
título: 'Fatos interessantes para mentes curiosas',
img: './images/livro-1.jpg',
},
{
autor: 'James Clear',
título: 'Hábitos atômicos',
img: 'https://images-na.ssl-images-amazon.com/images/I/81wgcld4wxL._AC_UL900_SR900,600_.jpg',
},
]

function ListaLivro() {
return <section className="booklist"></section>
}

const Livro = (props) => {
const { img, titulo, autor } = props

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
</artigo>
)
}
```

- não pode renderizar objetos no React

```js
function ListaLivro() {
  return <section className="booklist">{books}</section>;
}
```

- map - cria um novo array chamando uma função para cada elemento do array.

```js
const nomes = ['joão', 'peter', 'susana']
const novosNomes = nomes.map((nome) => {
console.log(nome)
retornar <h1>{nome}</h1>
})

function ListaLivro() {
return <section className="booklist">{newNames}</section>
}
```

#### Lista adequada

- remover nomes e newNames

```js
function ListaLivro() {
  retornar(
    <section className="lista de livros">
      {livros.map((livro) => {
        console.log(livro);

        // retorna 'olá';
        retornar(
          <div>
            <h2>{book.title}</h2>
          </div>
        );
      })}
    </section>
  );
}
```

- componente de renderização
- passar as propriedades uma a uma

```js
function ListaLivro() {
  retornar(
    <section className="lista de livros">
      {livros.map((livro) => {
        console.log(livro);
        const { img, titulo, autor } = livro;
        return <Livro img={img} título={título} autor={autor} />;
      })}
    </section>
  );
}
```

#### Suporte de chave

- normalmente será id

```js
const livros = [
  {
    autor: "Jordan Moore",
    título: "Fatos interessantes para mentes curiosas",
    img: "./images/livro-1.jpg",
    identificação: 1,
  },
  {
    autor: "James Clear",
    título: "Hábitos atômicos",
    img: "https://images-na.ssl-images-amazon.com/images/I/81wgcld4wxL._AC_UL900_SR900,600_.jpg",
    identificação: 2,
  },
];

function ListaLivro() {
  retornar(
    <section className="lista de livros">
      {livros.map((livro) => {
        console.log(livro);
        const { img, titulo, autor, id } = livro;
        return <Livro livro={livro} key={id} />;
      })}
    </section>
  );
}
```

- você verá o índice, mas não é aconselhável se a lista estiver mudando

```js
function ListaLivro() {
  retornar(
    <section className="lista de livros">
      {livros.map((livro, índice) => {
        console.log(livro);
        const { img, titulo, autor, id } = livro;
        return <Livro livro={livro} chave={índice} />;
      })}
    </section>
  );
}
```

#### Passe todo o objeto

- componente de renderização
- passar objeto inteiro
- Desestruturação (objeto)
  [JS Nuggets - Destruindo (objeto)](https://www.youtube.com/watch?v=i4vhNKihfto&list=PLnHJACx3NwAfRUcuKaYhZ6T5NRIpzgNGJ&index=8&t=1s)

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
{livros.map((livro) => {
console.log(livro)
const { img, titulo, autor } = livro
return <Livro livro={livro} />
})}
</section>
)
}

const Livro = (props) => {
const { img, título, autor } = props.livro

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
</artigo>
)
}
```

- alternativa

```js
const Livro = ({ livro: { img, titulo, autor } }) => {
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
</artigo>
)
}
```

#### Minha preferência pessoal

- utilizar o operador spread (...) - copiar valores
- Operador de spread
- [JS Nuggets - Spread Operator](https://www.youtube.com/watch?v=4Zyr5a3m0Fc&list=PLnHJACx3NwAfRUcuKaYhZ6T5NRIpzgNGJ&index=10)

```js
const amigos = ["joão", "peter", "ana"];
const novosAmigos = [...amigos, "susan"];
console.log(amigos);
console.log(newFriends);
const algumObjeto = {
  nome: "joão",
  trabalho: "desenvolvedor",
};
// COPIE NÃO UMA REFERÊNCIA!!!!
const newObject = { ...someObject, localização: "florida" };
console.log(someObject);
console.log(newObject);
```

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
{livros.map((livro) => {
return <Book {...book} key={book.id} />
})}
</section>
)
}

const Livro = (props) => {
const { img, titulo, autor } = props
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<h4>{autor} </h4>
</artigo>
)
}
const Livro = ({ img, titulo, autor }) => {
// restante do código
}
```

#### Eventos - Fundamentos

- Baunilha JS

```js
const btn = document.getElementById('btn')

btn.addEventListener('clique', função (e) {
// acessa o objeto de evento
// faz alguma coisa quando o evento dispara
})
```

- abordagem semelhante
- elemento, evento, função
- novamente camelCase

```js
const EventExamples = () => {
const handleButtonClick = () => {
alert('lidar com o clique do botão')
}
retornar (
<seção>
<button onClick={handleButtonClick}>clique em mim</button>
</section>
)
}
```

- [React Events](https://reactjs.org/docs/events.html)
- não há necessidade de memorizá-los (a ideia é a mesma)
- mais comum
- onClick (eventos de clique)
- onSubmit (enviar formulário)
- onChange (mudança de entrada)

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
<EventExamples />
{livros.map((livro) => {
return <Book {...book} key={book.id} />
})}
</section>
)
}

const EventExamples = () => {
const handleFormInput = () => {
console.log('manipular entrada de formulário')
}
const handleButtonClick = () => {
alert('lidar com o clique do botão')
}
retornar (
<seção>
<forma>
<h2>Forma Típica</h2>
<entrada
digite="texto"
nome="exemplo"
onChange={handleFormInput}
estilo={{ margem: '1rem 0' }}
/>
</form>
<button onClick={handleButtonClick}>clique em mim</button>
</section>
)
}
```

#### Objeto de evento e envio de formulário

```js
const EventExamples = () => {
const handleFormInput = (e) => {
console.log(e)
// e.target - elemento
console.log(`Nome de entrada: ${e.target.name}`)
console.log(`Valor de entrada: ${e.target.value}`)
// console.log('manipular entrada de formulário');
}
const handleButtonClick = () => {
alert('lidar com o clique do botão')
}
const handleFormSubmission = (e) => {
e.preventDefault()
console.log('formulário enviado')
}
retornar (
<seção>
{/* add onSubmit Event Handler */}
<form onSubmit={handleFormSubmission}>
<h2>Forma Típica</h2>
<entrada
digite="texto"
nome="exemplo"
onChange={handleFormInput}
estilo={{ margem: '1rem 0' }}
/>
{/* adicionar botão com type='enviar' */}
<button type="submit">enviar formulário</button>
</form>
<button onClick={handleButtonClick}>clique em mim</button>
</section>
)
}
```

- Abordagem alternativa

```js
<button type="submit" onClick={handleFormSubmission}>
  Enviar formulário
</button>
```

#### Granada Mental

- Abordagem alternativa
- passar função anônima (neste caso, função de seta)
- um forro - menos código

```js
const EventExamples = () => {
retornar (
<seção>
<button onClick={() => console.log('olá')}>clique em mim</button>
</section>
)
}
```

- também pode acessar o objeto de evento

```js
const EventExamples = () => {
retornar (
<seção>
<forma>
<h2>Forma Típica</h2>
<entrada
digite="texto"
nome="exemplo"
onChange={(e) => console.log(e.target.value)}
estilo={{ margem: '1rem 0' }}
/>
</form>
<button onClick={() => console.log('você clicou em mim')}>clique em mim</button>
</section>
)
}
```

#### Granada Mental #2

- remover exemplos de eventos
- os componentes são independentes por padrão

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
{livros.map((livro) => {
return <Book {...book} key={book.id} />
})}
</section>
)
}

const Livro = (props) => {
const { img, titulo, autor } = props
const displayTitle = () => {
console.log(título)
}

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<button onClick={displayTitle}>exibir título</button>
<h4>{autor} </h4>
</artigo>
)
}
```

- botão remover

#### Perfuração Prop

- reage ao fluxo de dados - só pode passar props para baixo
- alternativas Context API, redux, outras bibliotecas de estado

```js
function ListaLivro() {
const someValue = 'shakeAndBake'
const displayValue = () => {
console.log(someValue)
}
retornar (
<section className="lista de livros">
{livros.map((livro) => {
return <Book {...book} key={book.id} displayValue={displayValue} />
})}
</section>
)
}

const Livro = (props) => {
const { img, título, autor, displayValue } = props

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<button onClick={displayValue}>clique em mim</button>
<h4>{autor} </h4>
</artigo>
)
}
```

#### Exemplo Mais Complexo

- configuração inicial
- criar a função getBook na lista de livros
- aceita id como argumento e encontra o livro
- [Javascript Nuggets - Filtre e encontre](https://www.youtube.com/watch?v=KeYxsev737s&list=PLnHJACx3NwAfRUcuKaYhZ6T5NRIpzgNGJ&index=4)
- passe a função para Book Component e chame no clique do botão
- no livro Componente desestrutura id e função
- invocar a função quando o usuário clicar no botão, passar o id
- o objetivo: você deve ver o mesmo livro no console

```js
const BookList = () => {
const getBook = (id) => {
const livro = livros.find((livro) => livro.id === id)
console.log(livro)
}

retornar (
<section className="lista de livros">
{livros.map((livro) => {
return <Book {...book} key={book.id} getBook={getBook} />
})}
</section>
)
}

const Livro = (props) => {
const { img, título, autor, getBook, id } = props
// console.log(props);

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
{/* isto não vai funcionar */}
<button onClick={getBook(id)}>exibir título</button>
<h4>{autor}</h4>
</artigo>
)
}
```

- duas correções
- primeira opção - wrapper de configuração

```js
const Livro = (props) => {
const { img, título, autor, getBook, id } = props
// console.log(props);
const getSingleBook = () => {
getBook(id)
}
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>
<button onClick={getSingleBook}>exibir título</button>
<h4>{autor}</h4>
</artigo>
)
}
```

- duas correções
- segunda opção - envolva a função de seta anônima

```js
const Livro = (props) => {
const { img, título, autor, getBook, id } = props
// console.log(props);
const getSingleBook = () => {
getBook(id)
}
retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>

<button onClick={() => getBook(id)}>exibir título</button>
<h4>{autor}</h4>
</artigo>
)
}
```

#### Declarações de Importação e Exportação

- remova todo o código getBook

```js
function ListaLivro() {
retornar (
<section className="lista de livros">
{livros.map((livro) => {
return <Book {...book} key={book.id} />
})}
</section>
)
}

const Livro = (props) => {
const { img, titulo, autor } = props

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>

<h4>{autor} </h4>
</artigo>
)
}
```

- configurar dois arquivos em src books.js e Book.js
- corte a matriz de livros de index.js
- adicionar a books.js

livros.js

```js
const livros = [
  {
    autor: "Jordan Moore",
    título: "Fatos interessantes para mentes curiosas",
    img: "./images/livro-1.jpg",
    identificação: 1,
  },
  {
    autor: "James Clear",
    título: "Hábitos atômicos",
    img: "https://images-na.ssl-images-amazon.com/images/I/81wgcld4wxL._AC_UL900_SR900,600_.jpg",
    identificação: 2,
  },
];
```

- dois sabores nomeados e exportações padrão

- com nomes de exportação nomeados DEVEM corresponder
- com exportações padrão, pode renomear, mas apenas um por arquivo

- exportação nomeada

```js
exportar livros const = [
{
autor: 'Jordan Moore',
título: 'Fatos interessantes para mentes curiosas',
img: './images/livro-1.jpg',
identificação: 1,
},
{
autor: 'James Clear',
título: 'Hábitos atômicos',
img: 'https://images-na.ssl-images-amazon.com/images/I/81wgcld4wxL._AC_UL900_SR900,600_.jpg',
identificação: 2,
},
]
```

index.js

```js
importar { livros } de './livros'
```

- exportação padrão

```js
const Livro = (props) => {
const { img, titulo, autor } = props

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>

<h4>{autor} </h4>
</artigo>
)
}

exportar livro padrão
```

index.js

```js
importar Livro de './Livro'
```

#### Imagens Locais (pasta src)

- melhor desempenho porque otimizado
- adicione mais um livro à matriz
- baixar todas as três imagens (renomear)
- pasta de imagens de configuração no src
- importar todas as três imagens no books.js
- definir propriedade de imagem igual a importar
- e sim cada imagem requer nova importação

```js
importar img1 de './images/book-1.jpg'
importar img2 de './images/book-2.jpg'
importar img3 de './images/book-3.jpg'

exportar livros const = [
{
autor: 'Jordan Moore',
título: 'Fatos interessantes para mentes curiosas',
img: img1,
identificação: 1,
},
{
autor: 'James Clear',
título: 'Hábitos atômicos',
img: img2,
identificação: 2,
},
{
autor: 'Stephen King',
título: 'Conto de Fadas',
img: img3,
identificação: 3,
},
]
```

#### Desafios

- números de configuração
- não se preocupe com css
- dica - índice (segundo parâmetro no mapa)

index.js

```js
const BookList = () => {
retornar (
<section className="lista de livros">
{livros.map((livro, índice) => {
return <Book {...book} key={book.id} number={index} />
})}
</section>
)
}

const Livro = (props) => {
const { img, título, autor, número } = props

retornar (
<article className="livro">
<img src={img} alt={title} />
<h2>{title}</h2>

<h4>{autor}</h4>
<span className="number">{`# ${number + 1}`}</span>
</artigo>
)
}
```

index.css

```css
.livro {
plano de fundo: #fff;
raio da borda: 1rem;
preenchimento: 2rem;
alinhamento de texto: centro;
/* definir relativo */
posição: relativa;
}

.número {
posição: absoluta;
superior: 0;
esquerda: 0;
tamanho da fonte: 1rem;
preenchimento: 0,75rem;
borda-superior-esquerda-raio: 1rem;
borda-inferior-direita-radius: 1rem;
plano de fundo: #c35600;
cor: #fff;
}
```

#### Adicionar Título

- adicione um título ao nosso aplicativo (css opcional)
- mudar o título da página

index.js

```js
function ListaLivro() {
  retornar(
    <>
      <h1>best-sellers da amazon</h1>
      <section className="lista de livros">
        {livros.map((livro) => {
          return <Book {...book} key={book.id} />;
        })}
      </section>
    </>
  );
}
```

index.css

```css
h1 {
alinhamento de texto: centro;
margem superior: 4rem;
transformação de texto: capitalizar;
}
```

public/index.html

```html
<title>Mais vendidos</title>
```

#### Criar aplicativo de produção

- pare o servidor dev "ctrl + c"
- execute "npm run build"
- a pasta de compilação é criada

#### Netlify

- inscrever-se
- adicionar novo site/implantar manualmente
- escolha a pasta de compilação
- renomear site - configurações do site/alterar nome do site

#### Create-React-App Boilerplate (src)

- index.js

```js
importar Reagir de 'reagir'
importar ReactDOM de 'react-dom/client'

// estilos (tipicamente globais)
importar './index.css'

// convenção para nomeá-lo App e configurar em um arquivo separado
importar aplicativo de './App'
// importa relatório de sinais vitais da web
importar reportWebVitals de './reportWebVitals'

// Modo estrito

// StrictMode é uma ferramenta para destacar possíveis problemas em um aplicativo. Ativa verificações e avisos adicionais para seus descendentes. Executa apenas no desenvolvimento, não afeta a compilação de produção. RENDE DUAS VEZES!!! Possível remover.

const root = ReactDOM.createRoot(document.getElementById('root'))
root.render(
<React.StrictMode>
<Aplicativo />
</React.StrictMode>
)

// Se você deseja começar a medir o desempenho em seu aplicativo, passe uma função
// para registrar os resultados (por exemplo: reportWebVitals(console.log))
// ou envie para um endpoint analítico. Saiba mais: https://bit.ly/CRA-vitals
reportWebVitals()
```

- remover em src

- setupTests.js
- reportWebVitals.js
- App.test.js

- tenha cuidado com vários arquivos css

App.js

```js
função Aplicativo() {
return <h1>aplicativo backroads</h1>
}

exportar aplicativo padrão
```

- remover
- remover logo.svg
- App.css

#### Vite Docs

(Vite)[https://vitejs.dev/]

#### Vite Install

```sh
npm create vite@latest app-name -- --template react
npm instalar
npm run dev
```

-http://localhost:5173/

#### Vite Setup

- precisa usar a extensão .jsx
- index.html na fonte em vez de public
- ativos ainda em público
- em vez de index.js, precisa usar main.jsx
- para ativar o servidor dev - "npm run dev"

- resto o mesmo - importações/exportações, implantação, ativos, etc...
