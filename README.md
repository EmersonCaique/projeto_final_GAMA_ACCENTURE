# Projeto GAMA ACADEMY + ACCENTURE - DESAFIO FINAL :rocket:
# Team {RA} DEVELOPERS

## Team :facepunch:

 [@RebeccaAlmeida](https://github.com/rebeccaalmeida1995) 
 
 [@RodrigoAlmeida](https://github.com/Rodrigoas3)
 
 [@EmersonCaique](https://github.com/EmersonCaique)
 
 [@DeyvessonCarlos](https://github.com/Deyvesson)
 
 [@LeandroOliveira]()
 

## Descrição do projeto :clapper:

:pushpin: Desenvolvemos um sistema de controle de habilidades e salários de uma emissora de TV, com as seguintes funcionalidades:

:heavy_check_mark: Cadastro de novo perfil de usuário (ator/atriz);

 Login e logout admin (produtor) e de usuário (ator/atriz); (WIP)
 
:heavy_check_mark: Busca na qual um admin (produtor) pode colocar o número de profissionais que precisa, o gênero de sua obra, a data na qual precisará iniciar as gravações e o orçamento máximo, e receber uma indicação de quais atores e atrizes contratar que se encaixem nos requisitos

:heavy_check_mark: Possibilidade de reservar a data de um ator ou atriz e exibição de status;

:heavy_check_mark: Filtro por status e classificação por relevância e preço;

:heavy_check_mark: Alguns outros filtros úteis;


## API :key:

:heavy_check_mark: React com a seguintes dependências: Wabpack, Babel, redux, sass, axios, express e material-ui.

:heavy_check_mark: Banco de dados: H2.

:heavy_check_mark: Ferramenta de gerenciamento de dependência de projeto: NPM.

## Planning :scroll:

:trophy: Divisão e priorização de tarefas.

:trophy: Durante os dias de desenvolvimento utilizamos ferramentas como Github, Trello, Slack e Discord para nos auxiliar.

:trophy: Encontros todos os dias, onde discutíamos pendências, dificuldades e estratégias para as próximas tarefas. Após o encontro, retornávamos para nossas atividades e quando necessário.

:trophy: Não definimos um scrum master para semana, todos acompanhávamos o desenvolvimento do projeto.


## GitHub :open_file_folder:

- [x] Mantivemos a main como branch principal.

## Requirements:

Para iniciar a API será necessário ter em sua máquina instalado a [versão JDK11 e configurar as variáveis de ambiente](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html), o Node.js (https://nodejs.org/en/) e utilizar o npm i para baixar todos as dependencias.


## Endpoints:

#### Atrizes
 
Criar atriz:
> POST `/actress/create`
```JSON
{
    "name": "Nome",
    "gender": "Gênero",
    "price": 0,
    "relevance": 0,
    "genre": "Gênero que atua",
    "status": true,
    "user": {
        "login": "login",
        "password": "senha"
    }
}
```

Listar todas as atrizes:
> GET `/actress/list`

Consultar dados de uma atriz pelo id:
> GET `/actress/{id}`

Atualizar dados de uma atriz:
> PUT `/actress/update/{id}`
```JSON
{
    "name": "Nome",
    "gender": "Gênero",
    "price": 0,
    "relevance": 0,
    "genre": "Gênero que atua",
    "status": true,
    "user": {
        "login": "login",
        "password": "senha"
    }
 }
```

Remover atriz:
>DELETE `/actress/delete?id=0`

Filtros:
>GET `/actress/getByStatus?status=true`

>GET `/actress/getMostRelevant`

>GET `/actress/getLessRelevant`

>GET `/actress/getMostExpensive`

>GET `/actress/getLessExpensive`


#### Produtores

Criar produtor:
> POST `/producer/create`
```JSON
{
    "name": "Nome",
    "user": {
        "login": "login",
        "password": "senha"
    }
}
```

Consultar dados de um produtor pelo id:
> GET `/producer/{id}`

Atualizar dados de uma produtor:
> PUT `/producer/update/{id}`
```JSON
{
    "name": "Nome",
    "user": {
        "login": "login",
        "password": "senha"
    }
}
```

Remover produtor:
>DELETE `/producer/delete?id=0`

Receber indicação de cast:
>GET `/producer/getCast?quantity=0&budget=0&genre=genero&date=2020-11-09`

#### Reservas

Criar reserva:
>POST `/reserve/save/{idDaAtriz}`
```JSON
{
    "reserveDate": "2020-11-09",
    "producer": {
        "id": 0
    }
}
```

Listar todas as reservas:
>GET `/reserve/list`

Atualizar reserva:
>PUT `/reserve/update/{idDaReserva}`
```JSON
{
    "reserveDate": "2020-11-09",
    "actress": {
    "id": 0
    },
    "producer": {
        "id": 0
    }
}
```

Deletar reserva:
>DELETE `/reserve/delete?id=0`

Filtros:
>GET `/reserve/listByActress/{idDaAtriz}`

>GET `/reserve/listByProducer/{idDoProdutor}`

>GET `/reserve/countByProducer/{idDoProdutor}`

>GET `/reserve/getMostReservedDatesByProducer/{idDoProdutor}`

>GET `/reserve/getMostReservedActressesByProducer/{idDoProdutor}`


## Experiência:

As maiores dificuldades foram relacionadas à pouco conhecimento tecnico, divisão de tarefas e ordem de execução das atividades.
Precisamos remodelar o projeto e redistribuir as entregas mais de uma vez.

E vimos que nossa maior produtividade e aprendizado foi utilizando a comunição e o trello.
A troca de experiências, qualidade de código e até velocidade de desenvolvimento foram muito proveitosas com essa técnica.

A equipe foi bastante agradável e unida, proporcionando sempre um ambiente leve e bem humorado, onde cada um supriu a deficiência existente no outro.
Não fomos muito independentes, mas bastante colaborativos!    