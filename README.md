# Relatório Financeiro de Vendas – Power BI

Projeto desenvolvido como parte do **bootcamp da DIO: Klabin - Excel e Power BI Dashboards**.

## 📌 Descrição do Projeto
Relatório financeiro construído a partir da base fictícia **"financias"**, com o objetivo de analisar vendas, unidades comercializadas e lucratividade por produto, país, período e segmento. O foco do projeto foi criar um relatório claro, responsivo e orientado ao consumo rápido de informação pelo usuário final.

---

## 🎯 Objetivo
Criar um relatório de vendas completo e navegável que permita a diferentes tipos de usuários (gestores, analistas e stakeholders) explorar rapidamente os principais indicadores e obter insights acionáveis.

---

## 🛠️ Ferramentas
- **Power BI Desktop**
- Modelagem de dados (medidas DAX)
- Técnicas de design para dashboards (disposição, cores, hierarquia)

---

## ✅ Pontos considerados na criação
1. **Disposição dos visuais** pensando em como o usuário consome a informação (hierarquia e fluxo de leitura).
2. **Uso de cores** para manter identidade visual e destacar métricas relevantes.
3. **Página de Detalhes** com visão aprofundada conforme o desafio.
4. **Criação de medidas DAX** necessárias para suportar os visuais e filtros.

---

## 🧩 Estrutura do Relatório (Páginas)
O arquivo contém **4 páginas**:

1. **Home** – página inicial com título e link para a próxima página.
2. **Principal** – painel com as principais métricas e visuais de alto nível.
3. **Detalhes de Vendas** – análise detalhada por semestre, trimestre, mês e produto.
4. **TOP 3 e Segmentos** – mostra os TOP 3 produtos por vendas, TOP 3 por país e análises por segmento.

Cada página contém botões de navegação (ícone Home, setas avançar/voltar) para facilitar o fluxo.

---

## 📊 Visuais Principais
- **TOP 3 Produtos** (tabela/visual que destaca nome, quantidade e vendas).
- **Principais Países** (treemap e mapa, alternáveis).
- **Gráfico de Dispersão**: unidades vendidas vs vendas por mês (cada ponto representa um mês).
- **Visuais de Agrupamentos**: semestres, trimestres e segmentos agrupados.
- **Matriz** com valores de vendas por trimestre e por mês.
- **Cards** com métricas-chave: Total Sales, Total Units, Profit etc.
- **Botões de alternância de visual** (barra ↔ rosca, treemap ↔ mapa) para aproveitar espaço.

---

## 🧠 Medidas e Agrupamentos Criados
Algumas medidas e agrupamentos implementados:

- `TOP_3_PRODUCT` – identifica os 3 produtos com maiores volumes de venda.
- `Total Sales` – soma das vendas (valor monetário).
- `Total Units` – soma das unidades vendidas.
- `Profit` – cálculo de lucro (quando aplicável).

Agrupamentos:
- **Semestres** – agrupa meses em 1º e 2º semestre por ano.
- **Segmentos Agrupados** – consolida categorias de produto em grupos maiores para análise.

---

## 🔍 Explicação detalhada: Gráfico de Dispersão (Buckets / Unidades vendidas)
Na página **Detalhes de Vendas** há um gráfico de dispersão que relaciona **Unidades Vendidas (eixo X)** com **Vendas (eixo Y)** por mês. Cada ponto do gráfico representa um mês inteiro, permitindo identificar padrões como:

- Meses com baixo volume (unidades) e baixa receita (pontos no canto inferior esquerdo).
- Meses com alto volume mas baixa receita (pontos à direita e abaixo), indicando possível queda no preço médio ou promoções.
- Meses com alto volume e alta receita (pontos à direita e acima), meses de melhor desempenho.

Esse enfoque ajuda a responder perguntas do tipo: "Quantos meses com vendas altas tiveram baixa receita média?" ou "Quais buckets concentram a maior parte do faturamento?".

---

## 📅 Por que é importante ter um filtro de data?
Um **filtro de data** é essencial em qualquer relatório temporal por vários motivos:

- **Contextualização**: permite ao usuário enxergar períodos específicos (ano, semestre, trimestre, mês) e comparar períodos distintos.
- **Performance**: ao limitar o intervalo de análise, o relatório carrega e calcula apenas o subconjunto de dados necessário, melhorando o desempenho.
- **Análises pontuais**: facilita análises ad-hoc como efeitos de campanhas, sazonalidade ou eventos específicos.
- **Reprodutibilidade**: ao aplicar um filtro, é possível reproduzir exatamente a mesma visão para validação ou apresentação.

Por isso, o relatório inclui um filtro de data em todas as páginas, com um botão para **limpar seleção** que devolve a visualização ao contexto global.

---

## ⚙️ Boas Práticas Aplicadas
- **Hierarquia visual**: disposição dos cards e gráficos conforme prioridade da informação.
- **Contraste e identidade visual**: paleta de cores consistente e contraste para legibilidade.
- **Alternância de visuais** para economizar espaço e fornecer múltiplas perspectivas sem poluir a página.
- **Otimização de performance**: evitar colunas calculadas desnecessárias, usar medidas DAX e ordenar carregamento dos elementos.

---

## ▶️ Como usar / Explorar
Arquivo do projeto: **[Sales Report 06-12-2025.pbix](https://github.com/gardguedes/relatorio_vendas_lucro)**

1. Abra o arquivo `.pbix` do projeto.
2. Comece pela **Home** e avance para **Principal** para ter uma visão geral.
3. Use o filtro de data para selecionar o período de interesse; limpe o filtro quando quiser voltar ao panorama total.
4. Na página **Detalhes de Vendas**, alterne os visuais de semestre/mês e observe os buckets no gráfico de dispersão.
5. Em **TOP 3 e Segmentos**, explore os produtos por país e segmento; use o gráfico de dispersão para ver variação mensal.

---

## 🧾 Conclusão
Este relatório combina modelagem de dados e boas práticas de design para entregar uma ferramenta analítica robusta e amigável. A inclusão de filtros, alternadores de visual e agrupamentos permite que diferentes audiências naveguem e encontrem respostas rapidamente — desde um executivo que precisa de um resumo até um analista que precisa de detalhes por mês e produto.
