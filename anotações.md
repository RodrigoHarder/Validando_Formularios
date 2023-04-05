**type dos inputs** 

* button: define um botão clicável
* number:define um campo para número inteiro
* text: define um campo para texto que permite também números e caracteres especiais
* date: define um campo para data
* checkbox: define uma caixa de seleção para múltiplas opções
* radio: define uma caixa de seleção para opção única
* password:define um campo de senha
* submit: define um botão para enviar os dados
* tel: define um campo para telefone

**minlength** = número mínimo de caracteres que podem ser inseridos em um campo de preenchimento;
**maxlength** = número máximo de caracteres que podem ser inseridos em um campo de preenchimento;

**required**: torna o campo obrigatório;

**pattern**: utiliza expressões regulares (regex) criando um formato a se seguir e o que deve ser aceito pelo nosso formulário.

`\d{3}\`: encontra correspondência com um número(equivalente a [0-9]) por 3 vezes.
`.?`: seguido por um ponto opcional.
`-?`: seguido por um hífen opcional.
`\d{2}`: encontra um número duas vezes.

`export default`: exportada como padrão;
`replace`: substitui um valor, recebe 2 parâmetros, sendo o primeiro o que queremos substituir e o segundo pelo que queremos substituir;

Como criar validações para CPF e pessoas menores de idade;

`nem Date`: vai receber o campo de data e converter o valor para uma forma que o JS entenda;

**ValidityState:** lista de possíveis erros de validaçoes que ocorrem automaticamente ao interagir com um formulário;

Tipos mais comuns ao preencher um formulário: 

* `valueMissing`: indica que não há nada no campo de preenchimento;
* `typeMismatch`: o tipo do elemento não combina com o dado que está sendo inserido;
* `patternMismatch`:  o padrão inserido no pattern não está sendo atendido e portanto não será aceito;
* `tooShort`: os dados não atingem o tamanho mínimo de caracteres definidos pelo minlength;
* `customerror`: erros customizados, por exemplo as lógicas feitas em JS;

`checkValidity`: vai verificar se o campo está válido ou não;

**localStorage:** permite salvar pares de chave/valor no navegador sem data de expiração, ou seja, os dados não são excluídos quando o navegador é fechado e ficam disponíveis para navegação futura. 

* Iniciar câmetra do usuário no navegador por meio do comando `await navigator.mediaDevices.getUserMedia({video:true, audio:false});`. Utilizando parâmetros async/await para lidar com funções assíncronas;

* Como capturar a fotografia por meio do comando: `canvas.getContext('2d').drawImage(video, 0, 0, canvas.width, canvas.height)`

* Inserir novos dados no localStorage, atualizando os dados já existentes:
```
const receberDadosExistentes = localStorage.getItem("cadastro");
const converteRetorno = JSON.parse(receberDadosExistentes);
converteRetorno.imagem = imagemURL;
localStorage.setItem('cadastro', JSON.stringify(converteRetorno))
```

