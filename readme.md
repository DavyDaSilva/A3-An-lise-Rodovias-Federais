# Previsão de Acidentes em Rodovias de São Paulo - 
# (Analises com Regressão Binomial Negativa)

Trabalho desenvolvido para a disciplina de **Machine Learning**, com o objetivo de **prever a quantidade de acidentes em rodovias do estado de São Paulo** ao longo de um ano e **propor recomendações de pontos de melhoria** para reduzir a ocorrência desses eventos.

📌 (aqui uma imagem do slide de introdução do projeto)


---

## Contexto do Projeto

Os acidentes rodoviários representam um grave problema de segurança pública e têm impactos sociais e econômicos significativos.  
Com base em dados históricos de acidentes e características das rodovias, este projeto busca **criar um modelo de aprendizado de máquina** capaz de estimar o número de acidentes futuros, auxiliando na **tomada de decisão e no planejamento de políticas preventivas**.

---

## Objetivos

- Desenvolver um modelo de **previsão de acidentes** por rodovia e período.  
- Analisar **fatores que influenciam** a ocorrência de acidentes (ex: tipo de rodovia, tráfego, clima, extensão, conservação, etc.).  
- **Identificar pontos críticos** e sugerir **recomendações de melhorias** com base nas previsões.  
- Aplicar **técnicas de aprendizado supervisionado** e validação de modelos.

---

## Metodologia

1. **Coleta de dados** (estamos aqui atualmente)
   - Fontes públicas, como DER-SP, DNIT, Infosiga-SP, entre outras.  
   - Dados complementares sobre infraestrutura, tráfego e clima.

2. **Pré-processamento**  
   - Limpeza, tratamento de valores ausentes e padronização.  
   - Engenharia de atributos e transformação de variáveis categóricas.

3. **Análise exploratória (EDA)**  
   - Visualização de padrões espaciais e temporais.  
   - Correlações entre variáveis explicativas e número de acidentes.

4. **Modelagem preditiva**  
   - Modelos testados: Regressão Linear, Random Forest, XGBoost, entre outros.  
   - Avaliação de desempenho usando métricas como MAE, RMSE e R².

5. **Recomendações**  
   - Análise dos pontos críticos.  
   - Sugestões de ações preventivas e melhorias em infraestrutura.

---

## Explicação Simples o que é "Regressão Binomial Negativa"?

Normalmente, quando contamos eventos (como número de acidentes), usamos modelos estatísticos.

Um modelo comum é o Poisson
Mas ele assume que a média ≈ variância

👉 No nosso caso:
Média ≈ 20
Variância > 1000
.
Isso mostra que os dados são muito dispersos

Por isso, usamos o modelo:

👉 Regressão Binomial Negativa

📌 Em termos simples:

É um modelo que funciona melhor quando há muita variação nos dados (caso comum em acidentes).

📌 (aqui uma imagem comparando Poisson vs Binomial Negativa)

---

## Dados Utilizados

Os dados estão organizados por trechos de rodovias e incluem:

### Tráfego
* Volume médio diário (VDM)
 Infraestrutura
* Tipo de pista (simples ou dupla)
* Índice de criticidade
### Geometria
* Tipo de terreno
* Tipo de área (urbana/rural)
* Extensão do trecho
### Acidentes
* Sem vítimas
* Com vítimas
* Com mortes

📌 (aqui uma imagem das variáveis do slide)

---

📌 (aqui uma imagem do código ou gráfico de distribuição)

---

## Principais Insights

### 1. Tipo de pista importa MUITO
* Pistas simples aumentam significativamente os acidentes
### 2. Áreas urbanas têm mais acidentes
* Maior interação entre veículos
### 3. Melhor infraestrutura reduz acidentes
* Índices de criticidade estão diretamente ligados ao risco
### 4. Volume de tráfego é um dos fatores mais fortes
* Quanto mais carros → mais acidentes
### 5. Para mortes:
* Pistas duplas reduzem o risco
* Infraestrutura ainda é decisiva

📌 (aqui uma imagem da tabela de coeficientes)

---
 
## 📌Conclusões

Este projeto mostra que:

* Infraestrutura salva vidas
* Pistas duplicadas são mais seguras

## 🎯 Recomendações
Com base nos resultados:

* ✅ **Priorizar duplicação de rodovias** (Especialmente em áreas com alto tráfego)

* ✅ **Investir em manutenção** (Reduz diretamente o risco)

* ✅ **Monitorar áreas urbanas** (Mais propensas a acidentes)

* ✅ **Usar modelos preditivos** (Para antecipar riscos)

---

## Ferramentas Utilizadas
* Python
* Pandas
* Statsmodels
* Jupyter Notebook
