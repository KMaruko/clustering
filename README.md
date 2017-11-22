Codificação dos quatro principais métodos de clusterização, sendo eles:
- K-Means
- Fuzzy C-means
- Mixture of Gaussians
- Hierarchical

Todos os códigos feito em Python, com a utilização de algumas bibliotecas como plot para exibição de gráficos no navegador para obter uma simulação mais real.

________________________________________________________________________________________________________________________________

Primeiramente, o que é clusterização de dados?

Clusterização podem ser considerados um dos problemas mais importantes de aprendizagem não-supervisionada, envolvendo muito fatores de inteligência artificial e questões de machine learning. Problemas que envolvem clusters enfrentam problemas de encontrar uma estrutura um “comum” em uma coleção de dados crus.

Um conceito informal que podemos ter sobre clusterização de dados é basicamente “o processo de organizar objetos e dados em grupos na qual eles são similares de alguma maneira”. 

Suas principais utilizações é na exploração de mineração de dados, com técnicas encima de analises estatísticas de análise de dados, machine learning, reconhecimento de padrões, bioinformações, compressão de dados e inclusive computação gráfica.

O procedimento de clusterização podem ser aplicado em base de textos utilizando algoritmos como text mining, onde o algoritmo procura agrupar textos que falem sobre o mesmo assunto e separar textos que possuem conteúdos diferentes.

Clusterização como já explicitado, não se trata de um algoritmo especifico, mas uma tarefa genérica a ser resolvida que podem ser atingidos ou dar uma solução que não é ótima mas é resolvida em tempo polinomial, de forma eficiente.
	
________________________________________________________________________________________________________________________________


Como já dito, o principal objetivo é determinar e agrupar um conjunto de dados crus. Mas como decidir o fator de utilidade e quão bom um algoritmo de clusterização é bom? Podemos com certeza afirmar que não existe um critério ideal para clusterizar dados. Consequentemente, podemos afirmar que é o usuário que deve suprir esse critério, de maneira a escolher um algoritmo que mais se aproxima do resultado desejado.
	
Por exemplo, podemos estar interessados em encontrar representantes para grupos homogêneos (redução de dados), em encontrar "clusters naturais" e descrever suas propriedades desconhecidas (tipos de dados "naturais"), na busca de agrupamentos úteis e adequados (classes de dados "úteis"), ou na busca de objetos de dados incomuns (detecção de valores aberrantes).

________________________________________________________________________________________________________________________________

As principais necessidades para clusterizar dados é a escabilidade, reconhecer diversos tipos de atributos, descobrir clusters arbitrários, conhecimento mínimo para determinar valores de entrada, usabilidade, suportar alto volume de dados, ordenação de entradas.

Porém, junto com os requerimentos, muitas dificuldades são encontrados no caminho, como por exemplo:
- Técnicas de clusterização quase não suprem 100% do objetivo desejado;
- Grande quantidade de dados em larga dimensão significa problemas em encontrar um algoritmo com eficiência em questões de complexidade de espaço e tempo;
- Um resultado podem ser interpretados de muitas maneiras.


________________________________________________________________________________________________________________________________

ALGORITMOS DE CLUSTERIZAÇÃO

Existem 4 classificações de clusterização, são elas:

•Clustering exclusivo: No primeiro caso, os dados são agrupados de forma exclusiva, de modo que, se um determinado dado pertencer a um cluster definido, ele não poderia ser incluído em outro cluster;
•Clustering sobreposto: O agrupamento sobreposto, usa conjuntos difusos para agrupar dados, para que cada ponto possa pertencer a dois ou mais clusters com diferentes graus de associação. Nesse caso, os dados serão associados a um valor de associação apropriado;

•Clustering hierárquico: Um algoritmo de agrupamento hierárquico é baseado na união entre os dois clusters mais próximos. A condição inicial é realizada definindo cada datum como um cluster. Depois de algumas iterações, ele atinge os clusters finais desejados;

•Clustering Probabilístico: O seu uso é com uma aproximação completamente probabilística.

Existem muitos algoritmos de clusterização, algum deles:
- Propagação por afinidade; 
- Binarização de matrizes de partição de consenso; 
- Canopy; 
- Modelagem ponderada; 
- Cluster de ligação completa; 
- Agrupamento restringido; 
- Agrupamento de fluxo de dados;
- Algoritmo de maximização de expectativa;
- Fuzzy;
- Agrupamento hierárquico;
- Método de estrangulamento da informação;
- K-means;
- Entre muitos outros.

Será usado como exemplo os quatro algoritmos mais utilizados para clusterização:
•K-Means
•Fuzzy C-means
•Hierarchical clustering
•Mixture of Gaussians

Cada um desses algoritmos pertence a um dos tipos de classificação. K-means é um algoritmo de cluster exclusivo, Fuzzy C-means é um algoritmo de agrupamento sobreposto, o agrupamento hierárquico é óbvio, da classe de hierarquica e, finalmente, Mixture of Gaussian é um algoritmo de agrupamento probabilístico. 

________________________________________________________________________________________________________________________________

K-MEANS CLUSTERING


	K-means é um dos algoritmos de aprendizagem mais simples que resolvem o bem conhecido problema de agrupamento. 
	
O procedimento segue uma maneira simples e fácil de classificar um determinado conjunto de dados através de um certo número de clusters (assumir k clusters) fixados a priori. A idéia principal é definir k centroides, um para cada cluster. Esses centroides devem ser colocados de forma astuta devido há diferentes locais que podem causar resultados diferentes. 
  
Logo, a melhor escolha é colocá-los o mais longe possível um do outro. O próximo passo é tomar cada ponto pertencente a um determinado conjunto de dados e associá-lo ao centroide mais próximo. Quando nenhum ponto está pendente, o primeiro passo é concluído e uma grupagem inicial é feita. 
Neste ponto, precisamos recalcular k novos centroides para os clusters resultantes do passo anterior. Depois de ter esses k novos centroides, é necessário fazer uma nova ligação entre os mesmos pontos de ajuste de dados e o centroide novo mais próximo. Um loop foi gerado. Como resultado deste loop, podemos notar que os k centroides mudam sua localização passo a passo até que não haja mais alterações feitas. Em outras palavras, os centroides não se movem mais.

Logo o algoritmo seguem os seguintes passos:
1)Coloque os pontos K no espaço representado pelos objetos que estão sendo agrupados. Esses pontos representam centrosides de grupo inicial;

2)Atribua cada objeto ao grupo que possui o centróide mais próximo;

3)Quando todos os objetos foram atribuídos, recalcule as posições dos centroides K;

4)Repita as etapas 2 e 3 até que os centroides não se movam mais. Isso produz uma separação dos objetos em grupos dos quais a métrica a minimizar pode ser calculada.


Embora possa provar-se que o procedimento sempre terminará, o algoritmo k-means não encontrará necessariamente a configuração mais ótima, correspondente à função de objetivo global mínimo. O algoritmo também é sensível aos centros de cluster inicialmente selecionados aleatoriamente. O algoritmo k-means pode ser executado várias vezes para reduzir esse efeito.

K-means é um algoritmo simples que foi adaptado a muitos domínios problemáticos.


________________________________________________________________________________________________________________________________

FUZZY C-MEANS CLUSTERING

	Fuzzy c-means (FCM) é um método de agrupamento que permite que uma parte de dados pertença a dois ou mais clusters. Este método (desenvolvido por Dunn em 1973 e melhorado por Bezdek em 1981) é frequentemente usado no reconhecimento de padrões. 

A iteração irá parar quando  , onde   é um critério de parada entre 0 e 1, enquanto k são as etapas de iteração. Este procedimento converge para um mínimo local ou um ponto de sela.

Logo o algoritmo seguem os seguintes passos:

1)Inicializa U=[uij] com a matriz, U(0)

2)No passo k: calcular os vetores centrais C(k)=[cj] com U(k)

3)Atualizar U(k), U(k+1)

4)Se || U(k+1) - U(k)||<  então PARA; se não retorna para o passo 2.

Os dados são vinculados a cada cluster por meio de uma Função, que representa o comportamento difuso desse algoritmo. Para fazer isso, simplesmente temos que criar uma matriz apropriada chamada U cujos fatores sejam números entre 0 e 1 e representar o grau de associação entre dados e centros de clusters.

________________________________________________________________________________________________________________________________

HIERARCHICAL CLUSTERING 

Dado um conjunto de N itens a serem agrupados e uma matriz N * N , o processo básico de agrupamento hierárquico segue estes passos:


1)Atribua cada item a um cluster, de modo que se você tiver N itens, você tenha N clusters, cada um contendo apenas um item;

2)Encontre o par de clusters mais próximos (mais parecidos) e misture-os em um único cluster, de modo que agora você tenha um cluster menos;

3)Calcule as semelhanças entre o novo cluster e cada um dos clusters antigos;

4)Repita as etapas 2 e 3 até que todos os itens sejam agrupados em um único conjunto de tamanho N.


O Passo 3 pode ser feito de maneiras diferentes, ligação única, agrupamento completo e agrupamento médio.


Em clustering de ligação única (também chamado de conexão ou método mínimo), consideramos a distância entre um cluster e outro cluster para ser igual à menor distância de qualquer membro de um cluster para qualquer membro do outro cluster. Se os dados consistem em semelhanças, consideramos a semelhança entre um cluster e outro cluster para ser igual à maior semelhança de qualquer membro de um cluster para qualquer membro do outro cluster.

Em clustering de ligação completa (também chamado de diâmetro ou método máximo), consideramos a distância entre um cluster e outro cluster para ser igual à maior distância de qualquer membro de um cluster para qualquer membro do outro cluster.

Em clustering de ligação média, consideramos a distância entre um cluster e outro cluster para ser igual à distância média de qualquer membro de um cluster para qualquer membro do outro cluster.

Esse tipo de agrupamento hierárquico é chamado de aglomerante porque combina os clusters iterativamente. Há também um agrupamento hierárquico divisório que faz o contrário começando com todos os objetos em um cluster e subdividindo-os em peças menores. Os métodos divisivos geralmente não estão disponíveis, e raramente são aplicados.

Não há nenhum ponto em ter todos os N itens agrupados em um único cluster, mas, uma vez que você tenha a árvore hierárquica completa, se você quiser k clusters, você só precisa cortar os links mais longos do k-1.

________________________________________________________________________________________________________________________________

MIXTURE OF GAUSSIANS CLUSTERING

Há outra maneira de lidar com problemas de cluster: uma abordagem baseada em modelo, que consiste em usar certos modelos para clusters e tentar otimizar o ajuste entre os dados e o modelo.
Na prática, cada cluster pode ser matematicamente representado por uma distribuição paramétrica, como um gaussiano (contínuo) ou um Poisson (discreto). Todo o conjunto de dados é, portanto, modelado por uma mistura dessas distribuições. Uma distribuição individual usada para modelar um cluster específico é muitas vezes referida como uma distribuição de componentes.

Um modelo de MIXTURE com alta probabilidade tende a ter os seguintes traços:

•As distribuições de componentes têm "picos" elevados;
•O modelo de MIXTURE "cobre" todos os dados (os padrões dominantes nos dados são capturados por distribuições de componentes).

Principais vantagens do clustering baseado em modelo:

•Técnicas de inferência estatística bem estudadas;
•Flexibilidade na escolha da distribuição do componente;
•Obter uma estimativa de densidade para cada cluster;


O algoritmo funciona dessa maneira:

•Escolhe o componente (o gaussiano) ao acaso com probabilidade;
•Faz um ponto  .
