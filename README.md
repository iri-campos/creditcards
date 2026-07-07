# 💳 Detecção de Fraudes em Cartões de Crédito com Machine Learning

Projeto desenvolvido em **Python** para identificação de transações fraudulentas utilizando técnicas de **Machine Learning**, tratamento de dados desbalanceados e avaliação de modelos de classificação.

O objetivo é comparar diferentes estratégias para detecção de fraudes, explorando desde modelos lineares até algoritmos baseados em árvores, além de técnicas de balanceamento de classes como **SMOTE** e **Undersampling**.

---

## 🎯 Objetivo

Construir modelos capazes de identificar transações fraudulentas em cartões de crédito, minimizando falsos negativos e avaliando o impacto do desbalanceamento dos dados na performance dos algoritmos.

---

## 🚀 Tecnologias Utilizadas

- Python 3
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- XGBoost
- Imbalanced-Learn (SMOTE)

---

## 📊 Dataset

O projeto utiliza o conjunto de dados público disponibilizado pelo TensorFlow:

**Credit Card Fraud Detection**

Características do dataset:

- Transações realizadas por cartões de crédito
- Classes altamente desbalanceadas
- Classe **0** → Transação legítima
- Classe **1** → Fraude

O conjunto de dados é carregado automaticamente durante a execução do notebook.

---

## 🔍 Etapas do Projeto

### 📥 1. Importação dos Dados

Leitura do dataset utilizando Pandas.

```python
pd.read_csv(...)
```

---

### 📈 2. Análise Inicial

Foi realizada a análise da distribuição das classes para verificar o nível de desbalanceamento existente entre transações normais e fraudulentas.

---

### ⚙️ 3. Engenharia de Atributos

Aplicação de transformações na variável **Amount**:

- Transformação logarítmica (`log1p`)
- Padronização utilizando `StandardScaler`

Essas etapas ajudam a reduzir a influência de valores extremos e melhoram o desempenho de alguns algoritmos.

---

### ✂️ 4. Divisão dos Dados

Separação entre treino e teste utilizando:

- 70% Treinamento
- 30% Teste

Mantendo a proporção original das classes com `stratify`.

---

### 🤖 5. Modelos de Machine Learning

Foram avaliados diferentes algoritmos:

#### Regressão Logística

Modelo linear utilizado como baseline para classificação.

---

#### Random Forest

Modelo baseado em árvores de decisão com configuração de pesos para lidar com classes desbalanceadas.

---

#### XGBoost

Modelo de Gradient Boosting configurado para aumentar o peso da classe minoritária.

---

## ⚖️ Tratamento do Desbalanceamento

Como fraudes representam uma pequena parcela das transações, foram exploradas diferentes estratégias para equilibrar os dados.

### Undersampling

Redução da quantidade de exemplos da classe majoritária para obter um conjunto balanceado.

---

### SMOTE (Oversampling)

Geração sintética de novos exemplos da classe minoritária utilizando a técnica **Synthetic Minority Over-sampling Technique**.

---

## 📈 Avaliação dos Modelos

Os modelos foram avaliados utilizando métricas apropriadas para problemas de classificação desbalanceada.

### Classification Report

- Precision
- Recall
- F1-score
- Support

---

### Curva ROC

Avaliação da capacidade discriminatória do modelo através da curva ROC e da métrica AUC.

---

### Curva Precision × Recall

Análise especialmente importante para problemas com forte desbalanceamento entre as classes.

---

### Ajuste de Threshold

Também foi explorada a alteração do limite de decisão da Regressão Logística para melhorar o equilíbrio entre:

- Recall
- Precision

dependendo do objetivo da aplicação.

---

## 📂 Estrutura do Projeto

```text
credit-card-fraud/
│
├── creditcards.ipynb      # Notebook principal
├── README.md
```

---

## ▶️ Como Executar

### Clone o repositório

```bash
git clone https://github.com/seu-usuario/credit-card-fraud.git

cd credit-card-fraud
```

### Crie um ambiente virtual

```bash
python -m venv venv
```

### Ative o ambiente

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### Instale as dependências

```bash
pip install pandas numpy matplotlib scikit-learn xgboost imbalanced-learn notebook
```

### Execute o notebook

```bash
jupyter notebook
```

Abra o arquivo:

```
creditcards.ipynb
```

---

## 🧠 Conceitos Aplicados

- Machine Learning Supervisionado
- Classificação Binária
- Engenharia de Atributos
- Normalização de Dados
- Dados Desbalanceados
- SMOTE
- Undersampling
- Logistic Regression
- Random Forest
- XGBoost
- Curva ROC
- Precision × Recall
- Ajuste de Threshold
- Avaliação de Modelos

---

## 📚 Aprendizados

Este projeto demonstra conhecimentos em:

- Pré-processamento de dados
- Construção de modelos de classificação
- Avaliação de desempenho utilizando métricas apropriadas
- Tratamento de classes desbalanceadas
- Comparação entre diferentes algoritmos de Machine Learning
- Ajuste de modelos para problemas reais de detecção de fraudes

---

## 📄 Licença

Projeto desenvolvido para fins educacionais e estudos em Ciência de Dados e Machine Learning.
