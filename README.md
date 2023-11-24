# Projeto 01 - Concessão de Cartões de Crédito

## Introdução

Este projeto tem como objetivo desenvolver um modelo preditivo para identificar o risco de inadimplência em concessões de cartões de crédito. Utilizaremos a metodologia CRISP-DM (Cross-Industry Standard Process for Data Mining) para guiar nossas etapas.

Etapa 1: CRISP-DM - Entendimento do Negócio

Objetivos do Negócio:

Desenvolver um modelo preditivo para auxiliar o cliente na avaliação de suas próprias decisões de crédito.

Objetivos da Modelagem:

Construir o melhor modelo preditivo para identificar o risco de inadimplência.

Atividades do CRISP-DM:

Avaliar a situação do setor de concessão de cartões de crédito.

Entender o tamanho do público, relevância e problemas presentes.

Construir um planejamento do projeto.

Etapa 2: CRISP-DM - Entendimento dos Dados

Dicionário de Dados:

Variáveis como sexo, posse de veículo/imóvel, quantidade de filhos, tipo de renda, educação, estado civil, entre outras.

Carregando Pacotes e Dados:

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn import metrics
from sklearn.ensemble import RandomForestClassifier

df = pd.read_csv('caminho/do/arquivo.csv')

Etapa 3: CRISP-DM - Preparação dos Dados

Operações com Dados:

Seleção, limpeza, construção, integração e formatação.
Tratamento de Dados Faltantes:

df = df.dropna()

Etapa 4: CRISP-DM - Modelagem

Seleção da Técnica de Modelagem:

Utilizaremos o algoritmo RandomForestClassifier.

Desenho do Teste:

Divisão da base em treinamento e teste.
Avaliação do Modelo:

Verificação da acurácia.

clf = RandomForestClassifier(n_estimators=10)
clf.fit(x_train, y_train)
y_pred = clf.predict(x_test)
acc = metrics.accuracy_score(y_test, y_pred)
Etapa 5: CRISP-DM - Avaliação dos Resultados
Matriz de Confusão:
Avaliação do impacto financeiro.
Exemplo Simples:
Lucro dos bons pagadores x Prejuízo dos maus pagadores.
Etapa 6: CRISP-DM - Implantação
Utilização do Modelo:
Implementação em um motor de crédito para tomada de decisões automatizada.
