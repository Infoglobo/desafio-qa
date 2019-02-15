# Quer trabalhar em nosso time de QA? 

Queremos analisar suas habilidades para criar cenários de testes e codificar os testes funcionais automatizados.
A maioria dos nossos produtos demanda testes focados no comportamento e no visual da aplicação (não em CRUD).

# O desafio
Nosso desafio consiste de três exercícios:
## 1. Mapear cenários e automatização de testes web
Queremos que você acesse a página "últimas notícias" do site do Globo emulando um dispositivo móvel (através do DevTools do seu navegador), mapeie e automatize as principais funcionalidades dessa página. Se atente mais nas funcionalidades principais da página.

Esse é o endereço da página que estamos falando: https://m.oglobo.globo.com/ultimas-noticias

Alguns exemplos das funcionalidades da página:
* A página possui dois "combo box", um para escolher o tipo da editoria e outro para escolher o tipo do conteúdo;
* Selecionando alguma opção nos "combo box" descritos, as matérias exibidas na lista devem pertencer a editoria selecionada;

Como dito, são só exemplos. Cabe a você mapear e automatizar as funcionalidades que julga importante para essa página. 

### Pontos obrigatórios
- Utilizar o Selenium como ferramenta de automatização;
- Utilizar o formato Gherkin para a criação dos cenários (BDD, Cucumber);
- Durante a execução do teste automatizado, o navegador também deve ser executado de forma que emule um dispositivo móvel;
- O teste deve ser executado no Google Chrome;
- Utilizar Java como linguagem de programação;
- Evitar o uso de XPath para identificação dos objetos da página;
- Ter um README no repositório com as instruções relevantes sobre o desafio. Por exemplo: como importar o projeto na IDE, como executar o projeto, ect.;

### Pontos adicionais (não são obrigatórios, mas podem ajudar na sua avaliação):
- Um vídeo da execução do teste (o script do teste não precisa gravar a execução, pode ser feita manualmente);
- O script do teste gerando screenshots no caso de falhas;
- Prezamos muito pela organização do código, então se atente a padrões e boas práticas adquiridos;
- Utilização de uma ferramenta de gerenciamento do projeto (ex: Maven, Gradle, etc);
- Não deixar as informações do teste "hard coded";
- Utilização de uma ferramenta de conteinerização;
- Manter o repositório "limpo" e organizado;

## 2. Automatização de testes em end-point
Queremos que, de forma automatizada, você faça uma requisição GET (sem header ou nenhum outro parâmetro) no endereço `assineglobo.com.br/services/rest/products` e verifique que o documento encontrado contém:
- Uma lista que possui outros documentos;
- Que os documentos na lista retornada contem o campo `id` e, cada documento possui um desses valores: `AT`, `CJ`, `CV`, `CF`, `EP`, `EN`, `GC`, `GL`, `GR`, `GQ`, `MC`, `PE`, `VG`;

### Pontos obrigatórios
- Utilizar uma lib que permita fazer requisições e validar resposta (ex: [Rest Assured)](http://rest-assured.io/);
- Utilizar Java como linguagem de programação;
- Ter um README no repositório com as instruções relevantes sobre o desafio. Por exemplo: como importar o projeto na IDE, como executar o projeto, ect.;

### Pontos adicionais
- Prezamos muito pela organização do código, então se atente a padrões e boas práticas adquiridos;
- Utilização de uma ferramenta de gerenciamento do projeto (ex: Maven, Gradle, etc);
- Não deixar as informações do teste "hard coded";
- Utilização de uma ferramenta de conteinerização;
- Manter o repositório "limpo" e organizado;

## 3. Apontar cenários em um teste unitário
Queremos que, a partir do código fonte da aplicação, você mapeie os testes unitários que julga relevante. Só é necessário mapear, não é necessário implementar nenhum teste.
Se atente apenas nos testes para o método `calc`, os outros métodos (`__add`, `__sub`, etc.) foram adicionados só para a compreensão do código como um todo.

Código fonte (em Javascript):
```
class  MathHelper {

	calc(operation, n1, n2) {

			switch (operation) {
				case 'addition':
					return this.__add(n1, n2);
				case 'subtraction':
					return this.__sub(n1, n2);
				case 'multiplication':
					return this.__mult(n1, n2);
				case 'division':
					return this.__div(n1, n2);
				default:
					return undefined;
			}
	}

	__add(n1, n2) {
		return n1 + n2;
	}

	__sub(n1, n2) {
		return n1 - n2;
	}

	__mult(n1, n2) {
		return n1 * n2;
	}

	__div(n1, n2) {
		return n1 / n2;
	}
}
```

Exemplos de teste unitário que pode ser feito:
- Chamando o método `calc`, com os parâmetros `("addition", 1, 1`), o método `__add` deve ser chamado com os valores (`1, 1`);
- Chamando o método `calc`, com os parâmetros `("addition", 1, 1`), o retorno deve ser `2`.

### Pontos obrigatórios
- É necessário descrever os cenários no formato a cima (ou similar), especificando parâmetros, resultado esperado e métodos que devem ser chamados;
- Entregar um arquivo de texto (txt, pdf, etc.);
- Descrever no README do repositório onde esses testes estão mapeados;

# Como entregar
 Você deve disponibilizar seu código em algum serviço de hospedagem como Bitbucket, Gitlab ou Github e manter o repositório como privado.

Assim que finalizar, nos avise para enviarmos os usuários que devem ter acesso para avaliação.

Bom desafio!

# Sobre nós

## Medium
Para conhecer um pouco sobre os nossos desafios nos acompanhe no Medium:

https://medium.com/editora-globo

## Infoglobo
A Infoglobo através de seus produtos - os jornais O Globo, Extra e Expresso, com os sites Globo e Extra e a Agência O Globo - tem o dever de apurar o fato, oferecendo aos seus leitores a informação mais completa, sempre com a preocupação de adequar a linguagem ao público a que se destina. Além de esclarecer o que acontece de mais importante no Brasil e no mundo, os produtos da Infoglobo também são uma ferramenta de acesso ao melhor do entretenimento e da cultura. A Infoglobo tem muito orgulho desse papel e trabalha com o compromisso de levar jornalismo sério e isento à população.

## Editora Globo
Desde 1952, a Editora Globo dissemina conhecimento entre os leitores e produz um jornalismo independente que antecipa as transformações da sociedade. Moderna, dinâmica e inovadora, a empresa conecta consumidores a conteúdos que transformam suas vidas e oferecem a eles a liberdade de escolherem em qual plataforma preferem ler. Com mais de 16 revistas no portfólio - incluindo as marcas Vogue, Casa Vogue, GQ e Glamour, após joint-venture estabelecida com a Condé Nast - a Editora Globo e Edições Globo Condé Nast têm 3,4 milhões de cópias por mês, 9,2 milhões de leitores, 18 websites, 11,4 milhões de visitantes únicos por mês, 40 eventos anuais, 25 aplicativos para iPhone, iPad e Android e mais de 1 milhão de downloads. Ainda, contamos com a marca Globo Livros, que tem mais de mil títulos no catálogo de livros, de autores nacionais e internacionais, publicados em menos de dois anos. No digital, a marca conta com 200 títulos e parcerias com os principais players do mercado, como Apple, Kobo Cultura, Google, Saraiva and Amazon.
