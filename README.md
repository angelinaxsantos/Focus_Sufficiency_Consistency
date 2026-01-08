# 📘 Focus, Sufficiency and Consistency in XAI

Este repositório contém o trabalho desenvolvido para avaliar **a fidelidade de métodos de Inteligência Artificial Explicável (XAI)**, combinando duas abordagens complementares da literatura recente.

O estudo segue:
- **Focus score** — *Arias et al., 2022*, aplicado a **classificação de imagens**, avaliando se a relevância das explicações está concentrada nas regiões corretas do input.
- **Consistency, Sufficiency e Uniqueness** — *Dasgupta et al., 2022*, aplicadas a **dados tabulares**, para medir a fidelidade das explicações em relação ao comportamento real do modelo.

---

## 🔬 Experimentos realizados

### 🖼️ Focus Score (Imagens)
- **Modelo**: CNN para classificação de 7 tipos de ecopontos  
- **Métodos XAI**:
  - GradCAM
  - GradCAM++
  - LIME
  - SmoothGrad
  - LRP-like
  - Integrated Gradients  
- **Avaliação**: mosaicos 2×2 (in-distribution noise)

### 📊 Métricas de Fidelidade (Dataset Adult)
- Decision Tree (caminhos raiz → folha)
- Logistic Regression + Top-k coefficients
- Random Forest + SHAP
- Random Forest + LIME
- Random Forest + Anchors (vários thresholds)

---

## 🎯 Objetivo

Avaliar **quantitativamente a fidelidade das explicações**, indo além da plausibilidade visual, analisando:
- **Consistency**: se explicações idênticas levam à mesma predição
- **Sufficiency**: se a explicação é suficiente para garantir a decisão
- **Uniqueness**: diversidade das explicações geradas

---

## 🧠 Principais conclusões

- **GradCAM e LIME** apresentaram maior fidelidade em imagens segundo o Focus score
- **Decision Trees e Anchors** produzem explicações altamente consistentes
- **LIME** mostrou bom equilíbrio entre fidelidade e interpretabilidade em dados tabulares
- **SHAP discretizado top-k** apresentou limitações em datasets tabulares densos
- A escolha do método XAI depende do **tipo de dado, modelo e objetivo da análise**

---

## 📚 Referências

- Arias et al., *FOCUS: Faithful Explanations for CNNs*, 2022  
- Dasgupta et al., *Evaluating Faithfulness of Explanations*, 2022  

---

Este repositório acompanha integralmente o relatório e tem como objetivo apoiar estudos sobre **avaliação rigorosa de explicabilidade em Inteligência Artificial**.
