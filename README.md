# Previsão de Demanda Mensal com Features de Lag

Este projeto utiliza dados de pedidos, produtos e preços para prever a demanda mensal de produtos por fornecedor, utilizando aprendizado de máquina com validação temporal e features de atraso (lags).

## 📂 Estrutura dos Dados

- `orders_2.csv`: informações dos pedidos, incluindo data.
- `orders_products_2.csv`: relação entre pedidos e produtos com data do preço.
- `prices_2.csv`: preços unitários dos produtos por ID.

## ⚙️ Etapas do Pipeline

1. **Carregamento e merges** dos datasets para consolidar os dados por produto e mês.
2. **Engenharia de atributos** com criação de variáveis de lag (demanda do mês anterior e dois meses atrás).
3. **Validação temporal** com `TimeSeriesSplit` para avaliar a performance em séries temporais.
4. **Modelagem preditiva** com:
   - Ridge Regression
   - Random Forest Regressor
   - HistGradientBoosting Regressor
5. **Avaliação com MAE** e seleção do melhor modelo.
6. **Previsão futura** da demanda para o próximo mês baseado nas features de lag dos dois meses anteriores.

## 🧪 Tecnologias e Bibliotecas

- Python 3.x
- Pandas
- scikit-learn
- TimeSeriesSplit
- Pipeline de modelagem
- Métrica MAE

- ---

📌 Projeto desenvolvido com a colaboração do Professor da Unichristus: **Pedro Bandeira** na etapa de imersão do Programa Residência em TIC-20 - Capacita Brasil/C-Jovem como parte de portfólio em Ciência de Dados com foco em previsão temporal baseada em lags.
