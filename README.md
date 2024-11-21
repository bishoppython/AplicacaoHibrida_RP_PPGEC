As métricas de avaliação dependem do objetivo do modelo, que neste caso é prever o **preço de imóveis**. Para problemas de regressão, como este, as métricas mais relevantes são as que avaliam a proximidade entre os valores preditos pelo modelo e os valores reais. Aqui estão as principais métricas que você pode usar:

---

### **1. Erro Médio Absoluto (MAE - Mean Absolute Error)**
**Fórmula:**
\[
\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |\hat{y}_i - y_i|
\]
- **Interpretação:** Média das diferenças absolutas entre os valores preditos (\(\hat{y}_i\)) e reais (\(y_i\)).
- **Vantagens:** Fácil de interpretar, pois está na mesma unidade da variável alvo (preço).
- **Quando usar:** Ideal quando penalizar todos os erros de forma uniforme é desejável.

---

### **2. Erro Quadrático Médio (MSE - Mean Squared Error)**
**Fórmula:**
\[
\text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (\hat{y}_i - y_i)^2
\]
- **Interpretação:** Média dos quadrados dos erros. Penaliza mais os erros maiores.
- **Vantagens:** Útil quando erros grandes devem ser penalizados mais severamente.
- **Desvantagens:** Não está na mesma unidade do preço (é o quadrado).
- **Quando usar:** Para modelos onde minimizar grandes desvios é prioritário.

---

### **3. Raiz do Erro Quadrático Médio (RMSE - Root Mean Squared Error)**
**Fórmula:**
\[
\text{RMSE} = \sqrt{\text{MSE}}
\]
- **Interpretação:** Raiz quadrada do MSE. Representa os erros na mesma unidade do preço.
- **Vantagens:** Mais interpretável do que o MSE.
- **Quando usar:** Quando você deseja penalizar mais os erros grandes, mas ainda quer uma métrica na mesma unidade.

---

### **4. Coeficiente de Determinação (R² - R-Squared)**
**Fórmula:**
\[
R^2 = 1 - \frac{\text{SSE}}{\text{SST}}
\]
Onde:
- \(\text{SSE}\): Soma dos erros quadrados do modelo.
- \(\text{SST}\): Soma dos erros quadrados em relação à média dos dados.

- **Interpretação:** Mede o quanto da variação nos dados é explicada pelo modelo (varia de 0 a 1).
- **Vantagens:** Ajuda a entender a qualidade geral do ajuste do modelo.
- **Quando usar:** Para comparar modelos diferentes e entender a proporção de variância explicada.

---

### **5. Mean Absolute Percentage Error (MAPE)**
**Fórmula:**
\[
\text{MAPE} = \frac{100}{n} \sum_{i=1}^{n} \left| \frac{\hat{y}_i - y_i}{y_i} \right|
\]
- **Interpretação:** Percentual médio de erro absoluto.
- **Vantagens:** Fácil de interpretar como percentual.
- **Desvantagens:** Pode ser sensível a valores reais próximos de zero.
- **Quando usar:** Quando a magnitude relativa dos erros é importante.

---

### **6. Mean Bias Error (MBE)**
**Fórmula:**
\[
\text{MBE} = \frac{1}{n} \sum_{i=1}^{n} (\hat{y}_i - y_i)
\]
- **Interpretação:** Mede a tendência média do modelo (superestimativa ou subestimativa).
- **Quando usar:** Para avaliar se o modelo está tendendo a superestimar ou subestimar.

---

### Resumo das Métricas a Usar
Para a avaliação do seu modelo:
1. **MAE:** Para erros absolutos e interpretação direta.
2. **RMSE:** Para penalizar erros grandes e manter a unidade.
3. **R²:** Para avaliar a capacidade explicativa geral.
4. **MAPE:** Para uma perspectiva percentual, especialmente em casos com preços variando em ordens de magnitude.

**Recomendação:** Use uma combinação de pelo menos **MAE, RMSE e R²** para obter uma avaliação abrangente. Se precisar de ajuda para implementá-las, posso fornecer o código.
