# TelecomX-Parte-2
Telecom X - parte 2
Este projeto realiza uma análise aprofundada da evasão de clientes para a empresa Telecom X, utilizando dados históricos para identificar os fatores que levam os clientes a cancelar seus serviços e construir modelos preditivos para prever a evasão.
Sobre o Projeto
O objetivo principal deste projeto é entender o comportamento de evasão de clientes e desenvolver um modelo de machine learning capaz de prever quais clientes têm maior probabilidade de cancelar seus serviços. As etapas incluem pré-processamento de dados, análise exploratória, balanceamento de classes, modelagem preditiva com diferentes algoritmos e avaliação de desempenho.
Tecnologias utilizadas:
    • Python
    • Pandas (manipulação de dados)
    • Scikit-learn (modelagem e avaliação)
    • Matplotlib e Seaborn (visualização de dados)
    • Imbalanced-learn (balanceamento de classes)
Análises e Visualizações
Distribuição da Evasão
A análise inicial da variável alvo 'Churn' revelou um desequilíbrio significativo nas classes.

Para lidar com o desequilíbrio de classes, foi aplicada a técnica de superamostragem SMOTE, resultando em um conjunto de dados balanceado para o treinamento do modelo de Regressão Logística.

Relação entre Variáveis e Evasão
Investigamos a relação entre algumas variáveis-chave e a evasão de clientes.

Matriz de Correlação
A matriz de correlação foi utilizada para visualizar as relações entre todas as variáveis no conjunto de dados balanceado.

keyboard_arrow_down
Modelagem Preditiva
Foram treinados dois modelos preditivos: Regressão Logística (com dados padronizados e balanceados) e Árvore de Decisão (com dados originais, sem padronização).
Desempenho dos Modelos
Avaliamos o desempenho dos modelos utilizando métricas como Acurácia, Precisão, Recall e F1-score.

Matrizes de Confusão
As matrizes de confusão fornecem uma visão detalhada do desempenho de cada modelo na classificação das instâncias.

Variáveis Mais Influentes
Analisamos os coeficientes da Regressão Logística e a importância das características da Árvore de Decisão para identificar as variáveis que mais influenciam a previsão de evasão.

Recarregar os dados
Subtask:
Carregar o arquivo "df_limpo.csv" e realizar a limpeza inicial (removendo 'customerID').

Transformar variáveis categóricas
Subtask:
Aplicar codificação one-hot às colunas categóricas.

Lidar com valores ausentes
Subtask:
Imputar valores ausentes em 'Total.Day' e 'account.Charges.Total'.

Balancear as classes
Subtask:
Aplicar SMOTE ao conjunto de dados para balancear as classes para a variável alvo 'Churn_Yes'.

Padronizar os dados
Subtask:
Padronizar as características numéricas nos dados reamostrados (X_resampled).

Dividir dados para árvore de decisão
Subtask:
Dividir os dados originais e imputados (X_original_imputed, y_original) em conjuntos de treinamento e teste para o modelo de Árvore de Decisão.

Dividir dados para regressão logística
Subtask:
Dividir os dados reamostrados e padronizados (X_resampled, y_resampled) em conjuntos de treinamento e teste para o modelo de Regressão Logística.

keyboard_arrow_down
Treinar e avaliar regressão logística
Subtask:
Treinar um modelo de Regressão Logística nos dados de treinamento reamostrados e padronizados (X_train_lr, y_train_lr) e avaliar seu desempenho nos dados de teste correspondentes (X_test_lr, y_test_lr).

Raciocínio: Treine o modelo de Árvore de Decisão nos dados de treinamento não escalonados, faça previsões e avalie seu desempenho usando acurácia, precisão, recall e F1-score, em seguida, imprima um relatório de classificação detalhado.

Raciocínio: Calcule e imprima as matrizes de confusão para ambos os modelos e, em seguida, forneça uma análise comparativa e uma avaliação crítica dos resultados.

Raciocínio: Interprete as variáveis mais relevantes para a previsão de evasão para os modelos de Regressão Logística e Árvore de Decisão, acessando e exibindo seus coeficientes e importâncias das características, respectivamente.

Raciocínio: Sintetize as descobertas da avaliação e interpretação do modelo para resumir o modelo com melhor desempenho e as variáveis mais influentes para a previsão de evasão.

keyboard_arrow_down
Resumo:
Principais Descobertas da Análise de Dados
    • O modelo de Regressão Logística, treinado com dados padronizados e balanceados por SMOTE, superou o modelo de Árvore de Decisão, treinado com dados desequilibrados e não padronizados, na previsão da evasão de clientes. O modelo de Regressão Logística alcançou um F1-score de 0.8566 para a classe de evasão, em comparação com 0.5060 da Árvore de Decisão.
    • As variáveis mais influentes consistentemente identificadas em ambos os modelos ou fortemente destacadas pelo modelo de Regressão Logística foram:
        ◦ Contratos mensais estão fortemente associados a uma maior evasão.
        ◦ Um maior tempo de permanência do cliente está associado a uma menor evasão.
        ◦ O uso de cheques eletrônicos como método de pagamento está fortemente ligado a maiores taxas de evasão.
        ◦ As cobranças totais e mensais são fatores importantes que influenciam a evasão.
        ◦ O serviço de internet por fibra ótica e a ausência de segurança online ou suporte técnico mostram uma influência notável na evasão.
        ◦ O faturamento sem papel (paperless billing) está associado a uma maior evasão.
Conclusões ou Próximos Passos
    • Focar os esforços de retenção em clientes com contratos mensais, aqueles que usam cheques eletrônicos para pagamento e clientes com menor tempo de permanência.
    • Investigar a relação entre altas cobranças e a evasão para entender se pacotes de serviços específicos ou estruturas de preços estão contribuindo para a perda de clientes.
