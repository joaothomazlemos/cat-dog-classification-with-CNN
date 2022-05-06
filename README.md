# cat-dog-classification-with-CNN
Master's assigment done in 2021

# OBJETIVO
Treinar uma rede neural convolucional para predição de imagens classificadas em cachorro ou gato.

O dataset utilizado tem 25000 imagens com label, de onde foi utilizado 4000, sendo 80% para treino, 20% para validação.

# Discussão e resultados:
A rede neural inicialmente foi alimentada com o mesmo número de amostras e mesma altura e largura em relação aos demais modelos. Contudo, a rede neural precisa de um conjunto muito grande de amostras, e também precisa que as amostras tenham alta resolução em relação aos outros modelos, para que ela consiga fazer predições coerentes. Foi possível ver isso na prática, já que com poucos dados a rede não conseguia generalizar tão bem, decorando o conjunto e chegando a overfitting, o que gerou predições aleatórias. Além disso, ocorreu da rede decorar apenas uma classe, tendo uma predição de aproximadamente 50%. Percebeu-se depois, pela matriz confusão, que o motivo era que a rede acertava tudo de uma classe apenas, naturalmente, pois qualquer imagem que ela julgasse, seria associada a somente uma das classes, e havia balanceamente dos dados, onde 50% do conjunto pertencia a cada uma das classes. Além do aumento do número de imagens, foi utilizada a técnica de image augmentation, de forma que cada vez que a rede via uma batch de imagens passar pela iteração (epoch), a imagem nunca era a mesma, já que podia estar com diferente escala, rotação, offset de altura, offset de largura e espelhamento. E ainda, foi utilizado o método de dropout, de forma que os nerônios eram desativados de forma aleatória a cada iteração, para que a influencia de um determinado peso não ofuscasse os outros de forma dominante, o que gerou menos biases e aumentou a generalização. Apóss essas modificações, obteve-se um bom resultado, como esperado das redes neurais, que são muito utilizadas para tarefas relacionadas a visão computacional, principalmente na detecção de objetos. A acurácia do modelo foi alta como esperado, de 83% de acuráci
