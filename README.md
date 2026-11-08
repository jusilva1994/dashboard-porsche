# Porsche Sales Dashboard

## Sobre o projeto

Este projeto consiste em um dashboard interativo para análise de vendas de veículos da Porsche, desenvolvido para transformar os dados de vendas em informações visuais e facilitar a identificação de padrões, tendências e oportunidades de negócio.

O dashboard foi desenvolvido em **HTML e React, com o auxílio do ChatGPT**. A escolha do React permite estruturar uma interface dinâmica e interativa, com filtros e gráficos que se atualizam conforme a seleção do usuário.

Inicialmente, a ideia era utilizar o Canvas do ChatGPT para desenvolver e visualizar o dashboard diretamente na plataforma. Entretanto, como essa funcionalidade não está mais disponível, o projeto foi desenvolvido em HTML com React, mantendo a proposta de criar uma experiência visual e interativa.

## Objetivos do dashboard

O dashboard tem como principais objetivos:

- Analisar o desempenho geral das vendas.
- Identificar os modelos da Porsche com maior volume de vendas.
- Comparar o desempenho das vendas entre diferentes cidades.
- Identificar os anos de modelo com maior quantidade de vendas.
- Analisar a distribuição das vendas por forma de pagamento.
- Identificar padrões de sazonalidade ao longo do ano.
- Apresentar indicadores que auxiliem na tomada de decisões.

## Tratamento e qualidade dos dados

Durante a preparação da base de dados, foi identificado um problema em algumas células da coluna de datas: determinados registros estavam preenchidos com o valor `INVALID`, impedindo a utilização correta dessas informações nas análises temporais.

Para solucionar o problema, foi realizada uma comparação entre a planilha corrigida e a planilha original, utilizando o **Microsoft Copilot** como ferramenta de apoio. O objetivo foi recuperar as datas dos registros inválidos a partir dos dados originais e padronizá-las de acordo com o formato utilizado na base final.

Segundo a resposta fornecida pelo Copilot, o procedimento realizado foi:

> Comparei as duas planilhas e gerei uma versão com os registros que estavam como **INVALID** na coluna de data preenchidos a partir da planilha original, ajustando as datas inválidas para o formato sanitizado utilizado na planilha final.
>
> **Observação:** os campos marcados como `INVALID` correspondiam a datas inválidas ou mal formatadas na planilha original (por exemplo, 30/02, 31/04, 40º dia do mês etc.). Eles foram corrigidos para datas válidas mantendo o padrão `YYYY-MM-DD` usado no restante da planilha.

Após esse procedimento, foi utilizada a versão corrigida da planilha para a construção do dashboard.

Essa etapa demonstra a importância da qualidade dos dados antes da criação de indicadores e visualizações, além da aplicação de ferramentas de inteligência artificial para auxiliar na identificação e correção de inconsistências.

## Perguntas de negócio respondidas

O dashboard foi desenvolvido para responder às seguintes perguntas:

### 1. Quais são os modelos da Porsche mais vendidos?

Apresenta um ranking dos modelos com maior quantidade de vendas, permitindo identificar quais veículos possuem maior participação no volume comercializado.

### 2. Quais modelos são mais vendidos em cada cidade?

Permite comparar a preferência dos consumidores entre diferentes cidades e identificar quais modelos apresentam maior volume de vendas em cada localidade.

### 3. Qual ano de modelo apresenta o maior número de vendas?

Identifica os anos de modelo com maior quantidade de veículos vendidos, permitindo analisar a preferência dos consumidores em relação ao ano do veículo.

### 4. Qual é o faturamento total das vendas?

Apresenta o valor total das vendas registradas, possibilitando acompanhar o desempenho financeiro da operação.

### 5. Qual é o ticket médio das vendas?

Calcula o valor médio por veículo vendido, permitindo avaliar o valor médio das transações realizadas.

### 6. Qual é a forma de pagamento mais utilizada?

Apresenta a distribuição das vendas por método de pagamento, permitindo identificar as formas mais utilizadas pelos clientes.

### 7. Como as vendas se comportam ao longo dos meses?

Apresenta a evolução mensal das vendas, permitindo identificar períodos de maior e menor movimentação comercial.

### 8. Existe sazonalidade nas vendas?

Agrupa as vendas por mês do calendário, permitindo identificar possíveis padrões sazonais, como meses que concentram maior ou menor volume de vendas.

### 9. Quais cidades apresentam maior volume de vendas?

Permite comparar o desempenho comercial entre as cidades e identificar as localidades com maior participação nas vendas.

## KPIs apresentados

Os principais indicadores de desempenho (KPIs) do dashboard são:

| KPI | Descrição |
|---|---|
| **Total de vendas** | Quantidade total de veículos vendidos no período selecionado. |
| **Faturamento total** | Soma dos valores de todas as vendas realizadas. |
| **Ticket médio** | Valor médio das vendas, calculado pela divisão do faturamento total pela quantidade de veículos vendidos. |
| **Ano de modelo líder** | Ano de modelo com maior quantidade de veículos vendidos. |
| **Mês com mais vendas** | Mês que apresentou o maior volume de vendas. |
| **Mês com menos vendas** | Mês com menor volume de vendas, considerando os meses que possuem registros. |

## Filtros disponíveis

O dashboard possui filtros interativos que permitem segmentar as informações e realizar análises específicas.

- **Porsche Model:** filtra as vendas por modelo do veículo.
- **Model Year:** filtra os registros pelo ano do modelo.
- **City:** permite selecionar uma cidade específica.
- **Pay Method:** filtra as vendas de acordo com a forma de pagamento.
- **Período:** permite delimitar o intervalo de datas para análise.

Os gráficos e indicadores são atualizados conforme os filtros selecionados, permitindo explorar diferentes perspectivas dos dados.

## Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
|---|---|
| **HTML** | Estrutura da página e dos elementos do dashboard. |
| **CSS** | Estilização, organização visual e identidade do dashboard. |
| **JavaScript** | Tratamento dos dados e implementação das interações. |
| **React** | Construção da interface interativa e atualização dos componentes. |
| **ChatGPT** | Apoio na criação do código HTML, desenvolvimento da interface, implementação das funcionalidades e organização do projeto. |
| **Microsoft Copilot** | Apoio na comparação das planilhas e na correção das inconsistências encontradas nos campos de data. |

## Fonte de dados

O dashboard utiliza uma base de dados de vendas de veículos Porsche, contendo informações como:

- Identificação da venda;
- Data da venda;
- Modelo do veículo;
- Ano do modelo;
- Valor da venda;
- Cidade e estado;
- Forma de pagamento;
- Status da entrega.

A base utilizada possui **100 registros** e os valores monetários são apresentados em dólares americanos (USD), conforme a unidade utilizada nos dados de origem.

## Considerações finais

O projeto demonstra como a utilização de tecnologias de desenvolvimento web e ferramentas de inteligência artificial pode contribuir para a construção de soluções de Business Intelligence.

O Microsoft Copilot foi utilizado como apoio no tratamento e na correção dos dados, enquanto o ChatGPT auxiliou no desenvolvimento do HTML, na construção da interface, dos gráficos, dos indicadores e das funcionalidades interativas.

A proposta é demonstrar conhecimentos em análise de dados, tratamento de informações, indicadores de desempenho, visualização de dados e desenvolvimento de dashboards, transformando dados brutos em informações úteis para a tomada de decisões.
