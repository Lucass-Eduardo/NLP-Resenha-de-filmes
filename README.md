# Projeto de NLP

O objetivo deste projeto foi colocar em prática o meu estudo em NLP, focando nas fases de pré-processamento da linguagem natural humana para a linguagem de máquina e, então, treinar um modelo de machine learning para fazer uma análise sentimental e detectar resenhas negativas. Foi utilizada uma base de dados contendo resenhas de filmes do IMDB com rotulagem de polaridade.

Primeiro, foi feito o pré-processamento clássico, incluindo a verificação de valores ausentes e duplicados. Logo em seguida, fiz uma análise da distribuição de filmes e resenhas ao longo dos anos.

Os dados já estavam separados em conjunto de treino e teste. Verifiquei a distribuição de classes e concluí que seria necessário uma ponderação para equilibrá-las, pois já estavam desequilibradas.

Com o primeiro pré-processamento feito, foi a hora de começar a fazer o pré-processamento focado na NLP. Foram removidos pontos, vírgulas e espaços múltiplos para normalizar os dados. Em seguida, os dados foram tokenizados e lematizados. Eu utilizei duas bibliotecas de lematização diferentes: SpaCy e NLTK.

O treinamento foi feito com três modelos: um modelo constante, LightGBMClassifier e Regressão Logística. O modelo constante foi utilizado para uma comparação. O LightGBMClassifier e a Regressão Logística conseguiram atingir a métrica objetivo de 0,85 para o F1 sem a tunagem de hiperparâmetros, então não a realizei, já que o foco do projeto era o pré-processamento. Comparando os processos de lematização com SpaCy e NLTK, o SpaCy se destacou, tendo o melhor desempenho.