Uma Rede Neural Artificial pode ser definida como uma estrutura complexa interligada por elementos (neuronios), que possuem a capacidade de calcular, para processamento de dados e representação de conhecimento.

Em 1943 seu conceito foi introduzido. Mas, apenas com novos conceitos como backpropagation que ela ganhou popularidade. 

Desde seu desenvolvimento, essa técnica vem sendo muito utilizada por diversas áreas da pesquisa que pretendem precender acontecimentos para ajudar na tomada de decisão.

Atualmente, há diversas topologias das RNA’s que buscam resolver diferentes tipos de problemas, tais como:

* **Processamento de linguagem natural;**
* **Reconhecimento de fala e imagens;**
* **Previsão de valores.**

Uma RNA é uma abstração de um neuronio biológico. Seu objetivo é servir de modelo para o aprendizado e resoluções de problemas complexos.

<h2>Neurônio Biológico</h2>

O sistema nervoso possui arquiteturas complexas. Esse sistema é composto por neurônios que desempenha funções diferentes. Falando da sua estrutura, eles possuem um corpo celular com dois tipos de ramos,**dendritos e axônios.**

O corpo celular carrega informações sobre suas características, além de um plasma que possui substânicas moleculares necesárias para o funcionamento da célula. 

A comunicação entre os neurônios ocorre através de impulsos captados pelos **dendritos**, responsáveis por receber a informação e repassar para o corpo da célula através do **axônio**. 

O **axônio**, que se divide em **colaterais**, recebe sinais a partir do corpo da célula e os transporta para os **dendritos** que vão repassar para os dendritos de outros neurônios vizinhos através da **sinapse**.

A relação entre as redes artificiais e biológica é que ambas possuem axônio e dendrito e comunicam-se por sinapses.  **A representação dessa relação é exibida na imagem abaixo** , onde a letra *x* representa os sinais recebidos e a força sináptica recebida é simbolizada por *w* .

 Ambas as redes possuem a capacidade de ajustar a amplitude das sinapses em uma série de camadas interligadas. O modelo artificial apresentado na imagem abaixo representa a mais simples rede neural artificial, chamada de perceptron.

![1730280546316](image/neural-network/1730280546316.png)

<h2>Perceptron</h2>

Em 1958 a Rede Neural Artificial *Perceptron* foi introduzida por [Frank Rosenblatt](https://en.wikipedia.org/wiki/Frank_Rosenblatt), inspirado nos trabalhos de [Walter Pitts](https://en.wikipedia.org/wiki/Walter_Pitts) e [Warren Sturgis McCulloch](https://en.wikipedia.org/wiki/Warren_Sturgis_McCulloch).

Esse modelo é lido com um único neurônio, classificando o resultado de [forma linear](https://pt.khanacademy.org/math/cc-eighth-grade-math/cc-8th-linear-equations-functions/linear-nonlinear-functions-tut/v/recognizing-linear-functions).

Na figura abaixo, o neurônio artificial é um Perceptron que recebe diversos valores de entradas  *y(n)* . Essas entradas multiplicam-se pelo peso da sinapse *w* e, no final, somam-se formando um conjunto de entrada *ξ* = ∑  *w * y(n)* . 

Esse resultado passa por uma função de ativação linear e transmite a saída  *v* . Quando o valor ξ exceder o limite da função de ativação, o neurônio será ativado e retornará um valor.

![1730280750442](image/neural-network/1730280750442.png)

<h2>Multilayer Perceptron</h2>

Com o intuito de lidar com os problemas não linearmente separáveis, foram adicionadas camadas de neurônio ocultas no modelo de Rosenblatt, formando então a Rede Neural Artificial Multilayer Perceptron (MLP).

![1730281116620](image/neural-network/1730281116620.png)

Essa nova topologia funciona como uma rede  *feedforward * (rede progressiva, a saída de um neurônio se conecta com outro neurônio da próxima camada, no sentido esquerda/direita), formada por um conjunto de neurônios denominados nos.

A rede possui uma camada de entrada (sem função computacional), uma ou mais camadas ocultas e uma camada de saída. A complexidade da rede MLP se dá pela quantidade de camadas ocultas que houver e a quantidade de neurônios que essas camadas possuírem.

<h2>Funcionamento na prática</h2>

![1730281270326](image/neural-network/1730281270326.png)

O funcionamento geral de uma rede MLP está representada na figura acima. Cada neurônio recebe todos os valores das entradas, representadas pelo símbolo *y* , que são multiplicadas pelos **pesos sinápticos** simbolizados pelo w e somadas entre si junto com uma constante chamada de polarização ou bias, representada pelo símbolo  *b* .

Essa constante possui o papel de centralizar a curva da função de ativação em um valor conveniente. Caso seja positivo, o movimento do gráfico é realizado para a esquerda, diminuindo o valor do eixo x. 

Porém, caso seja negativo, o movimento do gráfico é feito para a direita, aumentando o valor do eixo x. A soma ponderada apresentada na equação da imagem acima gera o potencial de ativação que é utilizado para determinar seu valor e propagar para outros neurônios da próxima camada.

![1730281375327](image/neural-network/1730281375327.png)

<h2>Função de Ativação</h2>

Logo após o somatório ponderado dos neurônios, o valor obtido passa por mais um cálculo, chamado de função de ativação ou transferência. 

Seu objetivo é limitar a amplitude de saída do neurônio, ou seja, o valor obtido no somatório é normalizado dentro de um intervalo fechado, como [0,1], podendo ser interpretado também como a probabilidade do resultado.

[Existem diversas funções lineares como a função degrau e identidade e não lineares como a gaussiana, tangente hiperbólica, sigmoide, entre outras, que testam o potencial de ativação através de sua fórmula](https://en.wikipedia.org/wiki/Activation_function).

Em funções lineares, uma das técnicas mais populares é a função degrau, que determina, através de condições, o resultado final. Ou seja, é possível determinar que se o resultado da soma ponderada for menor ou igual zero, o algoritmo entregará um resultado, caso seja maior, ele entregará outro valor final. As condições dependem do que está se classificando.

<h2>Backpropagation</h2>

Quando uma rede neural artificial é inicializada, os pesos sinápticos recebem valores aleatórios que, quando multiplicados pelos valores recebidos, algumas vezes da camada de entrada e outras de neurônios da camada anterior, não atingem os valores desejados no momento do treinamento.

Para corrigir os pesos sinápticos, uma das técnicas populares é a retropropagação, conhecido também como  *backpropagation* , que corrige os valores dos pesos pela diferença entre o valor obtido e o esperado (recebido no treinamento) pelo algoritmo, propagando para todas as células nervosas.

Em 1986, David Rumelhart e seus colegas introduziram o algoritmo  *backpropagation* , possibilitando o treinamento das redes neurais com diversas camadas através da retropropagação. O processo de correção ocorre em dois passos. No primeiro passo, chamado de  *feedforward* , é introduzido um valor na camada de entrada e outro na camada de saída. O resultado flui dentro das camadas internas até que a resposta seja reproduzida na camada de saída. 

Já no segundo passo, ocorre o aprendizado da rede, comparando o valor obtido com o valor desejado, através da equação (1), que subtrai o valor esperado ( *rr* ) do valor obtido ( *ro* ) do neurônio *j* e, caso o resultado não esteja no padrão aceitável, a rede calcula o erro e propaga a correção para as demais camadas internas até a entrada, ajustando os seus pesos sinápticos.

![1730281987472](image/neural-network/1730281987472.png)

![1730281991808](image/neural-network/1730281991808.png)


[Fontes do estudo](https://medium.com/brasil-ai/entendendo-o-funcionamento-de-uma-rede-neural-artificial-4463fcf44dd0)

[Github do criador](https://github.com/Murillo/Artificial-Neural-Networks?source=post_page-----4463fcf44dd0--------------------------------)
