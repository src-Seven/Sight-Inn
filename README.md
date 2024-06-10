# Sight Inn

Projeto Integrador 2 - Hotel

## Descrição

O **Sight Inn** é um projeto integrador 2 que consiste em um site para gerenciar e visualizar informações de hotéis e resorts ao redor do mundo. O projeto foi desenvolvido utilizando Node.js e EJS, e inclui funcionalidades para exibir detalhes dos hotéis, realizar avaliações e gerenciar reservas.


## Pré-requisitos
- Node 17 ou mais recente
- Um meio de execução do projeto (IDE)

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução para JavaScript.
- **Express**: Framework web para Node.js.
- **EJS (Embedded JavaScript)**: Motor de template para gerar HTML com dados dinâmicos.
- **MongoDB**: Banco de dados NoSQL para armazenar informações dos hotéis.
- **Mongoose**: Biblioteca para modelar dados do MongoDB.
- **express-session**: Middleware para gerenciar sessões no Express.
- **nodemon**: Ferramenta para reiniciar automaticamente o servidor Node.js durante o desenvolvimento.
- **@barba/core**: Biblioteca para animações de transições de páginas.
- **popmotion**: Biblioteca para animações.

## Instalação

Siga os passos abaixo para configurar e executar o projeto localmente:

1. Clone o repositório:
    git clone https://github.com/seu-usuario/sight-inn.git
    cd sight-inn
2. Instale as dependências:
    npm install

3. Configure o arquivo de ambiente:
    Modificar o URI de acordo com a porta do banco de dados: 
    MONGODB_URI=mongodb://localhost:27017/sightinn

5. Execute o projeto:
    npm start

## Estrutura do Projeto

- `index.js`: Arquivo principal do servidor Node.js.
- `views/`: Diretório que contém os templates EJS.
- `public/`: Diretório para arquivos estáticos (CSS, JS, imagens).
- `models/`: Diretório para definir os modelos de dados do MongoDB.
- `controller/`: Diretório para definir as rotas do aplicativo.
- `service/`:  Diretório das classes de serviço.
- `repository/`: Diretório com os repositórios que possuem conexão ao banco de dados.

## Endpoints

### Hotel

#### Hotel (GET) 
- /?Page -> Retornará a home, poderá receber requisição de query para acesso da página, exemplo /2 -> Página 2.
- /hotel/apartamento/{id} -> Retornará um hotel específico com um quarto, normalmente o de índice 0.
- /hotel/usuario/recents -> Retornará os recentes do usuário, não há necessidade de login, porém o armazenamento é resetado com o reiniciar do servidor node.
- /hotel/points/map -> Retorna o mapa com hotéis.
- /hotel/fav/{idPessoa} -> Verifica os favoritos de uma pessoa em específico.

#### Hotel (POST)
- /hotel/fav/{idHotel} -> Adiciona um favorito ao hotel, mas verifica anteriormente se a pessoa está ou não em sessão logada.
- /hotel/fav/delete/{idHotel} -> Remove um favorito nas mesma condições acima.



#### Usuário (POST)
- /cadastro/usuario -> Realiza o cadastro do usuário recebendo como parâmetro email e senha.
- /login -> Realiza o login com os mesmos parâmetros citados anteriormente.


## Banco de Dados
Para o banco foram utilizados o MongoDB como banco não relacional específico para documentos e o Mongoose como meio de acesso fácil e ágil ao banco.
