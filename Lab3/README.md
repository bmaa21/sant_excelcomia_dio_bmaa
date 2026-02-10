# sant_excelcomia_dio_bmaa_lab3
Lab3 DIO Bootcamp Santander Excel com IA: Criando um Dashboard de Vendas do Xbox com Excel
# **📝 Resumo da Análise da Base de Dados**
Ao analisar a base fornecida para o projeto, identifiquei que as assinaturas presentes — Xbox Game Pass, EA Play Season Pass e Minecraft Season Pass — eram totalmente independentes entre si.
Embora estivessem listadas na mesma tabela, cada uma possuía:

*   lógica de compra diferente,
*   valores distintos,
*   e principalmente, periodicidades não relacionadas.

A periodicidade (Monthly, Annual, Quarterly) se aplicava somente ao Xbox Game Pass, e não aos Season Pass adicionais. Portanto, utilizar esse filtro para segmentar EA Play ou Minecraft geraria uma relação falsa e distorceria a interpretação das métricas.

# **🔧 Correção Aplicada**
Para garantir coerência analítica, precisão dos KPIs e uma experiência mais intuitiva para o usuário, as visões foram separadas em módulos independentes dentro do app.
A correção consistiu em:

*   Manter periodicidade e tipo de plano apenas no módulo Xbox Game Pass.
*   Criar uma visão própria para as assinaturas agregadas (EA Play e Minecraft), já que não dependem da periodicidade do Game Pass.
*   Construir indicadores e gráficos de forma isolada para cada categoria, evitando cruzamentos incoerentes.
*   Permitir que o usuário navegue entre as visões de maneira clara e segmentada.

Essa abordagem torna o dashboard mais fiel à estrutura real do negócio e segue boas práticas de BI, onde filtros só devem afetar métricas que pertencem àquela dimensão.

# **🎮 Descrição do App Desenvolvido**
XBOX Game Pass and Aggregated Subscriptions Dashboard
O aplicativo foi construído para oferecer uma visão completa e estruturada das assinaturas relacionadas ao ecossistema Xbox. Ele é dividido em três módulos principais, cada um refletindo um aspecto independente do negócio.

🟩 1. Visão Geral — Dashboard Consolidado
Apresenta os KPIs financeiros principais da plataforma, incluindo:

*   Gross Value: Soma total de receitas antes dos descontos.
*   Coupon Value: Total de descontos aplicados.
*   Total Value: Receita líquida após cupons.

Este módulo permite ter uma visão macro do impacto financeiro combinado de todos os produtos.

🟦 2. Xbox Game Pass — Assinaturas Base
Esta visão concentra exclusivamente os dados referentes à assinatura principal do Xbox, incluindo:

*   Valor total arrecadado com o Game Pass.
*   Quantidade total de assinantes.
*   Quantidade de assinantes apenas do Game Pass (sem add-ons).
*   Distribuição por tipo de plano (Core, Standard, Ultimate).
*   Filtro funcional por periodicidade (Annual, Monthly, Quarterly).
*   Análise de Auto Renew (Yes/No).

A lógica dessa seção corresponde fielmente ao modelo de assinatura recorrente do serviço.

🟧 3. Aggregated Subscriptions — EA Play e Minecraft
Nesta seção estão concentradas as assinaturas que funcionam como add‑ons, sem relação com o tipo de plano ou periodicidade do Xbox Game Pass.
KPIs incluídos:

*   Gross Value EA Play Season Pass
*   Gross Value Minecraft Season Pass
Distribuição de assinantes entre:

*   Only Minecraft
*   Only EA
*   Both
*   None



Essa visão permite entender o comportamento de compra dos usuários nesses produtos complementares.

# **✔️ Conclusão**
A separação das visões não só está correta, como fortalece a fidelidade analítica do modelo.
O dashboard final:

*   respeita a independência das assinaturas,
*   evita filtros inconsistentes,
*   organiza os dados de forma intuitiva,
*   e entrega uma experiência profissional de navegação e leitura.
