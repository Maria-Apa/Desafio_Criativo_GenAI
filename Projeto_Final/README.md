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
| nome          | Texto        | Nome completo do cliente       |
| idade         | Inteiro      | Idade do cliente               |
| genero        | Texto        | Gênero informado               |
| estado_civil  | Texto        | Estado civil                   |
| profissao     | Texto        | Profissão do cliente           |
| renda_mensal  | Decimal      | Renda mensal estimada          |
| cidade        | Texto        | Cidade de residência           |
| estado        | Texto        | Estado de residência           |
| data_cadastro | Data         | Data de cadastro no banco      |

### Exemplo

```json
{
  "id_cliente": 1001,
  "nome": "João Silva",
  "idade": 35,
  "profissao": "Engenheiro",
  "renda_mensal": 8500
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
| nome_produto    | Texto        | Nome do produto               |
| categoria       | Texto        | Categoria do produto          |
| descricao       | Texto        | Descrição resumida            |
| taxa_juros      | Decimal      | Taxa de juros aplicada        |
| tarifa_mensal   | Decimal      | Valor da tarifa mensal        |
| data_lancamento | Data         | Data de lançamento do produto |

### Exemplo

```json
{
  "id_produto": 201,
  "nome_produto": "Cartão Platinum",
  "categoria": "Cartão de Crédito",
  "tarifa_mensal": 35.90
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
| id_produto    | Inteiro      | Produto avaliado                |
| avaliacao     | Inteiro      | Nota atribuída pelo cliente     |
| comentario    | Texto        | Comentário do cliente           |
| data_feedback | Data         | Data do registro                |
| sentimento    | Texto        | Classificação do sentimento     |

### Exemplo

```json
{
  "id_feedback": 5001,
  "id_cliente": 1001,
  "id_produto": 201,
  "avaliacao": 3,
  "comentario": "Aplicativo lento e limite abaixo do esperado.",
  "sentimento": "Negativo"
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
* Consolidação das informações em uma única base.

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

