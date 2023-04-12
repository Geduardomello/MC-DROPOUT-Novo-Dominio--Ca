# MC-DROPOUT-novo-dominio
MONTE CARLO DROPOUT
Replicação do estado da arte em novo domínio
Incerteza Epistêmica em Redes Neurais - Gerson Eduardo de Mello

Esta é uma aplicação do método de incerteza em redes neurais proposto por Yarin Gal. O Dataset escolhido foi retirado de um artigo (RAMIREZ‐LOPEZ, Leonardo et al. Robust soil mapping at the farm scale with vis–NIR spectroscopy. European Journal of Soil Science, v. 70, n. 2, p. 378-393, 2019.) https://bsssjournals.onlinelibrary.wiley.com/doi/pdfdirect/10.1111/ejss.12752 , a variável predita é Concentração de Calcio (Ca) no solo e as variáveis preditoras são niveis de absorbância gerados por sensores óticos em 10 diferentes comprimentos de onda (spc).

#Descrição do método proposto por Yarin Gal:

Em 2015, Yarin Gal mostrou que é possível obter incerteza a partir de redes neurais quase que gratuitamente, se olhássemos técnicas de regularização estocásticas, como Dropout, sob uma perspectiva Bayesiana. Dropout (Srivastava et al, ‎2014) é uma técnica utilizada na maioria das redes neurais modernas para prevenir sobre-ajustamento. Durante o treinamento, Dropout funciona zerando aleatoriamente uma percentagens de neurônios nas camadas da rede neural. No momento de fazer previsões, todos os neurônios são mantidos e a rede neural atua como uma grande mistura de sub-redes menores. Durante o treinamento do modelo, nada muda; mas, durante o teste mantemos a probabilidade de Dropout fixada durante o treino e realizamos T forward-pass pela rede, coletando assim T previsões y para cada amostra. Assim para cada ponto teremos uma previsão para a média e uma previsão para a variância, que será nossa medida de incerteza.
