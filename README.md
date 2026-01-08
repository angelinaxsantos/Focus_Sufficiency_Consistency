# Focus, Sufficiency and Consistency — Faithfulness in XAI

Este repositório contém os experimentos desenvolvidos para o estudo da **fidelidade (faithfulness) de métodos de Explainable AI (XAI)**, aplicados a **classificação de imagens** e **dados tabulares**, conforme descrito no relatório.

O trabalho baseia-se em **dois artigos distintos**, aplicados em **cenários diferentes**:

- **Arias et al. (2022)** — métrica **Focus**, aplicada a **classificação de imagens**
- **Dasgupta et al. (2022)** — métricas **Consistency, Sufficiency e Uniqueness**, aplicadas a **dados tabulares**

---

## Experimentos Realizados

### 1. Classificação de Imagens — Focus (Arias et al., 2022)

- Modelo CNN para classificação de **7 tipos de ecopontos**
- Construção de **mosaicos 2×2** (in-distribution noise)
- Avaliação da fidelidade com a métrica **Focus**
- Métodos XAI avaliados:
  - GradCAM
  - GradCAM++
  - SmoothGrad
  - LRP-like
  - Integrated Gradients
  - LIME

---

### 2. Dados Tabulares — Consistency, Sufficiency e Uniqueness (Dasgupta et al., 2022)

Dataset: **Adult**

Cinco experimentos de interpretabilidade:

1. **Decision Tree** (caminhos raiz → folha)
2. **Logistic Regression + Top-k coefficients**
3. **Random Forest + SHAP (Top-k discretizado)**
4. **Random Forest + LIME (Top-k)**
5. **Random Forest + Anchors** (threshold variável)

As explicações foram avaliadas quantitativamente usando:
- **Consistency**
- **Sufficiency**
- **Uniqueness**

---

## Principais Conclusões

- **Focus** é eficaz para avaliar fidelidade em classificação de imagens, destacando GradCAM e LIME como os métodos mais confiáveis no modelo de ecopontos.
- Em dados tabulares:
  - **Decision Trees** e **Anchors** apresentam consistência elevada e explicações verificáveis.
  - **LIME** oferece bom compromisso entre fidelidade local e interpretabilidade.
  - **SHAP Top-k** mostrou limitações em datasets densos após discretização.
  - **Logistic Regression + Top-k** é intuitivo, mas pouco diverso e pouco suficiente.
- Não existe um método XAI universalmente superior: a fidelidade depende do **tipo de dado**, **modelo** e **objetivo da explicação**.

---

## Referências

- Arias et al., *FOCUS: A Faithfulness Metric for XAI*, 2022  
- Dasgupta et al., *Evaluating the Faithfulness of Explainable AI*, 2022
