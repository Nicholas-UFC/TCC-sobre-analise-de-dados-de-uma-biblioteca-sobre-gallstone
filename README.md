# 🏥 Predição da Doença de Cálculo Biliar com Machine Learning

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

Este repositório contém o código-fonte e os experimentos desenvolvidos para o Trabalho de Conclusão de Curso (TCC) em Engenharia Elétrica: **"O Uso de Algoritmos de Classificação de Machine Learning Para Predição da Doença de Cálculo Biliar a Partir de Dados Laboratoriais e de Bioimpedância"**.

---

## 📄 Resumo do Projeto

A doença do cálculo biliar (colelitíase) é um desafio de saúde pública, com o diagnóstico padrão (ultrassonografia) apresentando barreiras de custo. Este projeto propõe uma abordagem de **triagem não invasiva** utilizando Inteligência Artificial.

Utilizando o dataset público **Gallstone-1**, foram testados **17 algoritmos de classificação** para prever a presença da doença com base em 38 atributos (dados clínicos, exames de sangue e bioimpedância).

### 🎯 Objetivos
1. Desenvolver um modelo preditivo de alta acurácia.
2. Identificar os principais fatores de risco usando **SHAP (Explainable AI)**.
3. Superar os benchmarks da literatura existente para este dataset.

---

## 📊 Principais Resultados

O modelo **Gradient Boosting Classifier** obteve o melhor desempenho, superando o estado da arte para este conjunto de dados.

| Métrica | Resultado |
| :--- | :--- |
| **Acurácia** | **91%** |
| **F1-Score** | **91%** |
| **Sensibilidade (Recall)** | **91%** |
| **Precisão** | **91%** |

> **Comparação com a Literatura:**
> * Este trabalho: **91.00%**
> * *Esen et al. (2024)*: 85.42%
> * *Sarker et al. (2025)*: 79.17%

### 🔍 Fatores de Risco Identificados (SHAP)
A análise de interpretabilidade revelou que os maiores preditores da doença são:
* **Proteína C-Reativa (PCR):** Níveis elevados indicam alto risco (Inflamação).
* **Vitamina D:** Níveis baixos indicam alto risco (Metabolismo).
* **Massa Óssea:** Relação inversa com a doença.

---

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido em **Python** utilizando as seguintes bibliotecas:

* **Manipulação de Dados:** `Pandas`, `NumPy`
* **Visualização:** `Matplotlib`, `Seaborn`
* **Machine Learning:** `Scikit-learn` (GridSearchCV, Métricas, Pré-processamento)
* **Modelos:** Gradient Boosting, XGBoost, Random Forest, MLP (Deep Learning), entre outros.
* **Interpretabilidade:** `SHAP` (SHapley Additive exPlanations)

---

## 📂 Estrutura do Repositório

```bash
├── TCC/                # PDF do TCC
├── data/                # Dataset utilizado (gallstone.csv)
├── notebooks/           # Jupyter Notebooks com os experimentos
│   └── main.ipynb       # Notebook principal (EDA, Modelagem e SHAP)
├── image/              # Imagens salvas (gráficos, matriz de confusão)
├── requirements.txt     # Dependências do projeto
└── README.md            # Documentação do projeto