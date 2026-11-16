# Renda Variável vs. Renda Fixa no Brasil (2010–2025)

### Análise histórica de retorno e inflação | MVP — PUC-Rio

Este projeto investiga o desempenho de uma carteira formada por cinco grandes empresas brasileiras em comparação com a Selic e a inflação (IPCA), entre janeiro de 2010 e dezembro de 2025.

O estudo foi desenvolvido como parte da pós-graduação em **Ciência de Dados e Analytics da PUC-Rio**, na sprint de Análise de Dados e Boas Práticas.

## Objetivo

Responder a duas perguntas:

- Uma carteira de ações de grandes empresas brasileiras teria superado o rendimento acumulado da Selic?
- Tanto a carteira quanto a Selic teriam conseguido preservar e aumentar o poder de compra do capital investido?

## Metodologia

Foi simulado um investimento inicial de **R$ 10.000**, distribuído igualmente entre cinco empresas selecionadas com base no ranking de valor de mercado da Bovespa ao final de 2009.

| Empresa | Ticker | Investimento inicial |
|---|---|---:|
| Petrobras | PETR4 | R$ 2.000 |
| Vale | VALE3 | R$ 2.000 |
| Itaú Unibanco | ITUB4 | R$ 2.000 |
| Bradesco | BBDC4 | R$ 2.000 |
| Ambev | ABEV3 | R$ 2.000 |

A carteira foi mantida sem rebalanceamento ao longo do período.

Foram utilizados preços históricos ajustados como aproximação do retorno total das ações, considerando os efeitos de proventos e eventos corporativos. A Selic foi utilizada como referência hipotética de capitalização diária, enquanto o IPCA permitiu avaliar o impacto da inflação sobre os resultados.

A análise também incluiu estatísticas descritivas, visualizações e três investigações de pré-processamento: tratamento de valores extremos, cobertura histórica dos ativos e eventos corporativos.

## Resultados

### Patrimônio acumulado após 16 anos

| Alternativa | Valor final | Rentabilidade nominal | Rentabilidade real |
|---|---:|---:|---:|
| Carteira de ações | R$ 40.257,94 | +302,58% | +64,09% |
| Selic | R$ 44.109,10 | +341,09% | +79,79% |
| Inflação (IPCA) | R$ 24.533,87 | +145,34% | — |

*Valores brutos, sem impostos ou custos operacionais. A comparação utiliza os resultados da simulação original; uma verificação posterior identificou pequena diferença no recálculo da Selic, sem impacto nas conclusões.*

**Principal resultado:** a Selic superou a carteira em aproximadamente R$ 3,85 mil, enquanto ambas apresentaram ganhos reais acima da inflação.

## Conclusões

O resultado chama atenção para a competitividade histórica da renda fixa no Brasil. Mesmo uma carteira formada por cinco grandes empresas não conseguiu superar a Selic no período analisado.

É importante destacar que as empresas foram selecionadas com base em seu valor de mercado no início do estudo, e não por critérios retrospectivos de rentabilidade ou distribuição de dividendos.

A análise também levanta uma reflexão sobre como o histórico de juros elevados no Brasil pode influenciar a atratividade relativa da renda fixa e da renda variável. Essa é uma questão que merece investigação adicional, não uma relação causal demonstrada pelo estudo.

Como possibilidade de expansão, seria interessante comparar os resultados com uma carteira selecionada retrospectivamente entre as ações de melhor desempenho, reconhecendo as limitações desse tipo de comparação.

## Tecnologias e fontes

**Tecnologias:** Python, Pandas, Matplotlib, Seaborn, Google Colab e GitHub.

**Fontes:** B3, Banco Central do Brasil, IBGE e Yahoo Finance.

## Acessar o projeto

**[Visualizar o notebook completo](Renda_Variável_vs_Renda_Fixa.ipynb)**

**[Abrir no Google Colab](https://colab.research.google.com/github/pedrohreisrj/mvp-renda-variavel-vs-selic/blob/main/Renda_Vari%C3%A1vel_vs_Renda_Fixa.ipynb)**

Os arquivos CSV utilizados estão disponíveis na pasta `dados/tratados`.

## Limitações

O estudo considera uma carteira específica, sem rebalanceamento, e utiliza preços ajustados como aproximação do retorno total. Não foram considerados impostos, taxas, custos de transação ou indicadores de risco.

Parte do processamento foi realizada previamente em ambiente local, com os resultados disponibilizados em arquivos CSV para análise no notebook.

---

**Autor:** Pedro Reis  
**Formação:** Pós-graduação em Ciência de Dados e Analytics — PUC-Rio
