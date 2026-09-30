# Miniguia de Estudos: AI Business Leader

> Caderno temático criado no **NotebookLM** para estudar liderança de negócios na era da IA: estratégia, adoção, cultura e governança. Projeto do Desafio de Projeto da DIO.

---

## 1. Contexto e Objetivos

### Contexto
Escolhi **AI Business Leader** porque a IA deixou de ser só um assunto técnico e passou a ser uma decisão de negócio. Quem lidera precisa saber escolher onde aplicar IA, como preparar a organização e como manter o uso seguro e responsável. Quero desenvolver essa visão para atuar em projetos e equipes que usam IA.

### Objetivos de estudo
1. Entender os pilares que um líder precisa conduzir para adotar IA com sucesso (estratégia, tecnologia, cultura e governança).
2. Aprender a priorizar casos de uso de IA com critérios claros (impacto, viabilidade e tempo).
3. Conhecer um framework de gestão de risco de IA (NIST AI RMF) e o papel da governança.
4. Praticar o uso do NotebookLM como ferramenta de estudo: curadoria de fontes, prompts e verificação de respostas.

### Como usei o NotebookLM
Criei um caderno com 5 fontes abertas, fiz perguntas estratégicas, comparei variações de prompts, conferi as citações apontadas pelo NotebookLM e documentei as dificuldades encontradas.

---

## 2. Curadoria de Fontes

| # | Fonte | Tipo | Por que escolhi |
|---|---|---|---|
| 1 | [Transform your business with AI (Microsoft Learn)](https://learn.microsoft.com/en-us/training/paths/transform-your-business-with-microsoft-ai/) | Trilha de aprendizagem | Base do tema: planejar, definir estratégia e escalar IA de forma responsável para líderes de negócio. |
| 2 | [Drive business value with AI solutions (Microsoft Learn)](https://learn.microsoft.com/en-us/training/paths/drive-value-generative-ai-solutions/) | Trilha de aprendizagem | Traz o lado prático: alinhar IA aos objetivos, automatizar tarefas e adotar soluções seguras. |
| 3 | [Building a Foundation for AI Success: A Leader's Guide](https://marketingassets.microsoft.com/gdc/gdcu5n8qE/original) | PDF | Organiza a adoção de IA em cinco pilares, ótimo para resumos estruturados. |
| 4 | [The AI Strategy Roadmap: Five drivers of successful AI transformation](https://www.microsoft.com/en-us/microsoft-cloud/blog/2026/07/21/the-ai-strategy-roadmap-five-drivers-of-successful-ai-transformation/) | Artigo | Fonte mais recente (2026); ajuda a avaliar a maturidade da organização e escalar a IA. |
| 5 | [NIST AI RMF 1.0 (NIST AI 100-1)](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf) | PDF | Fonte neutra e oficial sobre gestão de risco de IA; equilibra as fontes de fornecedor. |

> **Ponto de atenção:** quatro das cinco fontes são da Microsoft, então existe viés de fornecedor. Isso influencia as respostas do NotebookLM (ex.: menções a Copilot e outros produtos). A fonte do NIST é a contrapartida neutra.

---

## 3. Engenharia de Prompts e Cicatrizes

Formato de cada teste: **prompt → resposta (resumo e fontes) → dificuldade → ajuste**. As respostas abaixo estão resumidas; o NotebookLM respondeu em português mesmo com fontes em inglês.

### Teste 1: Visão geral da adoção de IA

**Prompt (versão inicial):**
```
Resuma o que é preciso para um líder conduzir a adoção de IA.
```
**Resposta (resumo):** o NotebookLM organizou a resposta em cinco pilares: (1) estratégia de negócios, com alinhamento aos objetivos, priorização de casos de uso e métricas de ROI; (2) estratégia tecnológica e de dados, com plataforma de dados governada, decisão entre comprar, modernizar ou construir e infraestrutura escalável; (3) estratégia e experiência em IA, com escolha do modelo certo para cada problema e práticas repetíveis; (4) organização e cultura, com modelo operacional, letramento em IA e ambiente que aceita aprender com falhas; (5) governança e segurança, com IA responsável desde o início, supervisão humana e gestão contínua de riscos.

**Dificuldade / cicatriz:** a resposta veio bem estruturada, mas **sem indicar de qual fonte vinha cada ponto**, o que impede conferir o conteúdo. Além disso, trouxe o dado de que fatores organizacionais respondem por 67% do valor gerado pela IA, sem dizer de onde vinha.

**Variação testada:**
```
Resuma em 5 tópicos, citando de qual fonte vem cada ponto.
```
**Resultado:** a resposta condensou os cinco pilares em 5 tópicos e passou a citar as fontes (Leader's Guide, AI Strategy Roadmap, Microsoft Learn e NIST AI RMF), cada uma ligada ao tópico correspondente.

**Verificação que fiz:** conferi o número de 67% no artigo *The AI Strategy Roadmap: Five drivers* (fonte 4). O artigo atribui o dado ao *Microsoft 2026 Work Trend Index*, ou seja, é uma pesquisa da própria Microsoft citada pela fonte, e não um estudo independente.

**Aprendizado:** pedir **formato + formato de citação** no prompt (número de tópicos e fonte de cada ponto) melhora a rastreabilidade e facilita a checagem.

---

### Teste 2: Glossário

**Prompt (versão inicial):**
```
Crie um glossário com os 15 termos mais importantes.
```
**Resposta (resumo):** lista numerada com 15 termos (IA, IA generativa, machine learning, cinco pilares, roteiro de estratégia de IA, governança, IA responsável, gestão de riscos, confiabilidade, explicabilidade, modelo operacional, ciclo de vida, TEVV, viés e RAG), cada um com uma definição.

**Dificuldade / cicatriz:** as definições vieram **sem fonte**. Termos muito gerais (IA, machine learning) parecem vir do conhecimento geral do modelo e não necessariamente das fontes do caderno, o que fere a ideia de estudar só com material curado.

**Variação testada:**
```
Crie o glossário em tabela com termo, definição simples e fonte.
```
**Resultado:** o NotebookLM devolveu uma tabela com três colunas (termo, definição simples, fonte). Pedir "definição simples" deixou os textos mais curtos.

**Nova dificuldade:** em vários termos a coluna de fonte trouxe **duas fontes juntas** (ex.: "Guia do Líder / NIST"), o que ainda não mostra com precisão de onde saiu cada definição. Para uso em estudo, o ideal seria conferir o termo diretamente na citação numerada.

**Aprendizado:** definir as colunas da tabela no prompt força a estrutura, mas a coluna de fonte precisa de checagem manual.

---

### Teste 3: O que é o NIST AI RMF?

**Prompt:**
```
O que é o NIST AI RMF?
```
**Resposta (resumo):** o NotebookLM explicou que é um framework voluntário e flexível do NIST, dividido em duas partes: a primeira define as sete características de uma IA confiável (válida e confiável, segura, protegida e resiliente, transparente e responsável, explicável e interpretável, com privacidade aprimorada, justa com vieses gerenciados); a segunda apresenta as quatro funções do núcleo (Govern, Map, Measure, Manage). Explicou também por que ele é necessário: a IA é socio-técnica e probabilística, diferente de software tradicional.

**Dificuldade / cicatriz:** a resposta é correta e organizada, mas **técnica**: mistura termos como TEVV e "socio-técnico" sem explicar para quem não é da área. Isso levou ao teste seguinte.

---

### Teste 4: As 4 funções do NIST para um gestor sem formação técnica

**Prompt:**
```
Explique as 4 funções (Govern, Map, Measure, Manage) como se eu fosse um gestor sem formação técnica.
```
**Resposta (resumo):** para cada função, o NotebookLM deu três blocos: **o que é**, **o papel do gestor** e **na prática**, com analogias de negócio (código de conduta, estudo de viabilidade, auditoria de qualidade, plano de contingência).

**Dificuldade / cicatriz:** a resposta anterior, sem definir o público, foi técnica demais. **Definir a persona** ("gestor sem formação técnica") mudou o tom e trouxe analogias, mas a resposta ficou longa; um limite de tamanho no prompt ajudaria.

**Aprendizado:** informar o público-alvo no prompt muda mais a resposta do que pedir "explique melhor".

---

### Resumo das cicatrizes (troubleshooting)

| Problema | O que fiz para resolver |
|---|---|
| Resposta correta, mas sem indicar a fonte de cada ponto | Pedi número de tópicos e a fonte de cada um no prompt |
| Glossário sem fonte e com termos genéricos | Pedi tabela com coluna de fonte e conferi manualmente |
| Fonte da tabela imprecisa (duas fontes juntas) | Passei a checar a citação numerada de cada definição |
| Dado numérico (67%) sem origem clara | Rastreei até o artigo da fonte 4 e registrei que é pesquisa da própria Microsoft |
| Resposta técnica demais | Defini a persona ("gestor sem formação técnica") |
| Viés de fornecedor nas fontes | Documentei o ponto na curadoria e mantive o NIST como fonte neutra |

---

## 4. Miniguia de Estudo

> Escrito com minhas palavras a partir das respostas do NotebookLM, conferidas com as fontes.

### 4.1 Resumos estruturados

**Visão geral:** adotar IA com sucesso não é só uma questão de tecnologia. O líder precisa alinhar a IA à estratégia do negócio, preparar dados e infraestrutura, escolher bem as soluções, cuidar da cultura e das pessoas, e manter governança e gestão de riscos desde o começo.

#### Pilar 1: Estratégia de negócio
- Ligar os investimentos em IA a objetivos de negócio mensuráveis.
- Priorizar casos de uso de alto impacto, com patrocínio executivo.
- Definir métricas de retorno (ROI) para os projetos não ficarem eternamente em "prova de conceito".
- Comunicar a visão de IA de forma clara na organização.

#### Pilar 2: Tecnologia e dados
- Ter uma base de dados confiável, governada e acessível com segurança.
- Decidir com critérios quando comprar, modernizar ou construir.
- Usar infraestrutura escalável (nuvem) com postura de segurança rigorosa.

#### Pilar 3: Estratégia e experiência em IA
- Escolher o modelo e a ferramenta certos para cada problema.
- Pensar na experiência de clientes e colaboradores.
- Criar práticas repetíveis de entrega para acelerar a geração de valor.

#### Pilar 4: Organização e cultura
- A cultura pesa muito: a fonte 4 cita que fatores organizacionais respondem por 67% do valor realizado com IA (dado da própria Microsoft).
- Definir um modelo operacional de IA (como a IA é distribuída entre as áreas).
- Investir em letramento e capacitação contínua.
- Criar um ambiente seguro para experimentar e aprender com falhas.

#### Pilar 5: Governança de IA
- Incluir ética, privacidade, segurança e conformidade desde a concepção.
- Manter supervisão humana e responsabilidades claras.
- Gerenciar riscos de forma contínua ao longo do tempo.

#### Gestão de risco: as 4 funções do NIST AI RMF
| Função | Ideia central | Na prática (visão do gestor) |
|---|---|---|
| **Govern** | Cultura, regras e responsabilidades | Definir políticas, limites de risco e quem responde por quê |
| **Map** | Entender contexto e riscos | Analisar quem usa, para quê e o que pode dar errado, antes de decidir se segue |
| **Measure** | Testar e monitorar | Exigir métricas e testes para provar que a IA é precisa, segura e justa |
| **Manage** | Agir sobre os riscos | Mitigar, aceitar ou evitar riscos e ter plano para corrigir ou desligar o sistema |

Uma IA confiável, segundo o NIST, equilibra sete características: válida e confiável, segura, protegida e resiliente, transparente e responsável, explicável e interpretável, com privacidade aprimorada e justa (com vieses gerenciados).

### 4.2 Glossário

> Definições reescritas a partir do glossário do NotebookLM. A coluna de fonte é a indicada pelo NotebookLM e deve ser conferida na citação.

| Termo | Definição simples | Fonte indicada |
|---|---|---|
| Inteligência Artificial (IA) | Sistemas de computador que fazem tarefas que normalmente exigem inteligência humana, como decidir, reconhecer fala e entender linguagem. | Leader's Guide / NIST AI RMF |
| IA Generativa | IA que cria conteúdo novo (texto, imagem, código) a partir de instruções em linguagem natural. | Microsoft Learn / Leader's Guide |
| Machine Learning (Aprendizado de Máquina) | Parte da IA em que modelos aprendem padrões a partir de muitos dados, sem serem programados regra por regra. | Leader's Guide |
| Cinco Pilares do Sucesso em IA | Estrutura de prontidão: estratégia de negócio, tecnologia e dados, estratégia e experiência em IA, organização e cultura, governança. | Microsoft Cloud Blog / Leader's Guide |
| AI Strategy Roadmap | Modelo de maturidade para levar a organização de testes isolados a um progresso repetível e governado. | Microsoft Cloud Blog / Leader's Guide |
| Governança de IA | Conjunto de controles, processos e responsabilidades para orientar privacidade, segurança e uso ético da IA. | Microsoft Cloud Blog / NIST AI RMF |
| IA Responsável | Princípios e práticas para que a IA seja ética, justa, transparente e centrada nas pessoas. | Microsoft Learn / NIST AI RMF |
| Gestão de Riscos de IA | Atividades para mapear, medir, gerenciar e mitigar possíveis danos da IA ao longo de todo o ciclo de vida. | NIST AI RMF |
| IA Confiável (Trustworthy AI) | Sistema de IA que atende a critérios como validade, segurança, resiliência, transparência, privacidade e justiça. | NIST AI RMF |
| Explicabilidade e Interpretabilidade | Explicabilidade mostra como o sistema chegou ao resultado; interpretabilidade ajuda o usuário a entender o que o resultado significa. | NIST AI RMF |
| Modelo Operacional de IA | Definição de como as capacidades e equipes de IA são organizadas e integradas nas áreas da empresa. | Leader's Guide / Microsoft Cloud Blog |
| Ciclo de Vida da IA | Fases da IA do planejamento e coleta de dados até implantação, operação e monitoramento. | NIST AI RMF |
| TEVV | Teste, Avaliação, Verificação e Validação: checagens contínuas em todo o ciclo de vida para garantir qualidade e conformidade. | NIST AI RMF |
| Viés Prejudicial (Harmful Bias) | Desvios vindos de dados não representativos, erros estatísticos ou preconceitos que geram resultados injustos. | NIST AI RMF |
| RAG (Retrieval-Augmented Generation) | Técnica que conecta o modelo a fontes de dados da empresa para gerar respostas mais precisas e atuais. | Microsoft Learn |

### 4.3 Prompts reutilizáveis para revisão

1. **Resumo com rastreabilidade**
   ```
   Resuma [TEMA] em 5 tópicos, citando de qual fonte vem cada ponto.
   ```
2. **Explicar para um público específico**
   ```
   Explique [CONCEITO] como se eu fosse um gestor sem formação técnica, com um exemplo prático e em até [N] parágrafos.
   ```
3. **Glossário com fonte**
   ```
   Crie um glossário em tabela com [N] termos sobre [TEMA], com colunas: termo, definição simples e fonte (uma única fonte por termo).
   ```
4. **Comparar conceitos**
   ```
   Monte uma tabela comparando [A] e [B]: definição, quando usar e riscos, citando as fontes.
   ```
5. **Checar viés das fontes**
   ```
   Quais afirmações das fontes valem para qualquer empresa e quais dependem de produtos de um fornecedor específico?
   ```
6. **Perguntas de revisão**
   ```
   Crie 10 perguntas de múltipla escolha sobre [TEMA] com gabarito e justificativa baseada nas fontes.
   ```
7. **Lacunas**
   ```
   O que as fontes NÃO respondem sobre [TEMA]? Liste os pontos que exigiriam outras referências.
   ```
8. **Plano de ação**
   ```
   Com base nas fontes, monte um plano de 30 dias para um líder iniciar a adoção de IA na sua equipe.
   ```

---

## 5. Conclusão

Este projeto me mostrou que liderar a adoção de IA depende tanto de pessoas, cultura e governança quanto de tecnologia. Na parte prática com o NotebookLM, aprendi que o prompt melhora bastante quando eu defino o formato, o público e a forma de citar as fontes, e que a checagem manual das citações continua necessária. Como quatro das cinco fontes são da Microsoft, numa próxima curadoria eu incluiria mais fontes independentes para equilibrar o ponto de vista.

---

## Fontes

Todas as fontes listadas na seção 2 são de acesso aberto.
