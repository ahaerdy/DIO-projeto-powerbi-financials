# Relatório de Vendas e Lucro com Power BI

Este repositório apresenta o projeto final desenvolvido para o desafio **"Analisando Dados de um Dashboard de Vendas no Power BI"**, parte integrante do bootcamp de Engenharia de Dados com Python oferecido pela **NTT DATA** na plataforma **DIO**. O trabalho consiste na elaboração de um dashboard analítico estruturado para fornecer *insights* estratégicos sobre o desempenho comercial de uma organização fictícia, utilizando ferramentas avançadas de visualização e modelagem de dados.

## Descrição do Projeto

O objetivo central deste projeto foi a construção de um relatório dinâmico composto por três páginas distintas, cada uma focada em diferentes dimensões de análise de negócios. A base de dados utilizada, denominada `financials.csv`, contém registros detalhados de transações comerciais ocorridas entre os anos de 2013 e 2014. Através do uso do **Power BI Desktop**, os dados brutos foram transformados em informações visuais que permitem a identificação de padrões de consumo, rentabilidade geográfica e eficiência por segmento de mercado.

## Estrutura do Relatório

O dashboard foi organizado de forma lógica para facilitar a navegação e a compreensão dos indicadores-chave de desempenho (KPIs). A tabela abaixo detalha a composição de cada uma das três páginas desenvolvidas:

| Página | Foco da Análise | Elementos Visuais Principais |
| :--- | :--- | :--- |
| **Página 1** | Vendas por Produtos e Segmentos | Gráfico de setores para participação de vendas por produto; gráfico de área para análise de preço médio; e gráfico de colunas agrupadas para evolução temporal por segmento. |
| **Página 2** | Performance Geográfica e Financeira | Gráfico de rosca para distribuição de vendas por país; gráfico de colunas para lucro mensal; e gráfico de barras para comparação de volume de vendas entre nações. |
| **Página 3** | Análise Geoespacial e Lucratividade | Mapas de bolhas para distribuição de vendas e lucro por país; gráfico de pizza para lucro por segmento com funcionalidade de filtro interativo. |

### Detalhamento da Página 3 (Desenvolvimento Autônomo)

A terceira página do relatório foi concebida para explorar a dimensão geoespacial dos dados. Para esta análise, foi crucial a escolha do visual **Mapa de Bolhas** (em detrimento do mapa coroplético), pois ele permite que o **tamanho da bolha** seja diretamente proporcional à métrica analisada, facilitando a comparação visual entre regiões [1].

O principal *insight* gerado por esta página é a constatação de que **o maior volume de vendas não se traduz necessariamente no maior lucro** [2].

A página é composta por:
1.  **Mapa de Vendas:** Utiliza a localização por `Country` e define o tamanho da bolha pela `Soma de Sales`. Inclui uma **Dica de Ferramenta (Tooltip)** para exibir a `Soma de Units Sold` ao passar o mouse, oferecendo uma camada adicional de detalhe [1].
2.  **Mapa de Lucro:** Focado na `Soma de Profit`, permitindo a comparação visual direta com o mapa de vendas para identificar disparidades de rentabilidade.
3.  **Lucro por Segmento:** Gráfico de pizza que exibe a `Soma de Profit por Segment` (Government, Small Business, etc.), atuando como um filtro interativo para os mapas.

## Metodologia e Tecnologias

Para a execução deste projeto, utilizou-se o **Power BI Desktop** como ferramenta principal de Business Intelligence. O processo envolveu etapas de extração e carregamento de dados (ETL), seguidas pela aplicação de expressões **DAX** para a criação de medidas calculadas essenciais. A estrutura dos dados originais é composta por variáveis categóricas e numéricas, conforme descrito na tabela a seguir:

| Atributo | Descrição |
| :--- | :--- |
| **Segment** | Classificação do cliente (ex: Government, Small Business). |
| **Country** | Localização geográfica da venda. |
| **Product** | Identificação do item comercializado. |
| **Units Sold** | Volume quantitativo de itens vendidos. |
| **Sales / Profit** | Valores financeiros de faturamento bruto e lucro líquido. |
| **Date** | Registro temporal da transação. |

Este projeto demonstra a capacidade de sintetizar dados complexos em *dashboards* intuitivos, servindo como uma ferramenta de suporte à decisão para gestores e analistas de dados.

## Entrega do Projeto

Conforme as instruções da aula, o relatório final deve ser exportado e anexado ao repositório. As opções de entrega incluem:
- **PowerPoint:** Importação do relatório para o PowerPoint como suplemento, com modificações para apresentar cada página em um slide [3].
- **PDF:** Exportação do relatório em formato PDF [3].

---
*Projeto desenvolvido como parte do percurso de Engenharia de Dados com Python da NTT DATA na plataforma DIO.*
