# 🗺️ Subsistema de Geoprocessamento (QGIS)

Esta pasta armazena o ecossistema de mapas e o arquivo vetorial consolidado (Shapefile) utilizados na fase de **Engenharia de Atributos, Cruzamento Espacial e Contagem Territorial** que gerou a matriz de dados para a Inteligência Artificial.

---

## 📂 Dicionário de Arquivos do Repositório

O ecossistema é composto pelo arquivo de projeto do QGIS e pelo conjunto de arquivos que formam o Shapefile unificado com todas as variáveis do modelo:

### 1. Projeto Principal
* **`Igrejas Cidade do Rio de Janeiro.qgz`**: Arquivo de projeto consolidado do QGIS (versão 4.0.3). Ele armazena as estilizações das camadas, os filtros aplicados para o município do Rio de Janeiro e o histórico das ferramentas de análise espacial utilizadas.

### 2. Camada Vetorial Unificada (Shapefile)
Abaixo estão os 6 arquivos interdependentes que compõem o Shapefile **`RJ_Bairros_Metro_BRT_Pontos_Igrejas_Renda.*`**. Eles guardam a geometria dos bairros e a tabela de atributos integrada que alimentou o Python:
* `.shp`: Armazena as propriedades geométricas dos polígonos dos bairros.
* `.dbf`: Tabela de atributos que guarda os dados numéricos e textuais de cada bairro (Renda, Ônibus, Metrô, BRT e Igrejas).
* `.shx`: Arquivo de índice que armazena a ligação posicional entre a geometria e a tabela de atributos.
* `.prj`: Guarda a projeção cartográfica e o sistema de coordenadas do mapa.
* `.cpg`: Define a codificação de caracteres (garante que acentos e caracteres da língua portuguesa nos nomes dos bairros não quebrem).
* `.qmd`: Arquivo de metadados gerado pelo QGIS contendo a documentação e propriedades da camada.

---

## 📐 Diretrizes para Replicação do Ambiente (Governança de TI)

1.  **Caminhos Relativos:** O projeto `Igrejas Cidade do Rio de Janeiro.qgz` foi configurado para ler os dados utilizando caminhos relativos (*Project > Properties > General > Save paths: Relative*).
2.  **Como Abrir:** Para que o QGIS carregue o mapa perfeitamente, faça o download de todos os arquivos desta pasta juntos. O arquivo `.qgz` e os 6 arquivos do Shapefile devem permanecer obrigatoriamente no mesmo diretório.
3.  **Sistema de Referência de Coordenadas (SRC):** Os dados estão projetados e alinhados em **SIRGAS 2000 / UTM zone 23S (EPSG:31983)**, garantindo o rigor métrico e a precisão espacial para as contagens territoriais na cidade do Rio de Janeiro.

---

## 🌍 Fontes dos Dados Originais
* **Malha de Bairros e Dados de Renda:** Instituto Brasileiro de Geografia e Estatística (IBGE) - Censo Demográfico.
* **Infraestrutura de Transportes (Ônibus, BRT, Metrô):** Portais de dados abertos da Prefeitura do Rio de Janeiro (Data.Rio).
* **Mapeamento Eclesiástico:** Overpass Turbo.
