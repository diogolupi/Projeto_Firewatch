# 🔥 Painel de Análise de Incêndios Florestais no Brasil - 2024

Este projeto realiza uma **análise exploratória de dados** sobre incêndios florestais no Brasil durante os três primeiros trimestres de 2024. Ele combina uma **planilha estática em Excel** e um **painel interativo em Streamlit**, permitindo que os usuários explorem os dados e identifiquem padrões críticos que possam ajudar na **prevenção e controle de incêndios**.

---

## 📑 **Descrição do Projeto**

O projeto utiliza dados do [Fire Watch Brazil 2024](https://www.kaggle.com/datasets/mayaravalliero/fire-watch-brazil-2024/data?select=Dataset_FireWatch_Brazil_Q3_2024.csv), disponível no Kaggle, para monitorar indicadores climáticos e de risco de fogo em diferentes estados e municípios do Brasil. As variáveis analisadas incluem:
- **Dias sem chuva**: Média de dias consecutivos sem precipitação.
- **Precipitação (mm)**: Quantidade média de chuva no período analisado.
- **Risco de Fogo (%)**: Probabilidade de ocorrência de incêndios florestais.
- **FRP (Fire Radiative Power)**: Energia liberada pelos incêndios, indicando a intensidade do evento.

A aplicação desenvolvida oferece duas abordagens de análise:
1. **Painel Interativo com Streamlit**: Permite explorar os dados de forma dinâmica e personalizada.
2. **Planilha Excel**: Fornece uma visão rápida e organizada para análises mais simples.

---

## 📦 **Bibliotecas Utilizadas**

- **NumPy**: Manipulação de arrays e cálculos numéricos.
- **Pandas**: Manipulação e transformação de dados tabulares.
- **Matplotlib**: Criação de gráficos para a visualização de dados.
- **Seaborn**: Gráficos estatísticos com visualizações elegantes.
- **Statsmodels**: Modelagem e testes estatísticos.
- **SciPy**: Cálculo de correlações estatísticas e outras funções científicas.
- **Unidecode**: Normalização de texto, removendo acentos e caracteres especiais.
- **Streamlit**: Desenvolvimento do painel interativo acessível no navegador.

---

## 🛠️ **Funcionalidades do Painel**

1. **Filtros por Estado e Município**:
   - O usuário pode escolher o **estado** e **município** de interesse.
   - Os dados filtrados são exibidos em uma **tabela centralizada** para facilitar a navegação.

2. **Visualização Interativa dos Dados**:
   - **Precipitação Média ao Longo do Tempo**: Gráfico de linha que mostra como a quantidade de chuva variou ao longo do período.
   - **Risco Médio de Fogo**: Gráfico que apresenta a evolução da probabilidade de incêndios.
   - **FRP Médio**: Mede a intensidade dos incêndios, com valores mais altos indicando eventos mais severos.

3. **Documentação e Explicações**:
   - O painel inclui uma seção de **explicação** sobre as variáveis e os gráficos apresentados.

---

## 🧹 **Tratamento dos Dados**

1. **Valores Ausentes**:
   - Valores nulos na coluna `bioma` foram preenchidos como **"Pampa"** para o município de **LAGOA DOS PATOS** e com **"Não identificado"** para os demais.
   - Valores ausentes em **`avg_frp`** foram preenchidos com a **média** dos valores existentes.

2. **Normalização de Texto**:
   - Os nomes de estados e municípios foram convertidos para **minúsculas** e tiveram os **acentos removidos**, para evitar inconsistências na filtragem.

3. **Conversão de Tipos de Dados**:
   - A coluna `data` foi convertida para o formato **datetime** para facilitar a análise temporal.
