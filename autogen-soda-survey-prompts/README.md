# AutoGen Studio - Pesquisa de Aceitação de Refrigerante

Este repositório contém os prompts usados na atividade multiagente desenvolvida no **AutoGen Studio**.

## Objetivo

O objetivo da atividade é simular uma pesquisa de aceitação de produto para um novo sabor de refrigerante:

> **Pitanga with Ginger Soda**

O fluxo utiliza um agente principal e três agentes avaliadores:

1. **MainAgent** - apresenta o produto, solicita avaliações e consolida o resultado final.
2. **SportsFanAI** - avalia o produto do ponto de vista de um consumidor ativo e esportivo.
3. **MinimalistAI** - avalia o produto do ponto de vista de um consumidor que prefere produtos simples e equilibrados.
4. **TechLoverAI** - avalia o produto do ponto de vista de um consumidor interessado em novidade e inovação.

## Modelo LLM Usado

As inferências foram realizadas com o modelo local:

```txt
google/gemma-4-e4b
```

O modelo foi executado por meio do **LM Studio** e conectado ao **AutoGen Studio** usando um endpoint local compatível com OpenAI.

## Configuração da Equipe

- **Tipo de equipe:** `RoundRobinGroupChat`
- **Ordem dos participantes:**
  1. MainAgent
  2. SportsFanAI
  3. MinimalistAI
  4. TechLoverAI
- **Condição de término:** `MaxMessageTermination`
- **Mensagens máximas:** `10`

## Mensagem Inicial da Tarefa

```txt
Start the product acceptance survey for the new Pitanga with Ginger soda. MainAgent must first present the product and ask the evaluator agents for their opinions. After all three evaluators respond, MainAgent must consolidate the final result.
```

## Arquivos de Prompt

- [`prompts/MainAgent.md`](prompts/MainAgent.md)
- [`prompts/SportsFanAI.md`](prompts/SportsFanAI.md)
- [`prompts/MinimalistAI.md`](prompts/MinimalistAI.md)
- [`prompts/TechLoverAI.md`](prompts/TechLoverAI.md)
