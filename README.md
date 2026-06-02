# 📈 Projeto: Previsão de Preços de Ações no Setor de Tecnologia

Este projeto foi desenvolvido com o objetivo de construir, avaliar e comparar modelos de **Machine Learning** e **Deep Learning** para a previsão de preços de ações de grandes empresas do setor tecnológico. Utilizando quatro datasets distintos, o projeto busca gerar insights preditivos robustos para apoiar a tomada de decisão no mercado financeiro.

---

## 🎯 Objetivo Geral

Desenvolver e avaliar modelos preditivos para ações de tecnologia, identificando padrões temporais, correlações de mercado e aplicando algoritmos avançados para prever comportamentos futuros dos ativos.

---

## 🔍 Objetivos Específicos e Etapas do Projeto

### 1. Análise Exploratória de Dados (EDA)
Realizar uma investigação profunda nos quatro datasets de ações tecnológicas para identificar padrões temporais, sazonalidade, volatilidade e correlações entre variáveis (preço, volume e indicadores técnicos).
- 📊 **Visualização:** Gráficos de séries temporais para análise do preço ao longo do tempo.
- 🔢 **Estatística:** Cálculo de estatísticas descritivas básicas (média, desvio padrão, mínimo e máximo).
- 🔗 **Correlações:** Análise de relações de mercado (ex: Preço × Volume; Ações da Apple × NVIDIA).
- 📉 **Indicadores Técnicos:** Incorporação de ferramentas analíticas como Média Móvel e RSI:

#### 🔹 Média Móvel (Moving Average)
Suaviza o gráfico de preços para ajudar a identificar a direção da tendência (alta ou baixa).
- **SMA (Simple Moving Average):** Média aritmética simples dos preços de fechamento.
- **EMA (Exponential Moving Average):** Atribui maior peso aos preços mais recentes.
> **Exemplo Prático (SMA 20):** Média dos últimos 20 pregões. Se o preço atual > SMA 20, indica tendência de alta; se preço atual < SMA 20, tendência de baixa.
> *Exemplo Numérico (5 dias: 100, 102, 101, 105, 108):*
> $$	ext{SMA 5} = rac{100 + 102 + 101 + 105 + 108}{5} = 103,2$$

#### 🔹 RSI (Relative Strength Index / Índice de Força Relativa)
Mede a velocidade e a força dos movimentos de preço, variando de 0 a 100 para identificar condições de sobrecompra ou sobrevenda.
- **RSI > 70:** Ativo sobrecomprado (alta probabilidade de correção/queda).
- **RSI < 30:** Ativo sobrevendido (alta probabilidade de repique/alta).
- **RSI [40, 60]:** Mercado neutro ou em tendência definida.
> **Exemplo:** NVIDIA com RSI em 85 (sobrecomprado) indica cautela; Apple com RSI em 25 (sobrevendido) aponta possível oportunidade de compra.

---

### 2. Pré-processamento de Dados
Preparação dos dados brutos aplicando técnicas específicas para séries temporais financeiras:
- Tratamento de valores ausentes (*missing values*).
- Normalização e escalonamento de recursos (*scaling*) para otimizar o treinamento dos modelos.

---

### 3. Desenvolvimento de Modelos de Machine Learning
Construção e comparação de diferentes abordagens algorítmicas divididas em dois cenários de modelagem:
1. **Regressão:** Prever o valor exato do preço de fechamento.
2. **Classificação:** Prever a direção do movimento do preço no dia seguinte (Alta ou Baixa).

#### 🤖 Regressão Linear
Modelo estatístico que busca mapear uma relação linear entre as variáveis de entrada (*features*) e o preço alvo.
$$	ext{Preço} = 45,3 + (0,0001 	imes 	ext{Volume}) + (1,25 	imes 	ext{RSI}) - (2,8 	imes 	ext{Média Móvel 20})$$

#### 🌲 Random Forest
Algoritmo de *Ensemble Learning* que combina múltiplas árvores de decisão para gerar predições mais robustas e evitar *overfitting*.
- Cria várias árvores usando subconjuntos aleatórios de dados e variáveis.
- Combina os resultados por **média** (regressão) ou **votação majoritária** (classificação).
> **Exemplo de Classificação (NVIDIA):** Se 68 árvores votam em "Subida" e 32 em "Queda", o resultado final do modelo será a tendência de **Subida**.

---

### 4. Avaliação e Validação de Desempenho
Análise comparativa rigorosa do desempenho dos modelos através de métricas de mercado nos quatro datasets:

| Tipo de Problema | Métricas Utilizadas | Descrição |
| :--- | :--- | :--- |
| **Regressão** | **RMSE** (Root Mean Squared Error) | Penaliza erros maiores elevando-os ao quadrado antes da média. |
| | **MAE** (Mean Absolute Error) | Média das diferenças absolutas entre o real e o previsto. |
| | **MAPE** (Mean Absolute Percentage Error) | Erro percentual médio em relação ao valor real da ação. |
| **Classificação**| **Acurácia, Precisão e Recall** | Medem a taxa de acerto geral, a assertividade dos sinais e a sensibilidade do modelo. |

---

### 5. Geração de Insights de Mercado
Extração de conhecimento estratégico fundamentado nos resultados operacionais, focando em eventos macro e micro do ecossistema de tecnologia, tais como:
- Impactos de notícias de Inteligência Artificial (IA).
- Lançamentos de produtos de grande porte e ciclos de inovação tecnológica.

---

### 6. Benchmarking Acadêmico e Literatura
Comparação dos resultados práticos obtidos neste ecossistema com abordagens consolidadas na literatura científica de finanças quantitativas, discutindo limitações, desafios da IA no mercado de ações e direções futuras.

---

## 🛠️ Tecnologias e Ferramentas Propostas
- **Linguagem:** Python 🐍
- **Análise e Manipulação:** Pandas, NumPy
- **Visualização:** Matplotlib, Seaborn, Plotly
- **Machine Learning:** Scikit-Learn
- **Deep Learning:** TensorFlow / Keras ou PyTorch

---
*Este repositório está sob constante desenvolvimento para fins acadêmicos e de pesquisa quantitativa.*
