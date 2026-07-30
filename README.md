# Incremental Learning

[Português](#português) | [English](#english)

## Português

### Visão geral
Este repositório apresenta um estudo de aprendizado incremental aplicado a dados meteorológicos reais, com foco em concept drift e adaptação temporal em modelos de machine learning.[file:1] O projeto investiga a previsão binária de chuva horária no Aeroporto Internacional de Miami com 14 anos de observações ASOS, comparando diferentes políticas de atualização de modelo sob as mesmas condições experimentais.[file:1]

### Objetivo
O estudo compara três estratégias de atualização de modelo em séries temporais: aprendizado incremental, retreinamento periódico e treinamento único como baseline estática.[file:1] A avaliação considera não apenas o desempenho agregado, mas também a estabilidade ao longo do tempo e a significância estatística das diferenças observadas entre os cenários.[file:1]

### Metodologia
O experimento usa validação temporal com janelas deslizantes de 180 dias para treino, 14 dias para teste e avanço de 14 dias entre janelas, preservando a ordem temporal dos dados.[file:1] O problema é tratado como classificação binária de chuva, com foco em F1-score como métrica principal devido ao desbalanceamento da classe positiva, complementado por precisão, recall e acurácia.[file:1]

### Cenários comparados
- **Incremental:** o modelo é treinado inicialmente e atualizado continuamente com novas observações.[file:1]
- **Retreinamento periódico:** o modelo é recriado do zero a cada nova janela de treino.[file:1]
- **Treinamento único:** o modelo é treinado uma vez e reutilizado sem atualização, servindo como baseline estática.[file:1]

### Principais resultados
Nos resultados agregados, o cenário Incremental alcançou F1 de 0.470, superando Retreinamento com 0.381 e Treinamento único com 0.333.[file:1] A análise anual mostrou que o cenário Incremental manteve o maior F1 ao longo de todos os anos avaliados, enquanto o teste pareado de Wilcoxon com correção de Bonferroni indicou diferenças estatisticamente significativas com tamanho de efeito grande entre os cenários.[file:1]

### Tecnologias
- Python
- Jupyter Notebook
- pandas
- NumPy
- River
- scikit-learn
- SciPy
- Plotly

### Estrutura do repositório
- `Incremental_Learning3.ipynb`: notebook principal com preparação dos dados, modelagem, avaliação e análise estatística.

### Como executar
1. Clone o repositório.
2. Instale as dependências do projeto.
3. Adicione a base de dados `MIA20122025.csv` no diretório de trabalho.
4. Abra o notebook `Incremental_Learning3.ipynb` em Jupyter.
5. Execute as células em sequência para reproduzir o experimento.[file:1]

### Destaques para recrutadores
Este projeto demonstra experiência em machine learning para dados temporais, avaliação experimental rigorosa e comparação de estratégias de adaptação sob concept drift.[file:1] Também evidencia prática com pipelines reprodutíveis, métricas apropriadas para dados desbalanceados e validação estatística de resultados.[file:1]

## English

### Overview
This repository presents an incremental learning study on real-world meteorological data, focusing on concept drift and temporal model adaptation in machine learning systems.[file:1] The project investigates binary hourly rainfall prediction at Miami International Airport using 14 years of ASOS observations and compares different model update policies under the same experimental setup.[file:1]

### Objective
The study compares three model update strategies for time series data: incremental learning, periodic retraining, and single training as a static baseline.[file:1] The evaluation covers both aggregate performance and long-term stability, along with statistical testing of the observed differences across scenarios.[file:1]

### Methodology
The experiment uses temporal validation with sliding windows of 180 training days, 14 test days, and a 14-day step, preserving chronological order.[file:1] The task is formulated as binary rainfall classification, with F1-score as the primary metric because the positive class is imbalanced, supported by precision, recall, and accuracy.[file:1]

### Compared scenarios
- **Incremental:** the model is trained initially and then continuously updated with new observations.[file:1]
- **Periodic retraining:** the model is rebuilt from scratch for each new training window.[file:1]
- **Single training:** the model is trained once and reused without updates, serving as a static baseline.[file:1]

### Key findings
In the aggregate results, the Incremental scenario achieved an F1-score of 0.470, outperforming Periodic Retraining at 0.381 and Single Training at 0.333.[file:1] The yearly analysis showed that Incremental maintained the highest F1-score across all evaluated years, and the paired Wilcoxon test with Bonferroni correction indicated statistically significant differences with large effect sizes between the scenarios.[file:1]

### Tech stack
- Python
- Jupyter Notebook
- pandas
- NumPy
- River
- scikit-learn
- SciPy
- Plotly

### Repository structure
- `Incremental_Learning3.ipynb`: main notebook containing data preparation, modeling, evaluation, and statistical analysis.

### How to run
1. Clone the repository.
2. Install the project dependencies.
3. Place the dataset file `MIA20122025.csv` in the working directory.
4. Open `Incremental_Learning3.ipynb` in Jupyter.
5. Run the notebook cells sequentially to reproduce the experiment.[file:1]

### Recruiter-facing highlights
This project showcases experience with machine learning for temporal data, rigorous experimental evaluation, and adaptation strategies under concept drift.[file:1] It also demonstrates reproducible notebook workflows, appropriate metrics for imbalanced data, and statistical validation of model performance differences.[file:1]
