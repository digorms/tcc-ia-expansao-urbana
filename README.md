# Análise Preditiva de Expansão Eclesiástica no Rio de Janeiro usando Machine Learning

Este repositório contém o ecossistema de Engenharia de Dados e o modelo de Inteligência Artificial desenvolvidos para o Trabalho de Conclusão de Curso (TCC). O objetivo do projeto é cruzar dados socioeconômicos e de infraestrutura de transporte urbano para identificar bairros com potencial de expansão eclesiástica latente na cidade do Rio de Janeiro.

---

## 📊 Desempenho do Modelo (Random Forest Regressor)

O algoritmo foi treinado utilizando uma divisão estatística de 80% para treino e 20% para teste. Os resultados obtidos foram:

*   **R² Score (Poder de Explicação):** 0.43  
    *Significado Acadêmico:* Fatores macroestruturais de transporte e renda média explicam **43%** da lógica de distribuição de templos na capital. Para fenômenos sociais e demográficos, trata-se de um índice de forte relevância científica.
*   **Erro Médio Absoluto (MAE):** 4.76 igrejas  
    *Significado Acadêmico:* Em média, as previsões do modelo flutuam em menos de 5 templos para mais ou para menos por bairro, demonstrando alta calibração e estabilidade algorítmica.

---

## 🛠️ Estrutura do Repositório

```text
├── data/
│   └── RJ_Bairros.csv             <- Matriz de dados consolidada e tratada
├── gis/
│   ├── README.md                  <- Documentação das camadas de mapas
│   └── RJ_Bairros_Metro_BRT_Pontos_Igrejas_Renda.prj         <- Arquivo de projeto do QGIS 3.x
├── notebooks/
│   └── modelagem_random_forest.ipynb <- Código original do Google Colab
└── README.md                      <- Esta documentação principal
