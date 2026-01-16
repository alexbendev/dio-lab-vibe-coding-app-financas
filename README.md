# VibeCod

**App de Finanças Pessoais com Prompt-Orchestrated Benchmarking (POB)**

## Visão Geral

O **VibeCod** é um aplicativo de **finanças pessoais** que ajuda usuários a registrar receitas e despesas, acompanhar sua saúde financeira e receber **recomendações inteligentes, explicáveis e confiáveis** baseadas em IA.

Seu principal diferencial é a adoção do framework **Prompt-Orchestrated Benchmarking (POB)**, que garante que as respostas da IA sejam **determinísticas, auditáveis e reprodutíveis**, reduzindo variabilidade indesejada e aumentando a confiança do usuário.

📄 **Paper oficial do POB:**
[https://github.com/alexbendev/pob-paper](https://github.com/alexbendev/pob-paper)

Além disso, o VibeCod utiliza **gamificação (badges e recompensas)** para transformar o controle financeiro em uma jornada educativa e engajadora.

---

## Diferenciais-Chave

* IA **explicável e estável**
* Recomendações com **confiança (%) e justificativa curta**
* Avaliação técnica baseada em POB
* Gamificação auditável
* Arquitetura pronta para MVP e evolução contínua

---

## Funcionalidades

### Gestão Financeira

* Cadastro de receitas e despesas
* Visualização de saldo atual e histórico
* Relatórios e gráficos de gastos
* Exportação de relatórios em PDF
* Autenticação de usuários

### Inteligência Artificial (POB)

* Aplicação do **Prompt-Orchestrated Benchmarking (POB)**
* Avaliação multidimensional:

  * Fenomenológica
  * Semântica
  * Numérica
  * Contextual
* Geração de **Occam-Regularized Risk Score (ORRS)**
* Filtro **TAR (Bounded-Input / Bounded-Output)** para estabilidade
* Respostas sempre contendo:

  * Categoria
  * Confiança (%)
  * Explicação curta (≤ 2 frases)
  * Ação sugerida

### Gamificação

* Sistema de **badges auditados pelo POB**
* Feedback positivo imediato
* Incentivo à correção e aprendizado do modelo

---

## PRD Resumido (Product Requirements Document)

### Objetivo do Produto

Construir um **MVP de finanças pessoais** que utilize IA de forma **controlada, explicável e confiável**, permitindo que usuários compreendam **por que** uma recomendação foi feita e **qual o nível de confiança** associado.

---

### Fluxo Principal de IA

Para cada transação enviada pelo usuário:

```
normalize_prompt
→ classify_prompt
→ explain_prompt
→ recommend_prompt
```

Cada etapa é orquestrada e avaliada pelo POB para garantir consistência e rastreabilidade.

---

### Exemplo de Interação

**Prompt enviado:**

```
Transação: 2026-01-10; R$ 45,00; Mercado Super Bom; cartão.
```

**Resposta esperada:**

```
Categoria: Alimentação
Confiança: 92%
Explicação: Compra em supermercado; valor e estabelecimento compatíveis.
Ação sugerida: Marcar como recorrente? [Sim / Não]
```

---

### API (MVP)

**Endpoint:** envio de transação financeira

**Resposta padrão:**

```json
{
  "category": "Alimentação",
  "confidence": 0.92,
  "explanation": "Compra em supermercado; valor e estabelecimento compatíveis.",
  "suggested_action": "Marcar como recorrente?"
}
```

---

### Critérios de Aceitação

* Acurácia de categorização **≥ 80%**
* Explicação clara e legível em **até 2 frases**
* Respostas consistentes sob o mesmo input (determinismo)
* Score ORRS dentro de limites aceitáveis
* Saída sempre dentro do escopo definido (TAR)

---

### Onboarding Inteligente

Onboarding guiado por prompts para criação do perfil financeiro:

* Renda mensal
* Prioridades financeiras
* Tolerância a risco

Esses dados alimentam o contexto do POB e influenciam as recomendações.

---

## Badges e Recompensas

* **Consistência:** registrar despesas por 7 dias consecutivos
* **Economia:** atingir 100%, 200% e 500% da meta
* **Correção Inteligente:** corrigir classificações da IA
* **Planejador:** definir e cumprir metas financeiras
* **Transparência:** consultar relatórios auditados pelo POB

🎁 Recompensas incluem selos visuais, feedback contextual e insights personalizados.

---

## Público-Alvo

* Jovens adultos organizando finanças pessoais
* Profissionais que buscam relatórios rápidos
* Usuários que valorizam **IA explicável**
* Pesquisadores e engenheiros interessados em **POB aplicado**

---

## Ferramentas de Apoio

* **Microsoft Copilot**

  * Estruturação e validação de prompts
  * Apoio à documentação e requisitos

* **Lovable**

  * Prototipagem rápida de UI
  * Simulação de fluxos conversacionais
  * Validação visual do PRD

---

## Stack Tecnológica

* **Frontend:** React Native (Expo)
* **Backend:** Node.js + Express
* **Banco de Dados:** SQLite / Firebase
* **Estilização:** Styled Components
* **IA:** Módulo **POB Engine**
* **Ferramentas:** Microsoft Copilot, Lovable

---

## Status do Projeto

🚧 **Em desenvolvimento (MVP)**
Foco atual: validação do fluxo POB, estabilidade das respostas e experiência do usuário.


Status do Projeto

🚧 Em desenvolvimento (MVP)
Foco atual: validação do fluxo POB, estabilidade das respostas e experiência do usuário.
