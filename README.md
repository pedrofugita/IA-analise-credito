# 📊 Credit Risk & Customer Segmentation Project

## 📌 Sobre o Projeto
Este projeto é um estudo de **Ciência de Dados e Machine Learning** desenvolvido para simular o ambiente de dados de uma instituição financeira.

Como resultado das análises, foi possível identificar duas aplicações em uma empresa:
1.  **Concessão de Crédito:** Automatizar a aprovação/recusa de empréstimos com base no risco (Aprendizado Supervisionado).
2.  **Marketing Direcionado:** Segmentar a base de clientes em "Personas" para ofertas personalizadas (Aprendizado Não Supervisionado).

## 🚀 Funcionalidades e Diferenciais

### 1. Engenharia de Dados (Data Engineering)
Desenvolvi um **Gerador de Dados Sintéticos** robusto em Python que simula 50.000 clientes, quantidade que pode ser alterada.
* **Lógica de Negócio Realista:** Criei correlações matemáticas genéricas onde variáveis como *Escolaridade* impactam a *Renda*, e a *Renda* limita o *Valor do Empréstimo*.
* **Tratamento de Dados:** Pipeline de pré-processamento com **One-Hot Encoding** para variáveis categóricas (Estado Civil, Escolaridade).

### 2. Análise de Risco (Random Forest)
Treinei um modelo de **Random Forest Classifier** para prever a probabilidade de inadimplência (calote).
* **Acurácia:** O modelo atingiu alta precisão na distinção entre bons e maus pagadores.
* **Explainable AI:** Análise de *Feature Importance* para entender quais fatores (ex: Score de Crédito, Razão Dívida/Renda) mais pesam na decisão.

### 3. Segmentação de Clientes (K-Means Clustering)
Apliquei o algoritmo **K-Means** para descobrir grupos ocultos na base de clientes (Clusterização) para CRM.
* **Cluster A (Iniciantes/Risco):** Renda baixa e Score volátil.
* **Cluster B (Consolidados):** Renda média e bom histórico.
* **Cluster C (Prime/VIP):** Alta renda e alto score (Foco em produtos de investimento).

### 4. Produto de Dados (Simulador Interativo)
Desenvolvi uma **Interface Gráfica (GUI)** dentro do Jupyter Notebook usando `ipywidgets`.
* A ferramenta permite que um analista simule um pedido de empréstimo em tempo real e receba a resposta da IA (Aprovado/Recusado) instantaneamente com as probabilidades calculadas.

## 🛠 Tech Stack
* **Linguagem:** Python 3.10+
* **Análise & Manipulação:** Pandas, NumPy
* **Visualização:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-Learn (Random Forest, K-Means)
* **Interface:** Ipywidgets
* **Ambiente:** Jupyter Notebook

## 📦 Como Rodar o Projeto

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/pedrofugita/IA-analise-credito.git](https://github.com/pedrofugita/IA-analise-credito.git)
    cd IA-analise-credito
    ```

2.  **Crie o ambiente virtual e instale as dependências:**
    ```bash
    python -m venv venv
    # Windows:
    venv\Scripts\activate
    # Linux/Mac:
    source venv/bin/activate

    pip install pandas matplotlib seaborn scikit-learn jupyter ipywidgets
    ```

3.  **Abra o Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```

4.  **Execute o Arquivo:**
    Abra o arquivo `.ipynb` principal e rode todas as células (`Cell > Run All`) para ver a geração de dados, o treinamento dos modelos e o simulador interativo no final.

---
*Desenvolvido por Pedro Fugita.*