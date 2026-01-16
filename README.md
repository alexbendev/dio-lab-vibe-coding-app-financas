# VibeCod

**App de Finanças Pessoais com Prompt-Orchestrated Benchmarking (POB)**

<img width="1920" height="1080" alt="Captura de tela de 2026-01-16 12-52-28" src="https://github.com/user-attachments/assets/d6ead9fc-79a7-455e-9444-eefcd80cf5ab" />
<img width="1920" height="1080" alt="Captura de tela de 2026-01-16 12-52-07" src="https://github.com/user-attachments/assets/93a9a6e7-4bc4-4975-a211-06ab34c3e0f9" />
<img width="1920" height="1080" alt="Captura de tela de 2026-01-16 12-52-14" src="https://github.com/user-attachments/assets/faed4996-dfd7-4e8e-a46b-884c2bbe7a4a" />
<img width="1920" height="1080" alt="Captura de tela de 2026-01-16 12-52-20" src="https://github.com/user-attachments/assets/65f07bdf-14ac-4070-952b-dd7c9b2d0e61" />

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

[cinnamon-2026-01-16T131534-0300.webm](https://github.com/user-attachments/assets/da82ef7a-e573-449b-bd96-b01891f4ecfd)

https://github.com/user-attachments/assets/8f76a2b4-36d7-4264-92f1-9e503eb8578a

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

## Prompt Final
16 de jan.at 11:56

Create a prototype of the VibeCod Finance App using the Prompt-Orchestrated Benchmarking (POB) framework.
The app must combine conversational AI, deterministic evaluation, and gamification (badges and rewards).
Development workflow integrates Microsoft Copilot (prompt design, documentation, evaluation) and Lovable (interface prototyping).
Core Framework (POB)

    ASR (Automatic Speech Recognition)
        Convert speech to text.
        Example input: "How much can I save this month and where to invest $2000 safely?"

    Phenomenological Layer
        Extract intents: "calculate monthly savings", "suggest safe investment".
        Formalization: Ψ(oi | m) = E[f(oi)] → produces phenomenological score.

    Multi-Dimensional Scoring
        Evaluation operator: Φ : (oi, pk) → sik ∈ [0,1]^d.
        Aggregated score: si = Σk wk sik , with Σk wk = 1.
        Dimensions: phenomenological, semantic, numeric, contextual.

    ORRS (Occam-Regularized Risk Score)
        Formula: ORRS(oi) = min_{Ml ∈ M} [ l(si | Ml) + λC(Ml) ].
        Penalizes complex or risky outputs, favors simple and safe recommendations.

    TAR Filtering
        Formula: r̃i = Σ_{k=1}^p ak(i) ri−k + εi.
        Ensures bounded-input bounded-output stability across sessions.

    Hallucination Risk Control
        Formula: P(Hi = 1 | si) = σ( α0 + Σj αj (1 − si) ).
        Uses sigmoid to estimate hallucination probability.

    Acceptance & Logging
        Final approved response delivered to user.
        All prompts, scores, and decisions logged for auditability and reproducibility.

Interface Requirements

    Chat screen for natural language interaction.
    History screen showing transactions and motivational messages.
    Summary screen with balance, goals, achievements, and badges.
    Universal Design: high contrast, adaptive fonts, screen reader compatibility.
    Developed by Alexandre Augusto Benavides

Gamification

    Badges: Consistency, Savings, Smart Correction, Planner, Transparency.
    Rewards: motivational feedback, visual seals, advanced reports, educational tips.
    All badges and rewards validated via POB scoring and ORRS.

Target Audience

    Young adults starting financial management.
    Busy professionals needing quick reports.
    Users with low tolerance for complex numbers.
    Researchers testing POB in real-world applications.

Technologies (conceptual)

    React Native (Expo)
    Node.js + Express
    SQLite / Firebase
    Styled Components
    POB Engine
    Microsoft Copilot (prompt orchestration and documentation)
    Lovable (interface prototyping)

---    

Reflexão

Relato de uso — versão aprimorada

Uso de Copilot e Lovable acelerou significativamente o fluxo de trabalho: vibe coding tornou-se uma forma eficiente de prototipagem rápida para tomada de decisão, permitindo validar hipóteses e obter feedback real em minutos. Essa abordagem reduz o atrito e diminui a necessidade de estudos longos e documentação extensa nas fases iniciais.
Entretanto, isso não elimina a necessidade da engenharia de software básica: arquitetura, testes, segurança e manutenção continuam essenciais para transformar protótipos em produtos confiáveis e escaláveis.

---

## Status do Projeto

🚧 **Em desenvolvimento (MVP)**
Foco atual: validação do fluxo POB, estabilidade das respostas e experiência do usuário, linguagens suportadas.
