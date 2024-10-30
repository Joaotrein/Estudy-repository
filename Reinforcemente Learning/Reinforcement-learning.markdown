b

**Reinforcement Learning** é um programa de computador que aprende a partir de dados, e após o aprendizado desempenha alguma ação quando mais dados são apresentados a ele. E tudo isso através de um sistema de recompensas.

Essas recompensas são basicamente o que vai definir as suas decisões no futuro, afim sempre estar recebendo as melhores recompensas.

Existem três características principais em RL:

**Aprendizagem por tentativa e erro de ações;**

**Maximização de recompensas futuras;**

**Interação e modificação das situações por meio de suas ações.**


<h2>2. Objetivo</h2>

**Objetivo:** Jogo da velha

**Agente:** Representa a abordagem programada. Em RL, o agente é qualquer entidade que está desempenhando ações e recebendo recompensas.

**Ambiente:** É tudo aquilo que não é considerado o agente. Basicamente representa o contexto ao redor do agente relevante ao problema sendo resolvido.

**Estados:** Estados são as situações e informações que compõem o ambiente.

No jogo da velha, os estados incluem informações que nosso agente não tem acesso e incluiriam os pensamentos do adversário, além de suas futuras jogadas. Já as observações seriam apenas as informações que se tem acesso e as configurações de posição das peças no tabuleiro.

Matematicamente se descrevem estados por meio de:

$$
\huge s \in S
$$

Um estado s pertencente ao conjunto de todos os estados possíveis S.

**Ações:** São as possíveis formas que o **agente** consegue interagir com o **ambiente**.

Existem ações discretas que contam as possíveis possibilidades dentro de um conjunto. E as ações continuas que não é possível contar o número de ações totais, visto que são infinitas.

A forma de se modelar matematicamente as ações que um agente pode tomar se define por:

$$
\huge a \in A
$$

**Uma ação a pertencente ao conjunto de ações possíveis A.** 

Cada ação tomada pelo agente pode causar uma mudança de estado e após a tomada da ação uma recompensa é recebida.

**Recompensa**: A a recompensa é obtida sempre por meio de uma transição do estado de origem para o próximo estado **após** a tomada de uma ação. Isto significa que o próximo estado sempre vem acompanhado de uma recompensa.

No exemplo do jogo da velha poderíamos dar uma recompensa de **+1** toda vez que o nosso programa fizesse uma jogada vencedora, **-1** toda vez que o adversário fizesse o mesmo e **0** nas demais jogadas.

A recompensa é expressa matematicamente como:

$$
\huge r \in R
$$

Podendo ser um número de qualquer valor negativo ou positivo. Lembrando que as recompensas diferem para cada transição de estado.

**Incerteza:** O processo de interação com o ambiente, mudança de estado e recompensas é um processo estocástico (aleatório). O próximo estado do agente nunca é uma certeza de qual vai ser, é definido aleatoriamente de acordo com as possibilidades.

As chamadas  **probabilidades de transição** , representam as probabilidades de se mudar para um próximo estado, dado que um agente tomou uma ação **A** e está no estado  **S** . Em termos matemáticos mais precisos:


$$
\huge  P(s_{t+1}, R_{t} \mid s_{t}, a_{t})
$$


**Política:** O que determina a ação que o agente tomará é chamada de política. A política do agente é o que diz qual ação ele tomará, dado o encontro de um determinado estado. 

Existem dois tipos de política: A **determinística** - que simplesmente retorna uma ação a ser tomada para cada estado e **probabilística** que diz qual será a próxima ação por meio de uma distribuição de probabilidades. A probabilística mais comumente utilizada é equacionada da seguinte forma:

$$
\huge \pi (a|s)

$$

**Aqui π representa apenas uma função, que retorna a probabilidade de tomar a ação a dado que o agente se encontra em um estado s.**

**Episódio**: Em RL o conceito de **episódio** representa uma série de interações entre um **agente** e o **ambiente** sendo que em algum momento o episódio chega ao fim.

Imagem final:

![1730195636532](image/Reinforcement-learning/1730195636532.png)


[Fonte do estudo](https://medium.com/datarisk-io/conceitos-para-enteder-reinforcement-learning-2b04d68bf4f9)
