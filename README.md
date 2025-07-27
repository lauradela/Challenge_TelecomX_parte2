# Challenge_TelecomX_parte2
Este projeto faz parte da segunda etapa do desafio Challenge_TelecomX_parte2 do curso datascience da Alura. Como tema desenvolver um pipeline de Machine Learning para prever o Cancelamento de Cliente permitindo que a empresa tome ações preventivas e estratégicas para retenção dos mesmos.
 A base de dados é composta por informações contratuais, demográficas e de comportamento dos clientes.

##  Estrutura do Projeto

- `01_preprocessamento.ipynb` → Limpeza, tratamento de dados e transformação de variáveis  
- `02_modelagem.ipynb` → Treinamento de modelos e avaliação de desempenho  
- `03_interpretacao.ipynb` → Análise de importância das variáveis com SHAP  
- `dataset.csv` → Conjunto de dados utilizado  
- `modelo_final.pkl` → Modelo final exportado (opcional)


##  Etapas Realizadas

✔️ Análise exploratória e tratamento de dados  
✔️ Encoding de variáveis categóricas (One-Hot Encoding)  
✔️ Normalização com `StandardScaler`  
✔️ Divisão treino/teste com `train_test_split`  
✔️ Treinamento de 3 modelos:
- Regressão Logística
- Random Forest
- XGBoost  
✔️ Avaliação com métricas: `accuracy`, `precision`, `recall`, `f1-score`, `AUC-ROC`  
✔️ Interpretação com `feature_importance_` e SHAP  
✔️ Conclusão estratégica com recomendações de negócio


 ## Principais Resultados
O modelo XGBoost apresentou o melhor desempenho entre os algoritmos testados, com destaque para a métrica AUC-ROC, indicando alta capacidade de distinguir entre clientes que cancelam e os que permanecem.

As variáveis com maior influência na previsão de churn foram:
Tipo de contrato: contratos de longo prazo (1 ou 2 anos) estão fortemente associados à redução do churn.
Tempo de permanência (tenure): quanto maior o tempo de cliente, menor a probabilidade de cancelamento.
Suporte técnico e segurança online: a ausência desses serviços está relacionada a um aumento nas chances de churn.
Método de pagamento: clientes que utilizam "Electronic check" apresentaram maior tendência de cancelamento.
Cobrança mensal (MonthlyCharges): valores mais altos estão positivamente associados ao churn.
 
    
##  Tecnologias e Bibliotecas

- Python 3
- Pandas, NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib, Seaborn, Plotly

##  Conclusão Estratégica

Com base nas análises, recomenda-se:
- Incentivar contratos longos (1 ou 2 anos)
- Oferecer suporte técnico e segurança online
- Monitorar clientes com valores altos de cobrança mensal
- Avaliar experiência de usuários que pagam via "Electronic Check"
- Agir proativamente com clientes novos (baixa permanência)

