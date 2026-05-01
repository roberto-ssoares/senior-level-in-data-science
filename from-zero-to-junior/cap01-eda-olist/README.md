# Cap01N01 — Análise Exploratória de Dados em Vendas E-commerce com Olist

## Visão Geral

Este projeto faz parte da trilha **Data Science from Zero to Junior** e representa o primeiro estudo prático do Cap01: **Aprofundamento em Análise Exploratória de Dados**.

O objetivo principal é desenvolver uma Análise Exploratória de Dados, ou EDA (*Exploratory Data Analysis*), utilizando o dataset público da Olist, um conjunto de dados de e-commerce brasileiro com informações sobre pedidos, clientes, produtos, vendedores, pagamentos, frete, localização geográfica, entregas e avaliações.

A proposta do notebook é ir além de uma análise puramente técnica. O estudo foi estruturado para conectar fundamentos de EDA com uma leitura prática de negócio, aproximando o trabalho de um cenário real de análise comercial, logística e experiência do cliente.

---

## Problema de Negócio

Marketplaces e operações de e-commerce precisam compreender continuamente o comportamento dos pedidos, o desempenho comercial, a distribuição geográfica da demanda, o impacto do frete, a eficiência logística e a satisfação dos clientes.

Neste contexto, a pergunta central do projeto é:



> Como os dados de pedidos, produtos, pagamentos, frete, localização e avaliações podem revelar padrões de desempenho comercial, experiência do cliente e oportunidades de melhoria em um e-commerce brasileiro?



A análise busca responder perguntas como:

- Qual é o volume total de pedidos?

- Qual período histórico é coberto pela base?

- Como os pedidos evoluem ao longo do tempo?

- Quais categorias concentram maior volume e maior GMV?

- Quais estados e regiões concentram mais clientes e pedidos?

- Quais métodos de pagamento são mais utilizados?

- Qual é o comportamento do frete em relação ao valor dos produtos?

- Existe relação entre atraso de entrega e avaliação negativa?

- Quais oportunidades de melhoria podem ser identificadas a partir dos dados?

---

## Justificativa do Projeto

A EDA é uma etapa essencial em projetos de dados porque permite compreender a estrutura, a qualidade, os padrões e as limitações dos dados antes da construção de dashboards, modelos preditivos ou recomendações executivas.

No contexto deste projeto, a escolha do dataset Olist se justifica por três motivos principais:

1. **Riqueza relacional dos dados**  
   O dataset é composto por múltiplas tabelas conectadas por chaves, permitindo trabalhar com conceitos importantes como relacionamento entre entidades, granularidade e integração de bases.

2. **Relevância de negócio**  
   O domínio de e-commerce permite analisar vendas, clientes, vendedores, produtos, pagamentos, logística e experiência do cliente, temas comuns em empresas orientadas a dados.

3. **Potencial de evolução da trilha**  
   A mesma base pode ser reutilizada em capítulos futuros, como SQL, Python para Analytics, PySpark, Power BI e projetos de portfólio.

---

## Estratégia Analítica

A análise foi conduzida de forma incremental, respeitando uma lógica profissional de exploração e preparação dos dados.

### 1. Entendimento inicial dos dados

Foram carregadas e catalogadas todas as tabelas do dataset Olist:

- `customers`

- `geolocation`

- `order_items`

- `order_payments`

- `order_reviews`

- `orders`

- `products`

- `sellers`

- `category_translation`

Nesta etapa foram avaliados volume de linhas, quantidade de colunas, consumo de memória e nomes dos campos disponíveis.

### 2. Inspeção estrutural

Foi criada uma função reutilizável para diagnosticar cada DataFrame, avaliando:

- tipos de dados;

- contagem de valores preenchidos;

- contagem de valores nulos;

- percentual de nulos;

- cardinalidade;

- percentual de valores únicos;

- registros duplicados.

Essa etapa permitiu identificar, por exemplo, que campos textuais de comentários em avaliações possuem alto percentual de ausência, enquanto a nota de avaliação está preenchida.

### 3. Conversão de tipos e variáveis temporais

As colunas de data foram convertidas de texto para `datetime`, permitindo criar variáveis derivadas como:

- ano da compra;

- mês da compra;

- ano-mês da compra;

- dia da semana;

- hora da compra;

- tempo entre compra e aprovação;

- prazo real de entrega;

- prazo estimado de entrega;

- atraso em dias;

- indicador de atraso.

### 4. Preservação de granularidade

Antes de integrar as tabelas, foi feita uma análise da granularidade:

- `orders`: uma linha por pedido;

- `order_items`: múltiplas linhas por pedido;

- `order_payments`: múltiplas linhas por pedido;

- `order_reviews`: possível múltipla avaliação por pedido.

Para evitar duplicação indevida de métricas financeiras, as tabelas de itens e pagamentos foram agregadas no nível do pedido antes dos joins.

### 5. Construção de visões analíticas

Foram construídas diferentes visões para análise:

- visão de pedidos;

- visão comercial por pedido;

- visão de produtos e categorias;

- visão geográfica de clientes e vendedores;

- visão de experiência do cliente;

- visão executiva consolidada.

---

## Tópicos Técnicos Trabalhados

Este notebook consolida fundamentos importantes para projetos reais de dados.

### Manipulação e preparação de dados

- leitura de arquivos CSV;

- organização de múltiplos DataFrames;

- uso de dicionários para controle de datasets;

- validação de arquivos esperados;

- criação de catálogo técnico;

- tratamento de tipos de dados;

- conversão de datas;

- criação de variáveis derivadas;

- validação de chaves;

- agregações por diferentes níveis analíticos;

- joins controlados entre tabelas.

### Qualidade de dados

- análise de nulos;

- análise de duplicidade;

- análise de cardinalidade;

- avaliação de colunas identificadoras;

- interpretação de campos opcionais;

- controle de granularidade antes de integrações.

### Análise de negócio

- evolução temporal de pedidos;

- distribuição de status dos pedidos;

- cálculo de GMV;

- análise de frete;

- análise de métodos de pagamento;

- análise de categorias de produto;

- análise geográfica por estado, cidade e região;

- análise de vendedores;

- análise de avaliações;

- relação entre entrega, atraso e satisfação do cliente.

### Visualização de dados

- gráficos de barras;

- gráficos de linha;

- boxplots;

- tabelas-resumo;

- cards executivos em HTML;

- outputs exportáveis para documentação.

---

## Tópicos Matemáticos e Estatísticos

A análise utiliza conceitos fundamentais de estatística descritiva e exploração quantitativa, incluindo:

- contagem de frequências;

- proporções e percentuais;

- média;

- mediana;

- máximo e mínimo;

- medidas de dispersão;

- análise de distribuição;

- comparação entre grupos;

- ranking por métricas;

- análise de concentração;

- análise de valores ausentes;

- análise de cardinalidade;

- cálculo de indicadores operacionais e comerciais.

Esses conceitos foram aplicados diretamente em perguntas de negócio, como volume de vendas, participação por categoria, percentual de atraso, cobertura de avaliações e concentração geográfica.

---

## Ferramentas Utilizadas

O projeto foi desenvolvido com foco em reprodutibilidade e organização analítica.

### Linguagem e bibliotecas

- Python

- Pandas

- NumPy

- Matplotlib

- Seaborn

- Pathlib

- IPython Display

- Watermark

### Ambiente

- Jupyter Notebook

- Ambiente Python gerenciado com `uv`

- Estrutura de projeto com camadas de dados

- Exportação para HTML

### Organização dos dados

A estrutura segue uma abordagem inspirada em camadas analíticas:

```text
 data/
 ├── 00-raw/      # dados brutos
 ├── 01-bronze/   # dados padronizados inicialmente
 ├── 02-silver/   # dados tratados
 └── 03-gold/     # tabelas analíticas finais
```

---

## Estrutura do Projeto

```text
from-zero-to-junior/
└── cap01-eda-olist/
    ├── notebooks/
    │   └── 01_cap01_eda_fundamentos.ipynb
    ├── reports/
    │   ├── figures/
    │   └── outputs/
    ├── references/
    └── README.md
```

---

## Principais Entregáveis

O notebook gera evidências intermediárias e finais para documentação do projeto.

Entre os principais artefatos estão:

- catálogo inicial dos dados;

- diagnóstico estrutural dos datasets;

- ranking de colunas com nulos;

- análise de cardinalidade;

- validação de conversão de datas;

- resumo logístico;

- análise temporal de pedidos;

- visão comercial consolidada;

- resumo por categorias;

- resumo geográfico;

- análise de avaliações;

- KPIs executivos;

- recomendações de negócio;

- tabela Gold com visão integrada de experiência do cliente.

---

## Principais Aprendizados

Durante o desenvolvimento deste notebook, alguns aprendizados foram especialmente importantes:

1. **EDA começa antes dos gráficos**  
   A análise exploratória deve partir de perguntas de negócio e entendimento da estrutura dos dados.

2. **Granularidade é crítica**  
   Antes de fazer joins entre tabelas, é necessário entender o nível de detalhe de cada base para evitar duplicação de métricas.

3. **Nem todo nulo representa problema**  
   Campos opcionais, como comentários textuais de avaliação, podem ter muitos nulos sem comprometer a análise principal.

4. **Datas precisam ser tratadas corretamente**  
   A conversão de colunas temporais permite analisar sazonalidade, prazos, atrasos e evolução histórica.

5. **Uma boa EDA termina com interpretação**  
   O valor da análise está em transformar tabelas e gráficos em insights, riscos, oportunidades e recomendações.

---

## Resumo Executivo

*A análise permitiu construir uma visão integrada da operação de um e-commerce brasileiro, conectando pedidos, itens, pagamentos, produtos, clientes, vendedores, geografia, logística e avaliações.*

*A abordagem adotada permitiu responder perguntas sobre desempenho comercial, concentração de categorias, comportamento regional, métodos de pagamento, prazos de entrega e experiência do cliente.*

*A camada final do notebook consolida KPIs, insights e recomendações, aproximando o estudo de uma entrega executiva aplicável a cenários reais de negócio.*

---

## Recomendações de Negócio

Com base nas análises realizadas, algumas frentes merecem aprofundamento:

1. **Logística e atraso**  
   Monitorar estados, regiões, vendedores e categorias com maior incidência de atraso.

2. **Experiência do cliente**  
   Investigar os fatores associados a avaliações negativas, especialmente atraso, prazo longo e frete elevado.

3. **Estratégia comercial**  
   Priorizar categorias com alto GMV, bom volume de pedidos e potencial de crescimento.

4. **Frete e competitividade**  
   Avaliar regiões e categorias com frete proporcionalmente elevado em relação ao valor dos produtos.

5. **Expansão regional**  
   Identificar estados com baixa participação e avaliar oportunidades de crescimento.

---

## Gancho para a Próxima Fase

Este Notebook 01 consolidou os fundamentos de EDA com Python e Pandas, criando uma visão analítica robusta sobre o dataset Olist.

A próxima fase da jornada será o **Cap01 — Notebook 02**, com foco em aprofundar a análise e transformar as evidências do primeiro notebook em uma camada mais refinada de interpretação, comunicação e preparação para os próximos capítulos.

Além disso, este mesmo dataset poderá ser reutilizado como base para:

- consultas SQL no Cap02;

- análises com Python para Big Data & Analytics no Cap03;

- processamento distribuído com PySpark no Cap04;

- construção de dashboards no Power BI no Cap05;

- publicação como projeto de portfólio.

---

## Status do Projeto

✅ Notebook 01 processado  
✅ Dados carregados e validados  
✅ Diagnóstico estrutural concluído  
✅ Conversão de datas realizada  
✅ Visões analíticas construídas  
✅ Evidências exportadas  
✅ Resumo executivo gerado  
✅ Base preparada para a próxima fase

---

## Autor

**Roberto SSoares**  
LinkedIn: [roberto-dos-santos-soares](https://www.linkedin.com/in/roberto-dos-santos-soares/)  
Portfólio: [Roberto Soares | Portfólio de Projetos em Dados](https://roberto-ssoares.github.io/meu-portfolio-hub/)




