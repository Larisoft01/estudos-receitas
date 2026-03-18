# estudos-receitas

#  Cozinhando na Juventude — Caderno Temático com NotebookLM

> **Projeto prático da DIO** | Explorando Inteligência Artificial como ferramenta de aprendizagem ativa

---

##  Contexto e Objetivos

### Por que esse tema?

Sair da casa dos pais, morar sozinho pela primeira vez, dividir república… quem viveu sabe: a cozinha pode parecer um território desconhecido e intimidador. Muitos jovens adultos acabam recorrendo a delivery todos os dias, gastando mais do que deveriam e sem ter ideia do que colocam no prato.

A proposta deste caderno temático é simples e direta: **aprender a cozinhar de forma prática, econômica e sem medo**, usando receitas com poucos ingredientes acessíveis — o tipo de prato que qualquer pessoa consegue fazer no fogão de uma kitnet, com panelas básicas e orçamento de estudante.

### Objetivos de Estudo

| # | Objetivo |
|---|----------|
| 1 | Construir um repertório de receitas simples e versáteis para o dia a dia |
| 2 | Entender técnicas básicas de cozinha (refogar, cozinhar no vapor, assar) sem jargões complicados |
| 3 | Aprender sobre substituições de ingredientes para economizar ou adaptar ao que tem em casa |
| 4 | Organizar o conhecimento em um guia estruturado e reutilizável com ajuda do NotebookLM |
| 5 | Praticar engenharia de prompts para extrair o melhor de uma IA como ferramenta de estudo |

---

## 📚 Curadoria de Fontes

As fontes abaixo foram selecionadas por serem abertas, confiáveis e diretamente relevantes ao tema. Todas foram carregadas no NotebookLM para compor o caderno temático.

| # | Fonte | Tipo | Link |
|---|-------|------|------|
| 1 | **SESI — Cartilha de Alimentação Saudável para Jovens** | PDF gratuito | [sesi.org.br](https://www.sesi.org.br) |
| 2 | **Ministério da Saúde — Guia Alimentar para a População Brasileira (2ª ed.)** | PDF oficial | [bvsms.saude.gov.br](https://bvsms.saude.gov.br/bvs/publicacoes/guia_alimentar_populacao_brasileira_2ed.pdf) |
| 3 | **EMBRAPA — Culinária com ingredientes acessíveis e nutritivos** | Artigo/PDF | [embrapa.br](https://www.embrapa.br) |
| 4 | **SENAC — Técnicas Básicas de Cozinha (material didático público)** | PDF | [senac.br](https://www.senac.br) |
| 5 | **Instituto Akatu — Como cozinhar com menos desperdício** | Texto/Guia online | [akatu.org.br](https://www.akatu.org.br) |

>  **Critério de seleção:** Priorizei fontes brasileiras, de instituições públicas ou sem fins lucrativos, com linguagem acessível e foco em alimentação saudável com baixo custo.

---

##  Engenharia de Prompts e "Cicatrizes"

Esta seção documenta o processo real de interação com o NotebookLM — incluindo o que funcionou, o que não funcionou e o que aprendi no caminho.

---

###  Prompt 1 — Exploração inicial

**Prompt testado:**
```
O que essas fontes dizem sobre receitas simples para quem está aprendendo a cozinhar?
```

**Resposta obtida:**
O NotebookLM gerou um resumo geral com foco em alimentação saudável, mas as respostas foram muito genéricas. Ele citou capítulos do Guia Alimentar sem conectar diretamente com praticidade no dia a dia de jovens.

**Problema identificado (cicatriz):**
A pergunta era vaga demais. A IA não sabia se eu queria receitas em si, técnicas ou conceitos de nutrição.

**Lição aprendida:**
> Prompts abertos demais geram respostas enciclopédicas. É preciso delimitar o contexto e o perfil do usuário.

---

###  Prompt 2 — Refinamento com contexto

**Prompt testado:**
```
Considerando que o leitor é um jovem adulto de 18 a 25 anos morando sozinho pela primeira vez, 
sem experiência na cozinha e com orçamento limitado, quais são as técnicas culinárias mais 
básicas que ele deveria aprender primeiro, segundo os materiais do SENAC e do Guia Alimentar?
```

**Resposta obtida:**
Muito melhor! O NotebookLM destacou três técnicas: refogar cebola e alho como base de sabor, cozinhar ovos de diferentes formas e preparar arroz e feijão. As referências às fontes foram precisas.

**Problema identificado (cicatriz):**
A IA listou as técnicas mas não sugeriu uma ordem de aprendizado progressivo (do mais fácil para o mais complexo).

**Lição aprendida:**
> Pedir explicitamente uma "sequência lógica de aprendizado" ou "do básico ao intermediário" melhora muito a estrutura da resposta.

---

###  Prompt 3 — Pedindo progressão

**Prompt testado:**
```
Monte uma trilha de aprendizado culinário para iniciantes, em ordem do mais simples ao mais 
elaborado, usando apenas o que está descrito nas fontes carregadas. Cada etapa deve ter: 
nome da técnica, exemplo de prato e tempo médio de preparo.
```

**Resposta obtida:**
O NotebookLM gerou uma trilha com 5 etapas bastante úteis, com pratos reais e tempos estimados. A resposta foi organizada em formato de lista, fácil de transformar em um guia visual.

**Resultado:**
✅ Prompt funcionou bem. Guardei como template reutilizável (ver seção de prompts do Miniguia).

---

###  Prompt 4 — Glossário culinário

**Prompt testado:**
```
Crie um glossário com os 15 termos culinários mais importantes para um iniciante, 
extraídos das fontes disponíveis. Formato: termo em negrito + definição em 1 linha.
```

**Problema identificado (cicatriz):**
O NotebookLM incluiu alguns termos muito técnicos (como "brunoise" e "mise en place") que não apareciam nas fontes — ele completou com conhecimento próprio sem avisar. Precisei pedir explicitamente que usasse **apenas** o que estava nas fontes.

**Prompt corrigido:**
```
Crie um glossário com os 15 termos culinários mais importantes para um iniciante. 
Use APENAS termos que aparecem literalmente nas fontes carregadas. 
Indique ao lado de cada termo qual fonte o menciona.
```

**Lição aprendida:**
> No NotebookLM, é fundamental deixar claro quando você quer que a IA se limite às fontes. Sem isso, ela pode misturar conhecimento externo sem indicar claramente.

---

###  Prompt 5 — Substituições de ingredientes

**Prompt testado:**
```
Quais substituições de ingredientes são sugeridas nas fontes para reduzir custos sem 
perder valor nutricional? Liste em formato de tabela: ingrediente original | substituto | motivo.
```

**Resposta obtida:**
Excelente resultado. A tabela foi gerada com precisão, com base principalmente no Guia Alimentar e no material da EMBRAPA. Muito útil para quem está com orçamento apertado.

---

##  Miniguia de Estudo — Resultado Final

---

###  Resumos Estruturados

#### Módulo 1 — Por onde começar (Semana 1–2)

A base de qualquer cozinheiro iniciante está em três preparações: **ovos**, **arroz** e **macarrão**. Esses ingredientes são baratos, versáteis e ensinam as técnicas mais fundamentais da cozinha — controle de fogo, tempo de cozimento e temperamento básico.

**Receitas-âncora:**
- Ovo mexido simples (5 min) — aprende controle de calor
- Arroz branco soltinho (20 min) — aprende proporção água/cereal
- Macarrão ao alho e azeite (15 min) — aprende refogar e finalizar

---

#### Módulo 2 — Construindo sabor (Semana 3–4)

O segredo do sabor na cozinha brasileira está no **refogado**: cebola + alho + azeite em fogo médio. A partir daí, qualquer proteína ou legume pode se transformar num prato digno.

**Receitas-âncora:**
- Frango desfiado refogado (25 min)
- Feijão com tempero caseiro (30 min com feijão em lata)
- Omelete de legumes (10 min)

---

#### Módulo 3 — Refeições completas com poucos ingredientes (Semana 5–6)

Com domínio dos módulos anteriores, é possível montar pratos completos com proteína + carboidrato + vegetal usando no máximo 5 ingredientes.

**Receitas-âncora:**
- Arroz com frango e cenoura (uma panela só)
- Macarrão com atum e tomate
- Batata assada recheada com cream cheese
- Sopa de legumes com caldo de frango

---

###  Glossário de Conceitos Essenciais

| Termo | Definição |
|-------|-----------|
| **Refogar** | Cozinhar ingredientes em pouca gordura em fogo médio-alto, mexendo constantemente |
| **Temperar** | Adicionar sal, pimenta e outros condimentos para realçar o sabor natural do alimento |
| **Al dente** | Ponto do macarrão em que está cozido mas ainda firme ao morder |
| **Redonar** | Cobrir o fundo da panela com água ou caldo para soltar o que grudou, aproveitando o sabor |
| **Branquear** | Mergulhar o alimento em água fervente por poucos minutos e depois em água gelada (preserva a cor) |
| **Dourar** | Cozinhar até obter uma superfície dourada e levemente crocante |
| **Marinar** | Deixar o alimento de molho em temperos por um tempo antes de cozinhar |
| **Reduzir** | Deixar um líquido cozinhar até evaporar parte da água e concentrar o sabor |
| **Nada de fogão? Sem pânico** | Muitas receitas funcionam em micro-ondas: ovos, arroz (em recipiente com tampa), legumes |
| **Mise en place** | Preparar e organizar todos os ingredientes antes de começar a cozinhar |
| **Proteína** | Nutriente essencial presente em ovos, feijão, frango, atum — base de qualquer refeição |
| **Carboidrato complexo** | Fonte de energia de liberação lenta: arroz integral, macarrão, batata-doce |
| **Gordura boa** | Presente no azeite, abacate e oleaginosas — importante para saciedade |
| **Proporção** | Relação entre quantidades: arroz branco usa 1 xíc de arroz para 1,5 xíc de água |
| **Panela de pressão** | Utensílio que cozinha feijão em 20–25 min. Sem ela, use feijão em lata |

---

###  Prompts Reutilizáveis para Revisão Futura

Use os prompts abaixo em futuras sessões no NotebookLM ou em qualquer IA para continuar aprendendo sobre culinária para iniciantes:

---

** Prompt para gerar novas receitas com o que você tem em casa:**
```
Tenho estes ingredientes disponíveis: [liste aqui]. 
Com base nas fontes do caderno, sugira 2 receitas simples que eu consiga fazer em menos de 30 minutos. 
Informe o tempo de preparo e o número de porções.
```

---

** Prompt para revisar técnicas:**
```
Explique o passo a passo de como [técnica: ex: refogar / cozinhar feijão / fazer arroz] 
para alguém que nunca cozinhou. Use linguagem simples, sem termos técnicos, e destaque 
os erros mais comuns a evitar.
```

---

** Prompt para criar plano alimentar semanal:**
```
Com base nas receitas e técnicas apresentadas nas fontes, crie um plano alimentar para 
5 dias (almoço e jantar) para uma pessoa morando sozinha, com orçamento de R$150 por semana. 
Priorize reaproveitamento de ingredientes entre os dias.
```

---

** Prompt para substituições de emergência:**
```
Estou fazendo [nome da receita] mas não tenho [ingrediente]. 
Quais são as melhores substituições possíveis sem prejudicar muito o resultado final? 
Explique o impacto de cada substituição no sabor e na textura.
```

---

**Prompt para dúvidas de técnica:**
```
Qual a diferença entre [técnica A] e [técnica B]? 
Quando devo usar cada uma? Dê exemplos práticos com pratos simples.
```

---

## Ferramentas Utilizadas

- **[NotebookLM](https://notebooklm.google.com/)** — organização e análise das fontes com IA
- **GitHub** — repositório e documentação do projeto
- **Claude (Anthropic)** — apoio na estruturação do miniguia e engenharia de prompts

---

## Reflexão Final

Este projeto me mostrou que a IA não substitui o aprendizado — ela o **acelera e organiza**. O maior aprendizado não foi sobre cozinha, mas sobre como **fazer as perguntas certas**. Um prompt mal formulado gera uma resposta medíocre. Um prompt com contexto, perfil do usuário e formato desejado gera algo muito mais útil.

Para qualquer jovem adulto: cozinhar é uma habilidade de vida. E para qualquer profissional de tecnologia: saber usar IA como ferramenta de estudo é uma vantagem competitiva real.

---
