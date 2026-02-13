# 🏖️ Análise de Vendas - Loja de Praia

## 📋 Sobre o Projeto

Este projeto realiza uma análise exploratória de dados (EDA) sobre as vendas de uma loja de praia, com o objetivo principal de responder à pergunta: **"A loja vende mais no verão?"**

Através de técnicas de análise de dados e visualização, investigamos padrões sazonais de vendas, comportamento de clientes e identificamos insights valiosos para tomada de decisão estratégica do negócio.

## 🎯 Objetivos

- Analisar o volume de vendas por estação do ano
- Identificar padrões de comportamento de compra dos clientes
- Investigar diferenças no ticket médio entre as estações
- Compreender se há variação na quantidade de itens comprados por período
- Fornecer insights baseados em dados para otimização de estoque e estratégias de marketing

## 🗂️ Estrutura do Dataset

O dataset `compras_loja_praia.csv` contém as seguintes informações:

- **id_compra**: Identificador único da compra
- **cliente_id**: Identificador do cliente
- **produto**: Nome do produto adquirido
- **quantidade**: Quantidade de itens comprados
- **preco_unitario**: Preço unitário do produto
- **data_compra**: Data da transação
- **genero_cliente**: Gênero do cliente
- **idade_cliente**: Idade do cliente (com dados parciais)
- **cidade**: Cidade do cliente (com dados parciais)

## 🔍 Principais Descobertas

### ✅ Sim, a loja vende mais no verão!

**Análise detalhada:**

1. **Volume de vendas**: O verão apresenta o maior valor total de vendas entre todas as estações
2. **Ticket médio**: R$ 2.173,65 no verão vs. R$ 2.004,11 no inverno (~8,5% maior)
3. **Quantidade de clientes**: Praticamente constante em todas as estações (~2.474 clientes)
4. **Quantidade média de itens**: 20,1 itens/compra no verão vs. 19,0 na primavera
5. **Preço unitário**: Permanece estável em todas as estações (~R$ 107)

### 💡 Insight Principal

**O aumento nas vendas no verão NÃO é causado por:**
- Maior número de clientes
- Produtos mais caros

**O aumento É causado por:**
- Clientes comprando mais itens por transação
- Maior volume de compras por cliente

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas**: Manipulação e análise de dados
- **NumPy**: Operações numéricas
- **Matplotlib**: Visualização de dados
- **Seaborn**: Visualizações estatísticas
- **SciPy**: Cálculos estatísticos (z-score)
- **Google Colab**: Ambiente de desenvolvimento

## 📊 Metodologia

### 1. Coleta de Dados
- Importação do dataset do Google Drive
- Análise inicial da estrutura dos dados

### 2. Análise Exploratória
- Verificação de dados ausentes (>50% em idade e cidade)
- Identificação de duplicatas
- Análise de distribuições estatísticas
- Visualização de histogramas e boxplots

### 3. Tratamento de Dados

**Tratamentos realizados:**
- ✅ Conversão do campo `data_compra` para formato datetime
- ✅ Preenchimento de valores ausentes em `genero_cliente` com "Não informado"
- ✅ Remoção de outliers em `quantidade` usando z-score (>3 desvios padrão)
- ✅ Correção de discrepâncias em `preco_unitario` (valores de 0,01 substituídos pelo Q1)
- ✅ Remoção de registros com datas inválidas
- ✅ Criação de colunas derivadas: `mes`, `ano`, `estacao`, `valor_total`

### 4. Análise por Estação
- Agrupamento de dados por estação (hemisfério sul)
- Cálculo de métricas agregadas por período
- Comparação entre estações


## 🚀 Como Executar

1. **Clone o repositório**
```bash
git clone https://github.com/seu-usuario/analise-loja-praia.git
cd analise-loja-praia
```

2. **Configure o Google Colab** (se usar)
   - Faça upload do notebook para o Google Colab
   - Monte seu Google Drive
   - Ajuste o caminho do dataset: `/content/drive/MyDrive/datasets/compras_loja_praia.csv`

3. **Execute o notebook**
   - Execute as células sequencialmente
   - Observe as visualizações e análises geradas

## 🎓 Aprendizados

Este projeto demonstra:
- Importância do tratamento adequado de outliers
- Técnicas de limpeza e preparação de dados
- Análise de séries temporais e sazonalidade
- Interpretação de métricas de negócio
- Comunicação de insights baseados em dados


## 📝 Conclusões

A análise confirmou que a loja de praia vende significativamente mais no verão, principalmente devido ao aumento na quantidade de itens comprados por cliente, não por aumento no número de clientes ou nos preços. Essa informação é valiosa para:

- **Gestão de estoque**: Aumentar estoque no verão
- **Marketing**: Campanhas focadas em aumentar o ticket médio nas outras estações
- **Precificação**: Estratégias de bundle para incentivar compras maiores o ano todo
- **Recursos Humanos**: Planejamento de equipe para alta temporada

