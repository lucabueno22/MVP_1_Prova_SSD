# Previsão Salarial em Cibersegurança com Machine Learning

Este projeto consiste em uma solução de Machine Learning supervisionado desenvolvida como parte da avaliação da disciplina **Sistemas de Suporte à Decisão (SSD)** na Universidade de Brasília.

O objetivo é construir um modelo capaz de **prever o salário anual (em dólares)** de profissionais da área de **cibersegurança**, com base em variáveis como cargo, experiência, país de residência, política de trabalho remoto, entre outras.

---

##  Dataset

- Origem: Kaggle – [Cyber Security Salaries Dataset](https://www.kaggle.com/datasets/deepcontractor/cyber-security-salaries)
- Quantidade de registros: **1.247**
- Colunas principais:
  - `job_title`
  - `experience_level`
  - `employment_type`
  - `employee_residence`
  - `company_location`
  - `company_size`
  - `remote_ratio`
  - `salary_in_usd` (variável alvo)

---

##  Tecnologias utilizadas

- Python 3.x
- Google Colab
- Pandas / NumPy
- Scikit-learn (Pipeline, GridSearchCV, Regressão, Árvores, Random Forest)
- Seaborn / Matplotlib (visualizações)
- ipywidgets (simulador interativo)

---

##  O que este projeto faz?

- Realiza **tratamento e pré-processamento completo** com pipeline
- Treina e avalia múltiplos modelos:
  - Regressão Linear
  - Decision Tree Regressor
  - Random Forest (com e sem otimização)
- Realiza **validação cruzada (K-Fold)**
- Utiliza **GridSearchCV** para otimizar hiperparâmetros
- Gera **métricas e gráficos de avaliação**:
  - R², MAE, RMSE
  - Histograma de erros
  - Real vs Previsto
  - Comparação entre regiões
- Permite **simulações manuais** e **interativas** com base no modelo final

---

##  Como rodar o projeto

###  Opção 1 – Colab (recomendado)

Abra diretamente no Colab:

 [Acessar notebook interativo no Google Colab](https://colab.research.google.com/github/SEU_USUARIO/SEU_REPOSITORIO/blob/main/MVP_1_Prova_SSD_Luca_Bueno.ipynb)

> Permite rodar todos os códigos e usar o **simulador interativo de salários** com interface gráfica.

---

###  Opção 2 – Visualizar no GitHub (versão estática)

Se você apenas deseja **visualizar** o projeto sem rodar os códigos:

 [Ver notebook renderizado no GitHub (sem widgets)](https://github.com/SEU_USUARIO/SEU_REPOSITORIO/blob/main/MVP_1_Prova_SSD_Luca_Bueno_Estatico.ipynb)

> Obs: a versão estática foi criada para visualização sem erros no GitHub. A versão interativa deve ser aberta no Colab.

---

##  Simulações incluídas

- Previsão para diferentes perfis (júnior, sênior, executivo)
- Comparações entre regiões: Brasil x EUA x Alemanha
- **Simulador interativo**: o usuário pode preencher os dados e ver o salário previsto na hora

---

##  Prints de exemplos

| Comparação de modelos | Real vs Previsto | Distribuição dos erros |
|-----------------------|------------------|-------------------------|
| ![](./prints/r2_comparacao.png) | ![](./prints/real_vs_previsto.png) | ![](./prints/erros_hist.png) |

> (Você pode subir essas imagens em uma pasta `/prints` no seu repositório)

---

##  Resultados

- Melhor modelo: **Random Forest Regressor otimizado com GridSearchCV**
- **R² no teste:** 0.4381
- **MAE:** \$34.831,65
- **RMSE:** \$51.644,72

---

##  Possíveis melhorias

- Testar modelos como **XGBoost**, **LightGBM**
- Aplicar técnicas de **feature engineering**
- Agrupar cargos semelhantes e padronizar localizações
- Explorar ensembles com `VotingRegressor` ou `StackingRegressor`

---

##  Autor

**Luca Bueno**  
Engenharia de Produção – Universidade de Brasília  
Projeto desenvolvido como parte da disciplina **Sistemas de Suporte à Decisão**  


