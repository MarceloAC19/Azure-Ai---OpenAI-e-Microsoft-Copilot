# Azure-Ai---OpenAI-e-Microsoft-Copilot

# Desafio: Explorando IA Generativa no Azure

Este repositório documenta a jornada de exploração das funcionalidades do **Azure OpenAI Studio** e do **Copilot**, conforme proposto no desafio. O objetivo principal é demonstrar o uso de ferramentas de IA generativa, a aplicação de prompts eficazes e a análise do comportamento dos filtros de conteúdo.

## 🎯 Objetivo

O laboratório consiste em explorar as funcionalidades do Copiloto e das ferramentas da OpenAI, com ênfase nos filtros de conteúdo e nos recursos de criação assistida por inteligência artificial. O entregável é este repositório organizado com exemplos de uso, prompts aplicados e anotações sobre os aprendizados adquiridos.

## 🛠️ Tecnologias Utilizadas

* **Azure AI Studio**: Plataforma para explorar, construir, testar e implantar soluções de IA, incluindo modelos de linguagem da OpenAI.
* **Azure OpenAI Service**: Serviço que fornece acesso aos modelos de linguagem avançados da OpenAI (como GPT-4, GPT-3.5) com os benefícios de segurança e conformidade do Azure.
* **Engenharia de Prompt**: A arte de criar entradas (prompts) claras e eficazes para obter as respostas desejadas da IA.
* **Filtros de Conteúdo**: Mecanismos de segurança do Azure AI para detectar e prevenir a geração de conteúdo potencialmente prejudicial (ódio, sexual, violência, auto-mutilação).

## 🧠 Aprendizados Adquiridos

### 1. Engenharia de Prompt

A qualidade da saída da IA está diretamente ligada à qualidade do prompt. Aprendi que a clareza, o contexto e a especificação são fundamentais.

* **Contexto é Rei**: Fornecer um contexto claro (`"Você é um roteirista de ficção científica..."`) melhora drasticamente a relevância da resposta.
* **Especificidade**: Em vez de pedir `"crie um código"`, um prompt como `"crie uma função em Python que recebe uma lista de números e retorna a média"` gera um resultado muito mais útil e preciso.
* **Interação**: O primeiro prompt raramente é o melhor. É um processo de refinar e adicionar detalhes até alcançar o resultado desejado.

### 2. Filtros de Conteúdo

A exploração dos filtros de conteúdo do Azure foi um dos pontos mais importantes.

* **Segurança por Padrão**: O Azure OpenAI vem com filtros de conteúdo habilitados por padrão para quatro categorias: **ódio, sexual, violência e automutilação**.
* **Níveis de Severidade**: É possível configurar a sensibilidade dos filtros (baixo, médio, alto), permitindo um balanço entre segurança e liberdade de geração.
* **Resposta do Filtro**: Quando um prompt ou uma resposta é bloqueado, a API retorna uma mensagem de erro clara, indicando que o filtro foi ativado (`"content_filter"`). Isso é essencial para o desenvolvimento de aplicações seguras e responsáveis.
* **Falsos Positivos**: Em alguns casos, um prompt legítimo pode ser interpretado erroneamente como prejudicial. A documentação do Azure sugere reportar esses casos para aprimorar o serviço.

### 3. Ecossistema Azure AI

O **Azure AI Studio** se mostrou uma ferramenta poderosa e centralizadora. A capacidade de testar prompts, ajustar parâmetros (como temperatura e `top_p`), e observar o comportamento dos filtros em uma única interface agiliza muito o desenvolvimento de soluções de IA Generativa de forma responsável.

---

*Projeto desenvolvido como parte do desafio de IA Generativa.*
