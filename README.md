# Análise de Cluster no Catálogo da Netflix: Explorando Padrões com KMeans e DBSCAN

## 📋 Descrição do Projeto

Este projeto apresenta uma análise exploratória de agrupamento de dados (clustering) aplicada ao catálogo de filmes da Netflix. Utilizamos dois algoritmos de aprendizado de máquina não supervisionado - **KMeans** e **DBSCAN** - para segmentar filmes com base no ano de lançamento, duração e classificação indicativa, identificando padrões estratégicos na distribuição do conteúdo.

## 🎯 Objetivos

- Identificar segmentos naturais no catálogo de filmes da Netflix
- Comparar diferentes abordagens de clustering (KMeans vs DBSCAN)
- Extrair insights sobre a estratégia de curadoria da plataforma
- Demonstrar a aplicação de técnicas de machine learning em dados de entretenimento

## 👥 Autores

- **Hissa Bárbara Oliveira** - hissa.barbara@discente.ufma.br
- **Mariane Feitosa de Oliveira** - mariane.feitosa@discente.ufma.br  
- **Mykael Levy Corrêa de Jesus** - mykael.levy@discente.ufma.br

*Universidade Federal do Maranhão (UFMA) - Bacharelado Interdisciplinar em Ciência e Tecnologia*

## 📊 Dataset

**Fonte:** [TidyTuesday - Netflix Titles Dataset](https://github.com/rfordatascience/tidytuesday/tree/master/data/2021/2021-04-20)
- **Total de títulos:** 7.787 (filmes e séries)
- **Filmes analisados:** ~6.131 filmes
- **Período:** Dados coletados até abril de 2021
- **Variáveis utilizadas:** Ano de lançamento, duração, classificação indicativa

## 🛠️ Tecnologias Utilizadas

### Linguagem e Ambiente
- **Python 3.8**
- **Google Colaboratory**

### Bibliotecas Principais
```python
pandas==1.3.3          # Manipulação de dados
numpy==1.21.2           # Operações numéricas
scikit-learn==1.0.2     # Algoritmos de machine learning
matplotlib==3.4.3       # Visualizações
seaborn==0.11.2         # Gráficos estatísticos
```

### Algoritmos de Clustering
- **KMeans** (k=4, random_state=42, n_init=10)
- **DBSCAN** (eps=0.25, min_samples=15)

## 📁 Estrutura do Projeto

```
netflix-clustering
│
├── Codigo/
│   ├── Análise de Cluster no Catálogo da Netflix - Explorando Padrões com KMeans e DBSCAN.ipynb    # Notebook principal
│
├── docs/
|
│   ├── Análise de Cluster no Catálogo da Netflix- Explorando Padrões com KMeans e DBSCAN.pdf       # Paper acadêmico completo
│
└── README.md                               # Este arquivo
```

## 🚀 Como Executar

### Executar Análise
```python
# Abrir e executar o notebook principal
jupyter notebook netflix_clustering_analysis.ipynb

# Ou executar no Google Colab:
# https://colab.research.google.com/github/seu-usuario/netflix-clustering-analysis/blob/main/notebook/netflix_clustering_analysis.ipynb
```

## 📈 Principais Resultados

### KMeans (4 Clusters)
- **Cluster 0** - Acervo Clássico: Filmes antigos (pré-2000), duração < 120 min
- **Cluster 1** - Mainstream Contemporâneo: Filmes pós-2010, 75-120 min (maior segmento)
- **Cluster 2** - Experiências Estendidas: Filmes longos > 150 min (épicos, documentários)
- **Cluster 3** - Era de Transição: Filmes 2000-2010, padrão similar ao contemporâneo

### DBSCAN (Análise de Densidade)
- **Cluster Principal**: Núcleo denso com filmes padrão (pós-2010, 90-120 min, TV-14/R/TV-MA)
- **Outliers**: ~20% do catálogo representando conteúdo de nicho e diversificação estratégica

### Insights Estratégicos
- **Estratégia "Núcleo e Periferia"**: Foco em conteúdo mainstream complementado por diversidade
- **Concentração Temporal**: Priorização de filmes da última década
- **Valor dos Outliers**: Conteúdo atípico contribui para diferenciação da plataforma

## 📊 Visualizações

### KMeans - Segmentação 2D
![KMeans Clustering](results/kmeans_clusters_plot.png)
*Distribuição de filmes por ano de lançamento vs duração*

### DBSCAN - Análise 3D
![DBSCAN 3D](results/dbscan_clusters_3d.png)
*Análise tridimensional incluindo classificação indicativa*

## 📚 Metodologia

### Pré-processamento
1. **Filtragem**: Apenas filmes (séries excluídas)
2. **Limpeza**: Remoção de dados faltantes
3. **Transformação**: Duração convertida para inteiro, classificação para escala 1-5
4. **Normalização**: StandardScaler para equalizar escalas

### Análise Comparativa
- **KMeans**: Visualização 2D (ano vs duração)
- **DBSCAN**: Visualização 3D (ano vs duração vs classificação)
- **Métricas**: Silhouette score, análise de outliers

## ⚠️ Limitações

- Dataset limitado até abril/2021
- Apenas 3 variáveis analisadas
- Sem dados de engajamento/audiência
- Não considera variações regionais
- Simplificação da classificação indicativa

## 📄 Documentação Acadêmica

O projeto inclui um relatório acadêmico completo seguindo padrões SBC:
- **Formato**: PDF, 8 páginas
- **Seções**: Introdução, Fundamentação Teórica, Metodologia, Resultados, Conclusão
- **Referências**
- **Conformidade**: Template SBC oficial

## 📞 Contato

Para dúvidas, sugestões ou colaborações:

- **Hissa Bárbara**: hissa.barbara@discente.ufma.br
- **Mariane Feitosa**: mariane.feitosa@discente.ufma.br
- **Mykael Levy**: mykael.levy@discente.ufma.br

## 📝 Licença

Este projeto é desenvolvido para fins acadêmicos como parte do curso de Bacharelado Interdisciplinar em Ciência e Tecnologia da UFMA.

## 🙏 Agradecimentos

- **TidyTuesday** pela disponibilização do dataset curado
- **Professor Haroldo Gomes Barroso Filho** pelo suporte acadêmico
- **Comunidade Python** pelas ferramentas de análise de dados

---

**⭐ Se este projeto foi útil para você, considere dar uma estrela no repositório!**
