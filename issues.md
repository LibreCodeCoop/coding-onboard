- [Tarefas (issues)](#tarefas-issues)
  - [Elementos necessários](#elementos-necessários)
    - [Definição da tarefa](#definição-da-tarefa)
    - [Contexto](#contexto)
    - [Escopo](#escopo)
    - [Fora de escopo](#fora-de-escopo)
    - [Critérios de aceitação](#critérios-de-aceitação)
    - [Observações](#observações)
  - [Marcadores (labels)](#marcadores-labels)
  - [Ciclo de aprovação](#ciclo-de-aprovação)
    - [Integração contínua](#integração-contínua)
    - [Revisão de tarefa](#revisão-de-tarefa)
      - [Revisores](#revisores)
      - [Teste em homolog](#teste-em-homolog)

# Tarefas (issues)

Você pode ver um template de issue [aqui](template/issue.md)

## Elementos necessários

### Definição da tarefa

As tarefas são documentadas seguindo o modelo:

**Eu como** [X] **quero** [Y] **para que** [Z]

Exemplo:

**Eu como** pessoa autenticada no sistema estando na página do perfil do usuário

**quero** enviar arquivos de identificação

**para que** apareçam no meu perfil para outras pessoas atendendo requisito de validação de conta.

### Contexto

Descrição breve do contexto onde esta tarefa está inserida, pode talvez fazer referência a estória.

### Escopo

Lista de resumo de entregáveis e macro-ações feitas na tarefa. É diferente dos critérios de aceitação pois não é um passo a passo para testar a funcionalidade.
- [ ] Salvar documento no storage do usuário
- [ ] Criar migration para as alterações de banco

### Fora de escopo

Lista de possíveis itens que podem talvez gerar confusão na hora de compreender a tarefa. Para ficar claro que não faz parte da tarefa, crie uma lista destes itens.

Exemplo:
- [ ] Atualizar o aplicativo em homolog
- [ ] Não vai ter preview de documentos

### Critérios de aceitação

Os critérios de aceitação devem seguir modelo gherkin de escrita de cenários descrevendo todas as etapas necessárias para que a tarefa seja executada.

Exemplo:

**Cenário**: título do primeiro cenário
- [ ] **Dado** algum contexto inicial,
- [ ] **Quando** ocorre um evento,
- [ ] **Então** verifique alguns resultados.

### Observações

Campo livre para uma outra observação que precisa ser feita.

Se necessário coloque prints para ilustrar melhor a tarefa.

## Marcadores (labels)

Toda tarefa deve conter [labels](labels.md)

## Ciclo de aprovação

### Integração contínua

Apenas será feito code review após a tarefa passar na integração contínua.

### Revisão de tarefa

Apenas será feito após todas as tarefas da CI passarem.

Necessário pelo menos um revisor para que uma tarefa seja aprovada e seja integrada ao código

#### Revisores

As tarefas devem ser revisadas por:
* outra pessoa do time técnico
* Gestor do projeto

#### Teste em homolog

Algumas tarefas precisam ser testadas em homologação antes de ter o code review aprovado.

