
# Teste Backend

Leia primeiro todo o projeto, faça sua estimativa de horas para o desenvolvimento e envie um e-mail com o título `[Teste Backend] Estimativa` para dev2@engenhadev.com.

Forke este projeto, desenvolva e quando finalizar, faça um PR aqui. Envie um e-mail com o título `[Teste Backend] Finalizado` para dev2@engenhadev.com com o link do seu PR.

Se você não sabe o que é fazer um `Fork` ou um `PR`, pesquise. Valorizamos muito a proatividade.

Lembre-se de verificar todos arquivos deste repositório.

**Lembre-se: atualize este README informando como instalar e executar seu projeto.**

## Missão

Desenvolver uma `API REST` com `Django Ninja`, que utilize os métodos `GET` e `POST`.

### Arquitetura

Implemente a API seguindo o padrão de `Arquitetura de Camadas`, utilizando as seguintes divisões:

- Models: Definição dos modelos de dados.
- Services: Lógica de negócio e manipulação dos dados.
- Schemas: Definição dos esquemas de entrada e saída de dados.
- API: Camada que lida com as requisições HTTP e delega para os serviços apropriados.

### Especificação

Monte uma base de veículos com a seguinte estrutura:

```
id:             uuid
name:           char
year:           positive integer
description:    text
sold:           bool
created:        datetime
```

Utilize `SQLite` para armazenar os dados que a API irá consumir.

### API Endpoints

`GET /cars`

Retorna todos os veículos.

---

`GET /cars/{car_id}`

Retorna o veículo com o id especificado no parâmetro.

---

`POST /cars`

Adiciona um novo veículo e envia um e-mail de confirmação `(Gmail)`.

### Bônus do Teste (⭐)

1. **Custom User Model:** Implementar um modelo de usuário personalizado e adicionar uma `FK` de user no modelo car.
```
id:             uuid
email:          email (unique)
created:        datetime
```
2. **PDF:** Gerar um PDF usando a biblioteca com `ReportLab Toolkit`, inserir os dados do carro e anexar ao e-mail.

### Desenvolvedores Mid Level

Obrigatório cumprir os requisitos de bônus, e também:

- **Autenticação:** Configurar uma rota que retorna um JWT e uma rota que retorna os dados do usuário pelo JWT da requisição usando a biblioteca `python-jose` e exigir autenticação em todas as outras rotas.
- **Documentação:** Configurar o `Swagger` e/ou `Redoc`
- **Admin**: Configurar o CRUD no `Django Admin` para car e user

## Dúvidas

Se tiver qualquer dúvida sobre esse teste, envie um e-mail com o título `[Teste Backend] O assunto que você deseja` para dev2@engenhadev.com.
