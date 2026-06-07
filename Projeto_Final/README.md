# Desafio Criativo com GenAI: Extraindo Insights do Feedback de Clientes Bancários

## 📌 Visão Geral

Este projeto foi desenvolvido para o desafio **"Desafio Criativo com GenAI: Extraindo Insights do Feedback de Clientes Bancários"** da DIO, com o objetivo de demonstrar a utilização de Inteligência Artificial Generativa para transformar feedbacks de clientes em informações estratégicas para o negócio.

A proposta consiste em simular um ambiente de uma instituição financeira que deseja compreender melhor a experiência dos seus clientes, identificar oportunidades de melhoria em seus produtos e descobrir novas demandas de mercado.

Para isso, foram criados conjuntos de dados fictícios contendo informações sobre clientes, produtos bancários e feedbacks. Após o tratamento dos dados utilizando Power Query, foi desenvolvido um prompt especializado para que o ChatGPT realizasse análises automatizadas e apresentasse recomendações de melhoria.

---

# 🎯 Objetivos do Projeto

## Objetivo Geral

Utilizar Inteligência Artificial Generativa para analisar feedbacks de clientes bancários e gerar insights que auxiliem na melhoria contínua dos produtos financeiros.

## Objetivos Específicos

* Criar uma base de dados simulando clientes de uma instituição financeira.
* Estruturar informações sobre produtos bancários.
* Registrar opiniões e experiências dos clientes.
* Realizar tratamento e padronização dos dados.
* Desenvolver prompt para análise automatizada.
* Identificar padrões e tendências nos feedbacks.
* Gerar recomendações para melhoria dos produtos.
* Demonstrar aplicações práticas de IA Generativa em análise de dados.

---

# 🛠 Tecnologias Utilizadas

| Tecnologia           | Finalidade                                  |
| -------------------- | ------------------------------------------- |
| JSON                 | Armazenamento dos dados simulados           |
| Excel                | Consolidação dos dados                      |
| Power Query          | Limpeza e transformação dos dados           |
| ChatGPT              | Análise dos feedbacks e geração de insights |
| Engenharia de Prompt | Construção das instruções para análise      |

---

# 📂 Estrutura do Projeto

```text
Projeto/
│
├── Docs/
│   ├── clientes.json
│   ├── feedbacks.json
│   └── produtos.json
│
├── Tratamento_Dados/
│   └── Feedbacks_clientes.xlsx
│
├── Projeto_Final
|   ├── README.md
|   ├── Prompt
│   └── Resultado_Analise.pdf
│
├── Visualizacao_Projetos/
|   ├── Arquivos_json
│   ├── PowerQuery_Transformacoes
|   └── Analise_ChatGPT
|
└── README.md
```

---

# 🗂 Base de Dados

O projeto utiliza três arquivos JSON como fonte de dados.

## 1. clientes.json

Armazena informações cadastrais dos clientes da instituição financeira.

### Finalidade

Permitir a identificação do perfil dos clientes e relacioná-los aos feedbacks e produtos contratados.

### Estrutura dos Dados

| Campo         | Tipo de Dado | Descrição                      |
| ------------- | ------------ | ------------------------------ |
| id_cliente    | Inteiro      | Identificador único do cliente |
| nome_cliente  | Texto        | Nome completo do cliente       |
| idade         | Inteiro      | Idade do cliente               |
| sexo          | Texto        | Gênero informado               |
| cidade        | Texto        | Cidade de residência           |
| estado        | Texto        | Estado de residência           |
| renda_mensal  | Decimal      | Renda mensal estimada          |
| segmento      | Texto        | Venda direta de produtos       |
| data_cadastro | Data         | Data de cadastro no banco      |

### Exemplo

```json
{
"id_cliente": 1,
"nome_cliente": "Ana Martins",
"idade": 32,
"sexo": "F",
"cidade": "São Paulo",
"estado": "SP",
"data_cadastro": "2022-03-15",
"segmento": "Varejo",
"renda_mensal": 5500
}
```

---

## 2. produtos.json

Contém informações sobre os produtos financeiros oferecidos pelo banco.

### Finalidade

Relacionar os feedbacks aos produtos utilizados pelos clientes.

### Estrutura dos Dados

| Campo           | Tipo de Dado | Descrição                     |
| --------------- | ------------ | ----------------------------- |
| id_produto      | Inteiro      | Identificador do produto      |
| produto         | Texto        | Nome do produto               |
| categoria       | Texto        | Categoria do produto          |
| descricao       | Texto        | Descrição resumida            |
| taxa_juros      | Decimal      | Taxa de juros aplicada        |
| tarifa_minimo   | Decimal      | Valor da tarifa mensal        |
| tarifa_maximo   | Decimal      | Valor da tarifa mensal        |
| parcelas_maximas| Interiro     | Número máximo de parcelas     |

### Exemplo

```json
{
"id_produto": 1,
"produto": "Emprestimo FGTS",
"categoria": "Emprestimo",
"descricao": "Antecipação do saque-aniversário do FGTS.",
"taxa_juros": "1,29% a 1,49% a.m",
"valor_minimo": 100,
"valor_maximo": 20000,
"parcelas_maximas": 12
}
```

---

## 3. feedbacks.json

Contém os comentários realizados pelos clientes sobre os produtos contratados.

### Finalidade

Servir como principal fonte de análise para geração de insights.

### Estrutura dos Dados

| Campo         | Tipo de Dado | Descrição                       |
| ------------- | ------------ | ------------------------------- |
| id_feedback   | Inteiro      | Identificador do feedback       |
| id_cliente    | Inteiro      | Cliente que realizou o feedback |
| data          | Data         | Data do registro                |
| canal         | Texto        | Canal de atendimento            |
| produto       | Inteiro      | Produto avaliado                |
| nota          | Inteiro      | Nota atribuída pelo cliente     |
| comentario    | Texto        | Comentário do cliente           |

### Exemplo

```json
{
"id_feedback": 25,
"id_cliente": 6,
"data": "27/01/2026",
"canal": "App",
"produto": "Residencial",
"nota": 5,
"comentario": "Todo o processo foi muito bem explicado."
}
```

---

# 🔄 Processo de Tratamento dos Dados

Os arquivos JSON foram importados para o Power Query para realização das etapas de preparação dos dados.

## Atividades Executadas

* Importação dos arquivos JSON;
* Expansão de registros e listas;
* Padronização dos tipos de dados;
* Renomeação de colunas;
* Tratamento de valores nulos;
* Ajuste de formatos de datas;
* Criação de relacionamentos lógicos;
* * Consolidação das informações em uma única base.

## Resultado

Arquivo final utilizado na análise:

```text id="v7s82v"
Feedbacks_clientes.xlsx
```

---

# 🤖 Engenharia de Prompt

Foi desenvolvido um prompt especializado para orientar a IA na interpretação dos dados.

O modelo recebeu instruções para:

* Atuar como Analista de Dados;
* Atuar como Analista de Experiência do Cliente;
* Identificar padrões nos feedbacks;
* Comparar opiniões entre produtos similares;
* Detectar problemas recorrentes;
* Sugerir melhorias para os produtos;
* Recomendar oportunidades para novos serviços financeiros.

---

# 📊 Análises Esperadas

A partir dos feedbacks, a IA deve ser capaz de identificar:

## Pontos de Melhoria

* Taxas consideradas elevadas;
* Limites insuficientes;
* Problemas de usabilidade;
* Lentidão em canais digitais;
* Falhas no atendimento.

## Oportunidades de Negócio

* Novos produtos financeiros;
* Segmentação de clientes;
* Personalização de ofertas;
* Benefícios mais aderentes ao perfil dos usuários.

---

# 📈 Benefícios para o Negócio

A utilização da IA nesse processo permite:

* Redução do tempo de análise;
* Identificação rápida de padrões;
* Apoio à tomada de decisão;
* Melhoria contínua dos produtos;
* Maior satisfação dos clientes;
* Criação de estratégias orientadas por dados.

---

# 🚀 Competências Demonstradas

Este projeto evidencia conhecimentos em:

* Análise de Dados
* Tratamento de Dados
* Power Query
* JSON
* Excel
* Inteligência Artificial Generativa
* Engenharia de Prompt
* Experiência do Cliente (CX)
* Documentação Técnica
* Storytelling com Dados

---

# 👩‍💻 Autor

**Maria Aparecida Leite da Silva**

Projeto desenvolvido para fins educacionais e composição de portfólio na área de Dados, Business Intelligence e Inteligência Artificial aplicada aos negócios.

