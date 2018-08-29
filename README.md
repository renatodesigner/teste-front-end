# Teste iCasei: Front-End
Desenvolver uma aplicação HTML5.

Teste commit

## Instruções
- Faça um fork desse projeto para a sua conta pessoal do GitHub, ou BitBucket.
- Siga as especificações abaixo.
- Crie um README com as instruções para compilar, testar e rodar o projeto.
- O link do repositório deverá ser enviado para o e-mail frontend@icasei.com.br com o título **Teste FrontEnd**

## Especificações tecnicas
- Utilizar diretrizes do [Google Material Design](https://www.google.com/design/spec/material-design/introduction.html)
- Utilizar a [API de busca do YouTube](https://developers.google.com/youtube/v3/docs/search/list)
- Mobile first e responsivo
- Usar framework JS (React, Angular ou frameworks relacionados)
- Cores livres, layout livre, imagens livres
- Gitflow
- Testes automatizados

## Especificações funcionais
### Tela Inicial
Essa tela terá um formulário de busca posicionado no meio da tela com campo de texto com placeholder "Pesquisar" e um botão "Buscar". Esse formulário deverá ter validação.

Essa busca deverá chamar a url https://www.googleapis.com/youtube/v3/search?part=id,snippet&q={termo_de_busca}&key={API_KEY}

Ao fazer a busca, o formulário deve ser movido para o topo da tela usando css animate e mostrar a lista de resultados com os campos título, descrição, thumbnail e um link para a página de detalhes.

Essa página deverá ter paginação, utilizando os [recursos de paginação da api](https://developers.google.com/youtube/v3/guides/implementation/pagination?hl=pt-br).

Construir um carrossel responsivo no footer abaixo da paginação, que deve exibir os vídeos apresentados na lista e obedecer os seguintes requisitos:

- Deve ser componente de autoria própria (não serão aceitos códigos de plugins reutilizados);
- Receber parâmetro de quantidade de quadros a serem exibidos e tempo de animação;
- Pausar animação no "mouse hover";
- Animação infinita (não deixar espaços vazios na exibição);
- Deve ter função de reload vinculada com a paginação;
- Deve ter status null (resposta de busca vazia).

### Tela de detalhes
A partir do videoId retornado na outra chamada, deve ser feito uma chamada para https://www.googleapis.com/youtube/v3/videos?id={VIDEO_ID}&part=snippet,statistics&key={API_KEY}

A partir desse retorno, deve-se montar uma tela contendo embed do video, título, like, deslike, descrição e visualizações.

Essa tela deve ter um botão para voltar, exibindo os últimos resultados da busca com a pagina em questão ativa.

### Wireframe
wireframe mobile: https://invis.io/TKNIYA2FH3M#/314438484_M-SearchHome

wireframe desktop: https://invis.io/TKNIYA2FH3M#/314438479_D-SearchHome

## O que será avaliado?
- Organização do projeto
- Lógica do código
- Uso do Git
- Uso de componentização
- Testes automatizados
