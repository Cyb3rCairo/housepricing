# 📈 Multiple Linear Regression From Scratch (Python)

Este projeto implementa **Multiple Linear Regression do zero**, usando apenas **NumPy**, sem bibliotecas de machine learning como `scikit-learn`.

O objetivo **não é performance**, e sim **entendimento profundo**:
- como o modelo funciona
- como o erro é calculado
- como o gradiente é derivado
- como o Gradient Descent aprende de fato

Inspirado no curso **Machine Learning – Andrew Ng**, mas aplicado em um **dataset real de preços de casas**.

---

## 🧠 O que é feito neste projeto

Implementação manual de:

- Multiple Linear Regression
- Normalização das features (Z-score)
- Função de custo (Mean Squared Error)
- Cálculo do gradiente
- Gradient Descent
- Predição
- Métrica de erro (RMSE)

Tudo **linha por linha**, sem atalhos.

---

## 📂 Dataset

Dataset de preços de casas (`housepricing.csv`), contendo apenas **features numéricas** como:

- bedrooms  
- bathrooms  
- sqft_living  
- sqft_lot  
- floors  
- waterfront  
- view  
- condition  
- sqft_above  
- sqft_basement  
- yr_built  
- yr_renovated  

Target:
- `price`

Features categóricas (cidade, estado, endereço) **foram propositalmente ignoradas** para manter o foco no algoritmo.

---

## ⚙️ Estrutura do Modelo

O modelo aprendido é:

\[
\$$hat{y} = w_1x_1 + w_2x_2 + \dots + w_nx_n + b$$
\]

Onde:
- `w` são os pesos aprendidos
- `b` é o bias
- `x` são as features normalizadas

---

## 📏 Normalização (Z-score)

Antes do treino, todas as features são normalizadas:

\[
x_{norm} = \frac{x - \mu}{\sigma}
\]

Isso é essencial para:
- evitar explosão do gradiente
- garantir convergência do Gradient Descent
- permitir um `alpha` estável

---

## 📉 Função de Custo

Usamos **Mean Squared Error**:

\[
J(w,b) = \frac{1}{2m} \sum (y - \hat{y})^2
\]

Essa função **não é métrica de avaliação**, e sim uma função matemática usada para **otimização**.

---

## 🧠 Gradiente vs Gradient Descent

- **Gradiente**: indica a direção de maior aumento do erro  
- **Gradient Descent**: usa o gradiente para atualizar os parâmetros e minimizar o erro

Atualização dos parâmetros:

\[
w := w - \alpha \cdot \frac{\partial J}{\partial w}
\]

\[
b := b - \alpha \cdot \frac{\partial J}{\partial b}
\]

---

## 📊 Avaliação do Modelo (RMSE)

Para interpretar o erro em unidades reais (dólares), usamos **RMSE**:

\[
RMSE = \sqrt{\frac{1}{m} \sum (y - \hat{y})^2}
\]

Isso responde:
> “Em média, quanto o modelo erra no preço de uma casa?”

⚠️ O RMSE é **apenas para avaliação**, não para treino.

---

## 🧪 Observações Importantes

- O modelo é **linear**
- O dataset é **altamente não-linear**
- Não há informações de localização detalhada
- O erro alto é esperado e faz parte do aprendizado

Este projeto **não busca alta precisão**, e sim **compreensão do algoritmo**.

---

## 🚫 O que NÃO foi usado

- scikit-learn
- `.fit()`
- `.predict()` prontos
- pipelines automáticos
- métricas prontas

Tudo foi implementado manualmente.

---

## 🎯 Objetivo do Projeto

Este repositório existe para:

- estudar Machine Learning de verdade
- entender o que acontece “por baixo do capô”
- criar base sólida para modelos mais avançados
- não depender cegamente de bibliotecas

---

## 📌 Próximos Passos Possíveis

- Train/Test split do zero
- Regularização (Ridge / Lasso) do zero
- Visualização da convergência do custo
- Comparação com implementação do `sklearn`
- Extensão para redes neurais

---

## 🧠 Autor

Projeto de estudo pessoal com foco em **fundamentos reais de Machine Learning**.

Sem atalhos.
Sem mágica.
Só matemática e código.
