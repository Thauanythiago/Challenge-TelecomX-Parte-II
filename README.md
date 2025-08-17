# 📊 Challenge Telecom X Parte II - Previsão de Evasão de Clientes (Churn)

## 📌 Sobre o projeto
Este projeto tem como objetivo analisar os dados dos clientes da operadora fictícia **Telecom X** e entender os fatores relacionados à evasão (churn).  
A análise foi dividida em duas etapas:

1. **Análise Exploratória e Tratamento dos Dados**  
2. **Construção de Modelos Preditivos de Churn**  

O desafio foi proposto como parte prática da formação **"Aprendendo a fazer ETL"** da Trilha de Data Science da Alura.

---

## 🎯 Objetivos

- **Importação e preparação dos dados**: extração via API, normalização do JSON e limpeza.  
- **Engenharia de variáveis**: criação da métrica de custo diário (`Contas_Diarias`).  
- **Padronização de variáveis**: conversão de respostas binárias ("Yes"/"No") para 1 e 0.  
- **Exploração do churn**: análises por gênero, faixa etária, tipo de contrato, serviços, forma de pagamento, tempo de permanência e custo mensal.  
- **Construção de modelos preditivos**: comparação entre Regressão Logística e Random Forest.  
- **Geração de insights e recomendações**: identificação de padrões e sugestões práticas para retenção.

---

## 🛠️ Tecnologias utilizadas

<div style="display: flex; flex-wrap: wrap; gap: 10px;">

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
<img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib">
<img src="https://img.shields.io/badge/Seaborn-4C4C9D?style=for-the-badge&logo=seaborn&logoColor=white" alt="Seaborn">
<img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
<img src="https://img.shields.io/badge/Imbalanced--Learn-FF6F61?style=for-the-badge&logo=python&logoColor=white" alt="Imbalanced Learn">
<img src="https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=google-colab&logoColor=white" alt="Google Colab">

</div>

---

## 📈 Parte I: Resultados da Análise Exploratória

- **Clientes com contrato mensal** apresentam maior taxa de evasão, indicando menor fidelização.  
- **Pagamentos por Electronic Check** estão fortemente associados ao churn, enquanto métodos como débito automático demonstram maior retenção.  
- **Idosos** têm taxa de churn quase duas vezes maior que clientes mais jovens.  
- **Clientes com menos serviços contratados** ou que utilizam apenas o serviço básico têm maior risco de cancelamento.  
- **Custos mensais e diários mais altos** aumentam a probabilidade de churn.  
- A quantidade de serviços contratados apresentou relação inversa: quanto mais serviços, menor a evasão.

### 💡 Recomendações da Análise Exploratória

- Incentivar **migração para contratos anuais ou bienais** com benefícios associados.  
- Criar campanhas específicas para **novos clientes nos primeiros meses**.  
- Oferecer **pacotes promocionais ou combos** que aumentem o engajamento com serviços adicionais.  
- Direcionar ofertas personalizadas para clientes com **alto custo mensal**.  
- Estimular a utilização de **métodos de pagamento mais estáveis** (ex: débito automático).

---

## 🤖 Parte II: Modelagem Preditiva de Churn

Nesta etapa, construímos modelos preditivos para identificar clientes com maior risco de evasão.

### Modelos testados

- **Regressão Logística**
  - Modelo clássico e interpretável, que mostra como cada variável impacta a probabilidade de churn.
  - Métricas:
    - Acurácia: ~0.75
    - ROC AUC: ~0.84
  - Vantagem: fácil interpretação das variáveis mais relevantes.

- **Random Forest**
  - Modelo de árvore ensemble, robusto e capaz de capturar interações complexas.
  - Observação: melhor desempenho no treino, mas tendência a overfitting.
  - Indicou variáveis relevantes semelhantes à regressão logística.

### Principais variáveis que influenciam o churn

- `Charges_Total` (custo total do cliente)  
- `Daily_cost` (custo diário)  
- `Monthly Charges` (custo mensal)  
- Tipo de contrato (mensal vs. anual/bienal)  
- Número de serviços contratados  
- Forma de pagamento (Electronic Check vs. métodos estáveis)

### Insights obtidos

- Clientes com **custos mais altos** têm maior probabilidade de cancelar.  
- **Contratos mensais** apresentam risco maior de churn do que contratos de longo prazo.  
- **Clientes com menos serviços** ou que usam apenas o serviço básico estão mais propensos a sair.  
- Métodos de pagamento instáveis (como Electronic Check) estão associados a maior evasão.

### Recomendações com base na modelagem

- Incentivar migração para **contratos de longo prazo** com benefícios claros.  
- Direcionar campanhas para **clientes de alto custo** visando retenção.  
- Criar **combos e promoções** que aumentem o uso de serviços adicionais.  
- Estimular o uso de **formas de pagamento mais estáveis**, como débito automático.

> 📘 **[Acesse a análise completa no notebook](https://github.com/Thauanythiago/Challenge-TelecomX-Parte-II/blob/main/TelecomX_Parte2.ipynb)**

## 👤 Autor
Desenvolvido por Thauany Eugenia Thiago como parte dos estudos na Alura e do programa ONE - Oracle Next Education.\
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thauany-eugenia-thiago-629048203)

<p align="center">
  <img src="Badgem%20telecomX%20II.png" alt="Badge TelecomX II">
</p>
