# Data Science from Zero to Junior

> Trilha prática de formação em Ciência de Dados, construída como um repositório de estudos, projetos aplicados e entregáveis orientados a portfólio.



---

## Visão Geral

Este repositório documenta minha jornada prática de evolução em **Ciência de Dados**, com foco em fundamentos, análise exploratória, SQL, Python, Big Data, PySpark, Power BI, Engenharia de Dados, carreira e projetos aplicados para portfólio.

A proposta é transformar uma trilha de estudos em um conjunto de entregáveis profissionais, organizados em capítulos, notebooks, documentação técnica, evidências analíticas e estudos de caso.

O objetivo não é apenas estudar conceitos isolados, mas construir uma base sólida e demonstrável de competências para atuar em projetos reais de dados.

---

## Propósito do Repositório

Este projeto nasce da necessidade de organizar uma jornada de aprendizado em dados de forma prática, progressiva e orientada a resultados.

Em vez de manter estudos dispersos, este repositório consolida:

- notebooks documentados;
- análises exploratórias completas;
- exercícios técnicos;
- estudos de caso;
- evidências geradas por projetos;
- documentação em Markdown;
- entregáveis para portfólio;
- preparação para entrevistas e recolocação profissional.

A ideia central é construir uma trilha que una **aprendizado técnico**, **interpretação de negócio** e **comunicação profissional**.

---

## Justificativa

A área de dados exige muito mais do que conhecer ferramentas. É necessário compreender problemas de negócio, estruturar perguntas analíticas, preparar dados, avaliar qualidade, gerar insights e comunicar resultados de forma clara.

Por isso, este repositório foi organizado como uma jornada de formação prática, cobrindo desde os fundamentos de análise até tópicos mais avançados de Engenharia de Dados e projetos aplicados.

A estrutura busca responder a uma pergunta central:

> Como construir uma base técnica e analítica consistente para evoluir em Ciência de Dados, conectando estudo, prática, portfólio e empregabilidade?

---

## Trilha de Estudos

A trilha está organizada em capítulos progressivos:

| Capítulo | Tema                                             | Objetivo                                                                 |
| -------- | ------------------------------------------------ | ------------------------------------------------------------------------ |
| Cap01    | Aprofundamento em Análise Exploratória de Dados  | Consolidar fundamentos de EDA com estudo aplicado                        |
| Cap02    | SQL: Do Zero a Consultas Avançadas               | Desenvolver domínio de consultas, joins, agregações e análise relacional |
| Cap03    | Python para Big Data & Analytics                 | Aprofundar manipulação, análise e automação com Python                   |
| Cap04    | PySpark para Análise de Dados                    | Introduzir processamento distribuído e análise em escala                 |
| Cap05    | Power BI                                         | Construir dashboards e comunicação visual de indicadores                 |
| Cap06    | Carreiras e Negócios                             | Conectar competências técnicas com posicionamento profissional           |
| Cap07    | Ferramentas e Fundamentos de Engenharia de Dados | Explorar pipelines, camadas de dados e boas práticas de engenharia       |
| Cap08    | Fundamentos de Análise de Dados I                | Reforçar conceitos analíticos essenciais                                 |
| Cap09    | Fundamentos de Análise de Dados II               | Aprofundar análise aplicada e interpretação                              |
| Cap10    | Projeto para Portfólio: EDA em Crédito           | Desenvolver um projeto completo orientado a portfólio                    |
| Cap11    | Checkpoint e Provas                              | Revisar aprendizados e consolidar evolução                               |

---

## Status Atual

| Etapa                            | Status        | Descrição                                                   |
| -------------------------------- | ------------- | ----------------------------------------------------------- |
| Estrutura inicial do repositório | Concluída     | Organização de pastas, ambiente e documentação inicial      |
| Cap01 — Notebook 01              | Concluído     | EDA aplicada ao dataset Olist com visão técnica e executiva |
| README do Cap01                  | Concluído     | Documentação específica do primeiro estudo aplicado         |
| README do repositório            | Em construção | Documentação geral do curso/portfólio                       |
| Cap01 — Notebook 02              | Próximo passo | Aprofundamento e evolução da análise                        |

---

## Projeto em Destaque — Cap01: EDA com Olist

O primeiro estudo aplicado da trilha utiliza o dataset público da Olist para desenvolver uma **Análise Exploratória de Dados em vendas de e-commerce**.

O notebook trabalha com múltiplas dimensões de negócio:

- pedidos;
- clientes;
- produtos;
- vendedores;
- pagamentos;
- frete;
- logística;
- localização geográfica;
- avaliações de clientes;
- indicadores executivos.

A análise foi conduzida com foco em:

- entendimento dos dados;
- validação da estrutura;
- inspeção de nulos e duplicidades;
- conversão de tipos;
- criação de variáveis temporais;
- preservação de granularidade;
- análise comercial;
- análise geográfica;
- análise de experiência do cliente;
- geração de KPIs e recomendações.

A documentação específica do capítulo está em:

```text
from-zero-to-junior/cap01-eda-olist/README.md
```

---

## Metodologia de Trabalho

A abordagem adotada neste repositório segue uma lógica incremental:

1. **Entendimento do problema**  
   Antes do código, o objetivo é compreender o contexto e formular perguntas relevantes.

2. **Entendimento dos dados**  
   Cada base é analisada em termos de estrutura, volume, tipos, nulos, duplicidades e cardinalidade.

3. **Preparação e validação**  
   São aplicadas conversões, padronizações e verificações antes de integrações entre tabelas.

4. **Análise exploratória**  
   As análises são conduzidas por dimensões de negócio e não apenas por gráficos isolados.

5. **Interpretação executiva**  
   Os resultados são traduzidos em insights, riscos, oportunidades e recomendações.

6. **Documentação e portfólio**  
   Cada entrega é documentada para ser reaproveitada em GitHub, LinkedIn e portfólio profissional.

---

## Estrutura do Repositório

```text
senior-level-in-data-science/
│
├── assets/                       # Imagens, banners e recursos visuais
├── data/                         # Estrutura local de dados
│   ├── 00-raw/                   # Dados brutos
│   ├── 01-bronze/                # Dados padronizados inicialmente
│   ├── 02-silver/                # Dados tratados
│   └── 03-gold/                  # Tabelas analíticas finais
│
├── docs/                         # Documentação geral da trilha
│   └── course-roadmap.md
│
├── from-zero-to-junior/          # Conteúdo principal da formação
│   └── cap01-eda-olist/          # Primeiro projeto aplicado
│       ├── notebooks/            # Notebooks do capítulo
│       ├── reports/              # Evidências, outputs e figuras
│       ├── references/           # Materiais de referência
│       └── README.md             # Documentação do capítulo
│
├── notebooks/                    # Notebooks gerais ou experimentais
├── src/                          # Funções Python reutilizáveis
│
├── .gitignore
├── .python-version
├── pyproject.toml
├── uv.lock
├── requirements.txt
└── README.md
```

---

## Camadas de Dados

A estrutura de dados utiliza uma organização inspirada em arquitetura medalhão:

| Camada      | Descrição                                      |
| ----------- | ---------------------------------------------- |
| `00-raw`    | Dados brutos, preservados como recebidos       |
| `01-bronze` | Dados padronizados ou convertidos inicialmente |
| `02-silver` | Dados tratados, limpos e enriquecidos          |
| `03-gold`   | Bases analíticas prontas para consumo          |

Essa estrutura ajuda a reforçar boas práticas de rastreabilidade, reprodutibilidade e evolução progressiva dos projetos.

---

## Ferramentas e Tecnologias

As principais ferramentas utilizadas ou previstas na trilha são:

### Linguagens e bibliotecas

- Python
- SQL
- Pandas
- NumPy
- Matplotlib
- Seaborn
- PySpark

### Ambiente de desenvolvimento

- Jupyter Notebook
- VS Code
- PowerShell
- Git e GitHub
- `uv` para gerenciamento de ambiente Python

### Visualização e entrega

- Power BI
- HTML exportado de notebooks
- Markdown
- GitHub
- LinkedIn
- Portfólio pessoal

### Engenharia de Dados

- Organização em camadas de dados
- Estrutura Raw / Bronze / Silver / Gold
- Preparação para pipelines reprodutíveis
- Versionamento de código e documentação

---

## Como Executar Localmente

### 1. Clonar o repositório

```bash
git clone https://github.com/roberto-ssoares/senior-level-in-data-science.git
cd senior-level-in-data-science
```

### 2. Criar ambiente Python

Com `uv`:

```bash
uv venv --python 3.12
```

### 3. Ativar o ambiente

No Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Instalar dependências

```bash
uv pip install -r requirements.txt
```

Ou, se estiver usando `pyproject.toml`:

```bash
uv sync
```

### 5. Abrir o Jupyter Notebook

```bash
jupyter lab
```

---

## Observação sobre Dados

Os dados brutos não devem ser versionados diretamente no GitHub quando forem grandes ou externos.

A recomendação é manter os arquivos localmente em:

```text
data/00-raw/
```

E documentar a origem dos dados em cada capítulo ou projeto.

---

## Entregáveis Esperados

Ao longo da trilha, este repositório deverá conter:

- notebooks documentados;
- análises exploratórias;
- scripts Python reutilizáveis;
- consultas SQL;
- dashboards;
- arquivos HTML exportados;
- READMEs por capítulo;
- evidências analíticas;
- projetos de portfólio;
- posts técnicos e executivos para LinkedIn.

---

## Competências Desenvolvidas

Este repositório busca demonstrar evolução em competências como:

- análise exploratória de dados;
- preparação e limpeza de dados;
- estatística descritiva;
- modelagem analítica;
- SQL;
- Python para dados;
- visualização de dados;
- interpretação de negócio;
- documentação técnica;
- comunicação executiva;
- organização de projetos;
- boas práticas de GitHub e portfólio.

---

## Próximos Passos

Os próximos movimentos planejados são:

1. Finalizar a documentação e publicação do Cap01 — Notebook 01.
2. Criar o post de LinkedIn apresentando o primeiro estudo aplicado.
3. Iniciar o Cap01 — Notebook 02 com aprofundamento analítico.
4. Evoluir a mesma base para SQL no Cap02.
5. Reaproveitar a estrutura para Python Analytics, PySpark e Power BI.
6. Transformar os principais estudos em páginas do portfólio.

---

## Autor

**Roberto SSoares**  
Profissional da área de dados em transição estratégica para projetos modernos de Ciência de Dados, Engenharia de Dados e Analytics.

- LinkedIn: [roberto-dos-santos-soares](https://www.linkedin.com/in/roberto-dos-santos-soares/)
- GitHub: [roberto-ssoares](https://github.com/roberto-ssoares)
- Portfólio: [roberto-ssoares.github.io](https://roberto-ssoares.github.io/meu-portfolio/)

---

## Nota Final

Este repositório representa uma jornada de aprendizado contínuo, prática aplicada e construção de portfólio. Cada capítulo é tratado como uma entrega progressiva, combinando fundamentos técnicos, análise de negócio e comunicação profissional.



> ### ***Aprender dados é importante.***
> 
> ### ***Transformar aprendizado em evidência prática é o que constrói autoridade profissional.***




