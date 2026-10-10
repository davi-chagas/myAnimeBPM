# AGENTS.md

## Visão geral

O **myAnimeBPM** é uma plataforma voltada a fãs de anime, mangá e da cultura japonesa, criada para reunir pessoas que reconhecem o impacto que essas histórias tiveram em suas vidas.

O projeto busca proporcionar um espaço para compartilhar sentimentos, reflexões, mensagens e informações sobre animes, além de incentivar discussões, conexões e a troca de experiências entre pessoas com interesses em comum.

## Tecnologias

- Node.Js
- HTML
- CSS
- MySQL

## Comandos

```
npm start
``` 
Serve para iniciar a aplicaçao em modo de Produção.

```
npm run dev
``` 
Serve para iniciar a aplicaçao em modo de desenvolvimento.

## Arquitetura

O projeto utiliza a arquitetura MVC (Model-View-Controller), organizando as responsabilidades da aplicação em rotas, controllers e models.

### Estrutura do projeto

- `routes/`: define as rotas e os endpoints disponíveis na aplicação.
- `controllers/`: recebe e processa as requisições, aplica a lógica de controle e coordena a comunicação entre as rotas e as models.
- `models/`: concentra as operações de acesso e manipulação dos dados no banco de dados MySQL.
- `.env`: armazena as variáveis de ambiente utilizadas na configuração da aplicação.
- `.env.dev`: armazena as variáveis de ambiente específicas do ambiente de desenvolvimento.
- `app.js`: ponto de entrada da aplicação, responsável pela inicialização e configuração do servidor.
- `public/`: contém os arquivos públicos do front-end, como HTML, CSS, JavaScript e imagens.

### Fluxo de uma requisição

O usuário interage com o front-end e realiza uma requisição HTTP para um endpoint definido em `routes/`. A rota direciona a requisição ao controller correspondente, que processa a solicitação e aciona a model quando há necessidade de consultar ou modificar dados no banco de dados. A model executa a operação e retorna o resultado ao controller, que prepara e envia a resposta HTTP ao cliente.


## Padrões de desenvolvimento
- Utilizar const por padrão e let apenas quando houver necessidade de reatribuição
- Utilizar formato snake_case para variaveis, const e o que for relacionado ao banco de dados
- Utilizar camelCase para funções

## Padrões de commits
Utilize os seguintes prefixos para identificar o objetivo de cada commit:

- `feat`: adiciona uma nova funcionalidade.
- `fix`: corrige um erro existente.
- `docs`: adiciona ou modifica documentação.
- `style`: altera formatação ou aspectos visuais sem modificar a lógica da aplicação.
- `perf`: melhora o desempenho.
- `refactor`: reorganiza ou melhora o código sem alterar seu comportamento esperado.
- `test`: adiciona, modifica ou corrige testes.
- `chore`: realiza tarefas de manutenção, configuração ou organização do projeto.

### Formato das mensagens

Utilize o seguinte formato:

`tipo(escopo): descrição breve da alteração`

Exemplos:

- `feat(login): adiciona validação de credenciais`
- `fix(cadastro): corrige validação do email`
- `docs(readme): atualiza instruções de instalação`
- `style(home): ajusta espaçamento dos elementos`
- `perf(models): otimiza consulta de usuários`
- `refactor(routes): reorganiza endpoints de autenticação`
- `test(login): adiciona testes de autenticação`
- `chore(deps): atualiza dependências do projeto`

A descrição deve ser curta, específica e indicar o que foi alterado.

## Padrões de branches

O repositório será organizado utilizando duas branches principais:

```text
main
└── dev
```

### `main` — Produção

É a branch principal do projeto e representa a versão considerada estável.

- Não desenvolver diretamente na `main`.
- Integrar alterações somente após verificar se estão funcionando corretamente.
- Manter a branch em um estado estável, evitando código incompleto ou experimental.

### `dev` — Desenvolvimento

É a branch destinada à integração das funcionalidades em desenvolvimento.

- Realizar o desenvolvimento cotidiano a partir da `dev`.
- Testar as alterações antes de integrá-las à `main`.
- Utilizar commits claros e seguir os padrões definidos neste documento.
- Integrar a `dev` à `main` quando houver uma versão estável do projeto.

### Fluxo de trabalho

1. Atualizar a branch `dev` antes de começar uma nova tarefa.
2. Implementar a alteração e registrar o trabalho com commits descritivos.
3. Verificar o funcionamento da aplicação.
4. Integrar as alterações à `main` quando a versão estiver estável.

## Cuidados e restrições

### Integridade do projeto
- Não altere a arquitetura, a estrutura de diretórios ou as tecnologias definidas para o projeto sem autorização explícita.
- Respeite os padrões de código, as convenções de nomenclatura e as decisões técnicas já adotadas.
- Não adicione dependências, ferramentas ou funcionalidades sem necessidade justificada e autorização.
- Antes de modificar arquivos existentes, compreenda sua finalidade e avalie o impacto da alteração.

### Código e legibilidade
- Escreva o código e os identificadores em português brasileiro (`pt-BR`), respeitando as convenções exigidas pelas tecnologias utilizadas.
- Priorize código simples, legível e didático, adequado ao nível de conhecimento de um estudante do primeiro semestre de Análise e Desenvolvimento de Sistemas.
- Prefira soluções fáceis de compreender e manter, em vez de otimizações prematuras de desempenho.
- Evite abstrações, padrões de projeto ou recursos avançados quando uma solução mais simples atender ao mesmo objetivo.

### Aprendizado e uso da IA
- Priorize o aprendizado e a compreensão dos conceitos utilizados no projeto.
- Não implemente funcionalidades completas sem uma solicitação explícita.
- Prefira orientar a resolução de problemas e apresentar exemplos pontuais em vez de desenvolver soluções inteiras pelo usuário.
- Ao apresentar ou sugerir código, explique sua lógica, os conceitos envolvidos e as decisões técnicas relevantes.
- Quando identificar um erro, explique sua causa e apresente possíveis caminhos para a correção antes de propor alterações extensas.
- Não modifique arquivos automaticamente apenas porque identificou uma possível melhoria; apresente a proposta e aguarde autorização quando a mudança não tiver sido solicitada explicitamente.


## Regra geral: 
Antes de implementar uma alteração, siga as tecnologias, arquitetura, convenções e restrições descritas neste documento. Caso alguma informação esteja ausente, analise o código existente e siga os padrões já adotados no projeto.
