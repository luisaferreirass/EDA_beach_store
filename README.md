# 🏖️ Sales Analysis - Beach Store

## 📋 About the Project

This project performs an exploratory data analysis (EDA) of a beach store's sales, with the main goal of answering the question: **"Does the store sell more in the summer?"**

Using data analysis and visualization techniques, we investigate seasonal sales patterns and customer behavior, and identify valuable insights for strategic business decisions.

## 🎯 Goals

- Analyze sales volume by season
- Identify customer purchasing behavior patterns
- Investigate differences in average ticket across seasons
- Understand whether the number of items purchased varies by period
- Provide data-driven insights to optimize inventory and marketing strategies

## 🗂️ Dataset Structure

The `compras_loja_praia.csv` dataset contains the following information:

- **id_compra**: Unique purchase identifier
- **cliente_id**: Customer identifier
- **produto**: Name of the purchased product
- **quantidade**: Number of items purchased
- **preco_unitario**: Unit price of the product
- **data_compra**: Transaction date
- **genero_cliente**: Customer gender
- **idade_cliente**: Customer age (partial data)
- **cidade**: Customer city (partial data)

## 🔍 Key Findings

### ✅ Yes, the store sells more in the summer!

**Detailed analysis:**

1. **Sales volume**: Summer has the highest total sales of all seasons
2. **Average ticket**: R$ 2,173.65 in summer vs. R$ 2,004.11 in winter (~8.5% higher)
3. **Number of customers**: Practically constant across all seasons (~2,474 customers)
4. **Average number of items**: 20.1 items/purchase in summer vs. 19.0 in spring
5. **Unit price**: Remains stable across all seasons (~R$ 107)

### 💡 Main Insight

**The increase in summer sales is NOT caused by:**
- A larger number of customers
- More expensive products

**The increase IS caused by:**
- Customers buying more items per transaction
- Higher purchase volume per customer

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical operations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical visualizations
- **SciPy**: Statistical calculations (z-score)
- **Google Colab**: Development environment

## 📊 Methodology

### 1. Data Collection
- Importing the dataset from Google Drive
- Initial analysis of the data structure

### 2. Exploratory Analysis
- Checking for missing data (>50% in age and city)
- Identifying duplicates
- Analyzing statistical distributions
- Visualizing histograms and boxplots

### 3. Data Treatment

**Treatments performed:**
- ✅ Converted the `data_compra` field to datetime format
- ✅ Filled missing values in `genero_cliente` with "Não informado" (Not informed)
- ✅ Removed outliers in `quantidade` using z-score (>3 standard deviations)
- ✅ Fixed discrepancies in `preco_unitario` (values of 0.01 replaced with Q1)
- ✅ Removed records with invalid dates
- ✅ Created derived columns: `mes`, `ano`, `estacao`, `valor_total`

### 4. Analysis by Season
- Grouping data by season (southern hemisphere)
- Computing aggregated metrics per period
- Comparing seasons


## 🚀 How to Run

1. **Clone the repository**
```bash
git clone https://github.com/seu-usuario/analise-loja-praia.git
cd analise-loja-praia
```

2. **Set up Google Colab** (if using it)
   - Upload the notebook to Google Colab
   - Mount your Google Drive
   - Adjust the dataset path: `/content/drive/MyDrive/datasets/compras_loja_praia.csv`

3. **Run the notebook**
   - Run the cells in order
   - Review the generated visualizations and analyses

## 🎓 Learnings

This project demonstrates:
- The importance of properly handling outliers
- Data cleaning and preparation techniques
- Time series and seasonality analysis
- Interpretation of business metrics
- Communicating data-driven insights
