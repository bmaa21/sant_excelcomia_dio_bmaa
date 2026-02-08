# sant_excelcomia_dio_bmaa_lab1
Lab1 DIO Bootcamp Santander Excel com IA: Criando uma Ferramenta de Controle de Investimentos com Excel

# 🎯 **Objetivo do Aplicativo**
O aplicativo foi desenvolvido para **simular cenários de investimento focados em Fundos Imobiliários (FIIs)**, utilizando como base:
*   o **perfil do investidor** (Conservador, Moderado ou Agressivo)
*   a **composição recomendada de tipos de FII** para cada perfil
*   valores e parâmetros financeiros inseridos pelo usuário

A solução responde às principais perguntas de negócio relacionadas ao acúmulo de patrimônio e renda passiva, tais como:

*   **Quanto preciso investir por mês?**
*   **Qual patrimônio posso alcançar em 2, 5, 10, 20 ou 30 anos?**
*   **Qual será meu dividendo mensal estimado no futuro?**
*   **Como deve ser distribuído meu aporte mensal entre os diferentes tipos de FII conforme meu perfil?**

O app funciona como um **laboratório de investimentos**, permitindo ao usuário testar cenários e visualizar projeções reais com base em juros compostos e na alocação recomendada do portfólio.

***

# 📊 **Como o app responde às perguntas de negócio**

## ✔ **1. Simulação de patrimônio futuro**

A aba *Cenários* calcula:

*   Patrimônio acumulado
*   Dividendos mensais estimados

… para prazos como **2, 5, 10, 20 e 30 anos**, usando:

*   investimento mensal
*   taxa de rendimento mensal
*   juros compostos

## ✔ **2. Cálculo da renda passiva**

O app estima **dividendos mensais** futuros com base na rentabilidade selecionada.

## ✔ **3. Sugestão de alocação por tipo de FII**

Com base no perfil do investidor, o sistema usa a tabela da aba *perfil\_fii* para sugerir quanto do aporte mensal deve ir para:

*   Papel
*   Tijolo
*   Híbridos
*   FOFs
*   Desenvolvimento
*   Hotelaria

Exemplo para perfil Conservador (extraído do arquivo):

| Tipo de FII | % sugerido | Valor  |
| ----------- | ---------- | ------ |
| Papel       | 30%        | R$ 60  |
| Tijolo      | 50%        | R$ 100 |
| Híbridos    | 10%        | R$ 20  |
| FOFs        | 10%        | R$ 20  |
| Demais      | 0%         | 0      |

Isso forma uma **carteira recomendada automaticamente**.

***

# ⚙️ **Descrição da Seção “Configurações”**

A seção **Configurações** é o coração da simulação. Ali o usuário informa os parâmetros que personalizam todos os cálculos.

### A seção inclui:

### **1. Salário**

Valor que pode ser usado para calcular percentuais de recomendação (ex: 30% do salário).

### **2. Rendimento da carteira**

Taxa mensal estimada dos FIIs escolhidos.  
Exemplo no arquivo: `0,006` (0,6% ao mês).

### **3. Sugestão de investimento (% do salário)**

Define quanto do salário o investidor deveria destinar mensalmente a FIIs.

### **4. Investimento mensal**

Valor que o usuário planeja investir todos os meses.

### **5. Por quantos anos?**

Horizonte do investimento utilizado nos cálculos do patrimônio futuro.

### **6. Taxa de rendimento mensal**

Taxa usada nas simulações (juros compostos).  
Ex: `0,010789` (aprox. 1,07% ao mês).

### **7. Patrimônio acumulado**

Resultado calculado automaticamente com base nos parâmetros.

### **8. Dividendos mensais**

Estimativa futura da renda passiva ao final do período selecionado.

***

# 🧭 **Resumo da lógica do App**

1.  O usuário preenche os parâmetros em **Configurações**.
2.  O app calcula patrimônio projetado e dividendos com **juros compostos**.
3.  O usuário seleciona seu **perfil**.
4.  O app busca na tabela *perfil_fii* quais percentuais usar.
5.  Com isso, distribui automaticamente o investimento mensal por categoria de FII.
6.  Os resultados são exibidos nas seções **Cenários** e **Carteira Recomendada**.
***
