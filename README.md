text

README.md

# Backtest de Carteira Recomendada em Python

Este projeto realiza o cálculo e a análise da cota diária de uma carteira de ações recomendada mensalmente, utilizando dados históricos de preços e pesos definidos por um algoritmo quantitativo.
O objetivo é reconstruir a rentabilidade da carteira ao longo do tempo e compará-la ao índice de Small Caps do Brasil, utilizando o ETF SMAL11 como proxy.

## Objetivo

Reconstruir a cota diária de uma carteira recomendada mensalmente

Calcular a rentabilidade diária da carteira a partir das ações e pesos recomendados

Avaliar o desempenho acumulado da carteira ao longo do tempo

Comparar o desempenho da carteira com o índice de Small Caps (SMAL11)

## Base de Dados

O projeto utiliza três conjuntos principais de dados:

1. Recomendações da Carteira

Contém:

- Data da recomendação

- Ticker da ação

- Peso da ação na carteira

As recomendações são atualizadas mensalmente. Caso um ativo deixe de ser recomendado em determinado mês, ele é considerado vendido para efeito de cálculo da rentabilidade.

2. Cotações das Ações

- Base histórica contendo:

- Datas de negociação

- Preços de fechamento ajustados (considerando eventos corporativos)

- Identificação do ticker

Esses dados permitem o cálculo do retorno diário de cada ativo.

3. Proxy de Mercado (SMAL11)

Os dados do ETF SMAL11 são utilizados como aproximação do índice de Small Caps do Brasil, permitindo a comparação direta de desempenho entre a carteira e o mercado.

## Metodologia

As principais etapas do projeto foram:

- Leitura e padronização das bases de dados

- Conversão e ordenação das datas em ordem cronológica

- Cálculo do retorno diário de cada ativo a partir do preço de fechamento ajustado

- Associação das cotações com as recomendações mensais da carteira

- Normalização dos pesos da carteira em cada data

- Cálculo do retorno diário ponderado da carteira

- Construção da cota diária acumulada da carteira

- Cálculo da cota acumulada do índice SMAL11

- Comparação entre carteira e índice ao longo do tempo

## Análises Realizadas

- Rentabilidade diária da carteira

- Evolução da cota acumulada da carteira

- Comparação gráfica entre a carteira e o índice SMAL11

- Avaliação do desempenho final da carteira em relação ao proxy de mercado 

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- yFinance
- Google Colab

## Reprodução
1) Clone o repositório
2) Instale as dependências listadas em requirements.txt
3) Execute o script em src/calculo_carteira.py
ou
4) Abra o notebook em notebooks/ e execute as células em sequência

## Observação

O projeto foi desenvolvido no Google Colab, mantendo a estrutura de diretórios do repositório para garantir reprodutibilidade e facilitar a avaliação do código e dos resultados.


