# 📘 Equações Bonfarianas de Growth e Produto

**Versão 1.1 – Framework Aberto, Prático e Evolutivo**

---

## O que são as Equações Bonfarianas?

As **Equações Bonfarianas de Growth e Produto** são um conjunto de modelos matemáticos abertos para planejar e operar crescimento de forma previsível e escalável.

Criadas por **Paulo Bonfá**, elas servem para transformar o "depende" em **respostas práticas e calculáveis**, permitindo decisões sobre:

- Quanto investir  
- Quanto cobrar  
- Quantos leads gerar  
- Qual CAC máximo pagar  
- Quando um canal está saturando  
- Como organizar o budget entre canais

---

## Por que esse framework existe?

- Evitar achismos no growth e nas vendas  
- Modelar o crescimento com inequações claras (valores máximos e limites operacionais)  
- Conectar marketing, vendas, produto e financeiro em um único sistema de decisão  

---

## Como funciona?

As Equações Bonfarianas funcionam como **sistema de inequações e planejamento reverso**.  
Você pode isolar qualquer variável:

- Budget  
- CPL ou CPA  
- Conversão  
- Ticket médio  
- Churn  
- LTV  
- Ponto de saturação da mídia  
- Alocação de orçamento multicanal

---

## Equações Principais e Variações

### 1 - Previsibilidade de Receita

Receita = (bg / CPL) × T × C × R

yaml
Copiar
Editar

| Variável | Isolamento |
|---|---|
| Budget (bg) | (Receita × CPL) / (T × C × R) |
| CPL máximo | (bg × T × C × R) / Receita |
| Conversão (T) | (Receita × CPL) / (bg × C × R) |
| Ticket (C) | (Receita × CPL) / (bg × T × R) |
| Retorno Composto (R) | (Receita × CPL) / (bg × T × C) |
| Leads (N) | bg / CPL ou Receita / (T × C × R) |

---

### 2 - Retorno Composto (RC)

Modelo discreto:

RC = Tempo de Contrato × (1 - churn)

nginx
Copiar
Editar

Modelo contínuo:

RC = 1 / ln(1 / (1 - churn))

yaml
Copiar
Editar

---

### 3 - LTV Efetivo

LTV = C × RC

yaml
Copiar
Editar

| Variável | Isolamento |
|---|---|
| C | LTV / RC |
| RC | LTV / C |

---

### 4 - CAC e Limite Máximo

Break-even:

CAC_limite = LTV

yaml
Copiar
Editar

Com margem:

CAC_máx = LTV × M

yaml
Copiar
Editar

---

### 5 - Payback Time

Payback = CAC / C

yaml
Copiar
Editar

---

### 6 - Saturação de Mídia (Logarítmica)

CPA(x) = a × ln(bx + 1)

yaml
Copiar
Editar

| Variável | Isolamento |
|---|---|
| x (investimento) | (e^(CPA/a) - 1) / b |

---

### 7 - Limite de CPA e Ponto de Saturação

x_máx = (e^(CPA_máx / a) - 1) / b

yaml
Copiar
Editar

---

### 8 - Orquestração Multicanal

∀ x_i: CPA_i(x_i) ≤ CPA_máx
∑ x_i = Budget total

yaml
Copiar
Editar

---

## Aplicações práticas

- SaaS e Assinaturas  
- Software House e projetos sob demanda  
- E-commerce com recompra  
- Infoprodutos e cursos  
- Startups B2B e B2C

---

## Exemplos de isolamento e uso

| Pergunta | Como resolve? |
|---|---|
| Quanto devo investir para gerar R$ 500k? | Isola o budget |
| Qual CPL máximo posso pagar? | Isola o CPL |
| Quantos leads preciso gerar? | Isola N |
| Como o churn impacta o LTV? | Simula com RC |
| Quando o CPA vai saturar? | Usa a curva log |
| Como distribuir orçamento entre canais? | Usa orquestração multicanal |

---

## Exercícios práticos

### Exercício 1 – Previsibilidade de Receita

Budget = R$ 10.000  
CPL = R$ 20  
Taxa de Conversão = 10%  
Ticket Médio = R$ 500  
RC = 12

**Quanto irá faturar?**

**Resolução:**

- Leads = 10.000 / 20 = 500  
- Clientes = 500 × 0,10 = 50  
- LTV = 500 × 12 = R$ 6.000  
- Receita = 50 × 6.000 = R$ 300.000

---

### Exercício 2 – CPL Máximo

Com meta de receita de R$ 240.000:

CPL_máx = (10.000 × 0,10 × 500 × 12) / 240.000 = R$ 20

yaml
Copiar
Editar

---

### Exercício 3 – Saturação de Mídia

Curva: CPA(x) = 10 × ln(0,001x + 1)

Investimento de R$ 10.000:

CPA(10.000) = 10 × ln(11) ≈ 10 × 2,397 = R$ 23,97

yaml
Copiar
Editar

---

### Exercício 4 – Orquestração Multicanal

| Canal | a | b |
|---|---|---|
| Meta Ads | 10 | 0,001 |
| Google Ads | 8 | 0,002 |

CPA máximo: R$ 25  
Budget total: R$ 20.000

**Alocação ótima:**

- Meta Ads: ~R$ 12.180  
- Google Ads: ~R$ 7.810

---

## Como contribuir

- Faça fork deste repositório  
- Abra issues ou PRs com melhorias  
- Proponha novas versões ou adaptações por setor  

---

## ⚖️ Licença

Creative Commons **CC BY-SA 4.0**: Uso livre, com atribuição e compartilhamento pela mesma licença.

---

## Contato

Criador: **Paulo Bonfá**  
[LinkedIn](https://www.linkedin.com/in/paulobonfa/)
[Instagram](https://www.instagram.com/obonfa/)
