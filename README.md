# Análise de Churn de Clientes

**Objetivo:**

Este projeto tem como objetivo analisar os dados de churn de clientes de uma empresa (não especificada) para identificar os principais fatores que contribuem para o cancelamento de serviços. O objetivo é fornecer insights acionáveis para que a empresa possa implementar estratégias de retenção de clientes mais eficazes.

**Linguagem de Programação:**

*   **Python:** A linguagem principal utilizada para a análise de dados, manipulação dos dados, criação de visualizações e geração de insights.

**Bibliotecas:**

*   **Pandas:** Utilizada para manipulação e análise de dados tabulares. Permite carregar, limpar, transformar e organizar os dados em DataFrames, facilitando a análise exploratória.
*   **Plotly:** Utilizada para criação de gráficos interativos e visualizações avançadas. Permite gerar gráficos de dispersão 3D, gráficos de barras e gráficos de pizza com recursos de zoom, rotação e tooltips.
*   **Matplotlib:** Utilizada para criação de gráficos estáticos e visualizações básicas. Permite gerar histogramas, boxplots e gráficos de barras.
*   **Seaborn:** Construída sobre o Matplotlib, oferece uma interface de alto nível para criar gráficos estatísticos atraentes e informativos.
*   **IPython.display:** Permite exibir os gráficos do Folium (mapas) diretamente no Colab, sem precisar salvar em arquivos externos.
*   **Folium:** Permite criar mapas interativos com marcadores e mapas de calor para visualizar dados geográficos.
*   **json_normalize:** Facilita o processo de converter arquivos JSON em formato tabular, melhorando a manipulação dos dados.
*   **ast:** Auxilia na conversão de strings para listas.

**Ambiente de Desenvolvimento (IDE):**

*   **Google Colaboratory (Colab):** Plataforma de desenvolvimento em nuvem que permite executar código Python em um ambiente Jupyter Notebook, com acesso gratuito a recursos de computação e bibliotecas populares de ciência de dados.

**Dados:**

Os dados utilizados neste projeto são provenientes de um arquivo JSON. Este arquivo contém informações sobre clientes, seus planos de serviço, informações de contato e histórico de cobranças. As colunas relevantes para a análise incluem:

*   `customerID`: Identificador único do cliente.
*   `Churn`: Indica se o cliente cancelou ou não o serviço.
*   `gender`: Gênero do cliente.
*   `SeniorCitizen`: Indica se o cliente é idoso (0 ou 1).
*   `Partner`: Indica se o cliente tem um parceiro.
*   `Dependents`: Indica se o cliente tem dependentes.
*   `tenure`: Tempo de contrato do cliente em meses.
*   `PhoneService`: Indica se o cliente tem serviço telefônico.
*   `MultipleLines`: Indica se o cliente tem múltiplas linhas telefônicas.
*   `InternetService`: Tipo de serviço de internet do cliente.
*   `OnlineSecurity`: Indica se o cliente tem segurança online.
*   `OnlineBackup`: Indica se o cliente tem backup online.
*   `DeviceProtection`: Indica se o cliente tem proteção de dispositivo.
*   `TechSupport`: Indica se o cliente tem suporte técnico.
*   `StreamingTV`: Indica se o cliente tem streaming de TV.
*   `StreamingMovies`: Indica se o cliente tem streaming de filmes.
*   `Contract`: Tipo de contrato do cliente.
*   `PaperlessBilling`: Indica se o cliente recebe fatura online.
*   `PaymentMethod`: Método de pagamento do cliente.
*   `Charges.Monthly`: Valor das cobranças mensais do cliente.
*   `Charges.Total`: Valor total das cobranças do cliente.
*   `lat`: latitude
*   `lon`: longitude

**Etapas da Análise:**

1.  **Carregamento e Limpeza dos Dados:**
    *   Carregamento dos dados a partir do arquivo JSON utilizando a biblioteca Pandas.
    *   Desaninhamento das colunas `customer`, `phone`, `internet` e `account` utilizando a função `json_normalize`.
    *   Tradução dos nomes das colunas e dos valores das colunas categóricas do inglês para o português.
    *   Tratamento de valores ausentes e remoção de linhas duplicadas.
    *   Correção do tipo de dados da coluna `Charges.Total` para float.
    *   Criação da coluna `Contas_Diarias` para calcular o valor diário da conta de cada cliente.
2.  **Análise Exploratória dos Dados (AED):**
    *   Análise da distribuição do churn.
    *   Análise do churn por gênero, tipo de contrato e método de pagamento.
    *   Análise da relação entre as variáveis numéricas (tempo de contrato e cobranças totais) e o churn.
    *   Identificação dos serviços com maior taxa de cancelamento quando o cliente os utiliza.
3.  **Visualização dos Resultados:**
    *   Criação de gráficos de barras, histogramas, boxplots e gráficos de pizza para visualizar os resultados da análise exploratória.
    *   Utilização do Plotly para criar gráficos interativos que permitem explorar os dados com mais detalhes.
    *   Utilização do Folium para criar mapas de dispersão e mapas de calor para visualizar dados geográficos.
4.  **Geração de Insights:**
    *   Identificação dos principais fatores que contribuem para o churn.
    *   Formulação de recomendações para a empresa com base nos insights obtidos.

**Conclusões:**

Este relatório resume as principais etapas e resultados da análise de churn de clientes. Os insights obtidos podem ser usados para desenvolver estratégias de retenção mais eficazes e reduzir o churn, aumentando a receita e a rentabilidade da empresa. As visualizações interativas
