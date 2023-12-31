# Algoritimos-e-Estrutura-de-dados-2
Abaixo segue o nome e enunciado de cada exercício resolvido.

# Força-bruta - problema do troco
Implemente a solução do problema do troco (conforme apresentado em sala de aula) utilizando a estratégia de força-bruta.

**Input Format:**

A primeira linha deve conter o valor do troco. A segunda linha deve conter a quantidade de moedas, que representará o tamanho do vetor que deverá ser lido logo em sequência.

**Output Format:**

Sequência de moedas que foram retornados como troco.

# Agoritmos gulosos - sequenciamento de tarefas em uma máquina
Dada uma máquina que execute uma sequência de n tarefas. Cada tarefa tem um tempo de execução e um deadline. É desejável que todas as tarefas sejam finalizadas sem atrasos, mas nem sempre isso é possível. Uma alternativa para compensar possíveis atrasos, seria a execução de tarefas que terminam antes do tempo e aproveitar esse saldo para executar as outras tarefas. No final da execução de todas as tarefas, se o saldo de tempo (deadline acumulado) for maior igual a zero, então o atraso é igual a zero. Caso o saldo de tempo seja negativo, então o atraso é equivalente ao módulo desse saldo (nesse problema, basta multiplicar o saldo por -1). Desse, o objetivo seria encontrar uma sequência de atividades que minimize o atraso.

Implemente uma função que receba um vetor de atividades de tamanho n. A função deverá imprimir a sequência ótima de atividades que foram executados até ou antes do deadline e retornar o valor do atraso.

Sugestão de estrutura para a representação do problema:

    typedef struct{
        int id; // identificador da tarefa, que será a i-ésima tarefa lida
        int e; // tempo de execução
        int d; // deadline
    }
    
**Input Format:**

Na primeira linha, dever lido o valor de n, que é a quantidade de tarefas.

Nas n seguintes linhas devem ser lidos, em sequência, o tempo de execução e o deadline da i-ésima tarefa.

**Output Format:**

Na primeira linha deve ser impressa a sequência ótima de atividades executadas sem atraso.

Na segunda linha deve ser impressa o atraso total.

# Algoritmos gulosos - Seleção de atividade
Dona Lurdes é responsável pelo gerenciamento de uma sala de aula, onde ela deve alocar a maior quantidade de aulas possíveis durante o expediente. No entanto, fazer essa tarefa de forma otimizada e manualmente pode ser uma tarefa muito difícil, pois muitas disciplinas podem ter horários que sobrepõem entre elas.

Implemente uma função, por meio da estratégia gulosa, para que a maior quantidade possíveis de aula possam ser alocadas na sala.

**Input Format:**

A primeira linha deve ser um número inteiro n referente à quantidade de atividades. Para cada uma das próximas n linhas devem ser lidos o id da tarefa e os horários de início e de fim para cada atividade.

**Constraints:**

As aulas devem ser ordenadas crescentemente pelo horário de término.

**Output Format:**

A primeira linha apresenta a mensagem "Aulas alocadas:" seguida do id das aulas que foram alocadas na respectiva sala.

# Divisão e conquista - soma máxima
Dado um vetor de inteiros. Implemente uma função, utilizando divisão e conquista, que encontre a soma máxima no vetor. Por exemplo: para o vetor v = {-1, 3, 0, -2, 1, 3, -4, 5}, a soma máxima é 12 (3 + 0 + 1 + 3 + 5).

**Input Format:**

A primeira linha deve ser um número inteiro n referente ao tamanho do vetor. Em seguinda, Para cada uma das próximas n linhas devem ser lidos os elementos do vetor.

**Output Format:**

Soma máxima dos elementos do vetor.

# Divisão e conquista - distância de Manhattan
Implemente, utilizando divisão e conquista, uma função para calcular a distância de Manhattan entre dois vetores de mesmo tamanho.

Equação da distância de Manhattan entre dois vetores:

![image](https://github.com/odilonneto/Algoritimos-e-Estrutura-de-dados-2/assets/92185618/533e25f0-418e-48d0-a864-1774fa1ff594)


**Input Format:**

A primeira linha deve ser um número inteiro n referente ao tamanho dos vetores. Na segunda linha, devem ser lidos os n elementos do primeiro vetor. Por fim, na próxima linha deve ser lido os elementos do segundo vetor, que também possui tamanho n.

**Output Format:**

O valor da distância entre os vetores.

# Programação dinâmica - corte ótimo de hastes metálicos
Uma empresa compra hastes de aço longas e as corta em pedaços mais curtos para revenda. Para cada polegada i de comprimento há um preço . Desse modo há uma tabela de preços para hastes de diversos tamanhos em polegadas: . Objetivo é maximizar o ganho em cima de uma haste cortada em vários pedaços.

Por exemplo, considere a tabela de preços abaixo:

Comprimento: 1|2|3|4|5 |6 |7 |8 |9 |10

Preço: 1|5|8|9|10|17|17|20|24|30

Para uma haste de tamanho igual a 4, de acordo com a tabela acima, o maior preço que pode ser alcançado é através da sua divisão em duas partes de 2 polegadas, onde o preço total seria 10.

Implemente, utilizando programação dinâmica, a solução para o problema acima. Essa função deverá retornar o valor máximo que pode ser obtido a partir da divisão de uma haste de x polegadas, que não pode ser maior que o tamanho da tabela (por exemplo, se a tabela tem tamanho 10, a haste não pode ter tamanho maior que 10).

**Input Format:**

Na primeira linha, deve ser lido o tamanho da haste a ser cortado.

Na segunda linha deve ser lido um número inteiro representando o tamanho da tabela de preços (n).

Para cada uma das n próximas linhas, deve ser lido um número inteiro: preço do (i + 1)-ésimo corte.

Observação: é importante ressaltar que, na leitura do tamanho da tabela, a ordem de leitura do tamanho dos cortes é crescente e a diferença de tamanho entre os cortes catalogados é um. Por exemplo, se a tabela tiver tamanho 5, então haverá preços para tamanhos de cortes de: 1, 2, 3, 4 e 5.

**Output Format:**

Deve ser impresso o valor máximo que pode ser obtido pela divisão de uma haste.

# Backtracking e branch-and-bound - soma da subsequência máxima
Seja um arranjo composto por números inteiros, podendo ser positivos e/ou negativos. A subsequência máxima é aquela que tem o maior valor de soma entre todos os os seus elementos.

Por exemplo, dada a sequência a seguir: [10, -3, -30, 20, -3, -16, -23, 15, 23, -7, 12, -4, -25, 6].

A subsequência máxima é [15, 23, -7, 12], pois, de todas as subsequências possíveis, essa foi a que registrou a maior soma entre os seus elementos (43).

Implemente, utilizando a estratégia backtracking ou branch-and-bound, uma função que retorne o somatório da subsequência máxima.

**Input Format:**

Na primeira linha deve ser lido um número inteiro (n). Na segunda linha deve ser lida um vetor de números inteiros de tamanho n.

**Output Format:**

Somatório da subsequência máxima.

# Árvores binárias de busca - nós folhas
Implemente uma função que receba uma árvore binária de busca. A função deverá imprimir os nós folhas da árvore.

**Input Format:**

Na primeira linha deve ser lido o número inteiro N, que é referente à quantidade de nós da árvore binária de busca. Em seguida, em cada linha deve ser lido um número inteiro para ser inserido como nó na árvore (fazer isso até que N números sejam lidos).

**Output Format:**

Imprimir o valor da chave de cada nó folha em uma única linha.

Obs.: antes de imprimir cada chave, um espaço em branco deve ser impresso.

# Árvores binárias de busca - altura da árvore
Implemente uma função que receba uma árvore binária de busca. A função deverá retornar a altura da árvore.

**Input Format:**

Na primeira linha deve ser lido o número inteiro N, que é referente à quantidade de nós da árvore binária de busca. Em seguida, em cada linha deve ser lido um número inteiro para ser inserido como nó na árvore (fazer isso até que N números sejam lidos).

**Output Format:**

O valor da altura da árvore.

Lembre-se: a altura do nó raiz é zero.

# Árvores binárias de busca - nro de nós faltantes para árvore cheia
Implemente uma função que receba uma árvore binária de busca. A função deverá retornar a quantidade de nós que faltam para a árvore ser cheia.

**Input Format:**

Na primeira linha deve ser lido o número inteiro N, que é referente à quantidade de nós da árvore binária de busca. Em seguida, em cada linha deve ser lido um número inteiro para ser inserido como nó na árvore (fazer isso até que N números sejam lidos).

**Output Format:**

Imprimir a quantidade de nós que faltam para a árvore ficar cheia.

# Árvore AVL - soma dos fatores de balanceamento
Implemente uma função que receba uma árvore AVL como parâmetro. A função deverá retornar a soma dos fatores de balanceamento.

**Input Format:**

Na primeira linha deve ser lido o número inteiro N, que é referente à quantidade de nós da árvore AVL. Em seguida, em cada linha deve ser lido um número inteiro para ser inserido como nó na árvore (fazer isso até que N números sejam lidos).

**Output Format:**

Imprimir o resultado da soma dos fatores de balanceamento de todos os nós da árvore.

# Árvore rubro-negra - contar nós pretos ímpares
Implemente uma função que receba uma árvore rubro-negra. A função deverá retornar a quantidade de nós pretos que contém valor ímpar.

**Input Format:**

Na primeira linha deve ser lido o número inteiro N, que é referente à quantidade de nós da árvore. Em seguida, em cada linha deve ser lido um número inteiro para ser inserido como nó na árvore (fazer isso até que N números sejam lidos).

**Output Format:**

Quantidade de nós pretos ímpares

# Árvore B - contagem de páginas cheias
Implemente uma função que receba uma árvore B de ordem 5. A função deverá retornar um número inteiro representado a quantidade de páginas cheias.

**Input Format:**

Na primeira linha deve ser lido o número inteiro N, que é referente à quantidade de chaves que serão alocadas na árvore. Em seguida, em cada linha deve ser lido um número inteiro para ser inserido na árvore (fazer isso até que N números sejam lidos).

**Output Format:**

Imprimir o número de páginas cheias.

# Árvore B - Média entre todas as páginas folhas
Implemente uma função que receba uma árvore B de ordem 5. A função deverá retornar um número inteiro representado valor médio entre os elementos de todas as páginas folhas.

**Input Format:**

Na primeira linha deve ser lido o número inteiro N, que é referente à quantidade de chaves que serão alocadas na árvore. Em seguida, em cada linha deve ser lido um número inteiro para ser inserido na árvore (fazer isso até que N números sejam lidos).

**Output Format:**

Imprimir a média dos valores da chave.

# Grafos - lista de adjacência para matriz de adjacência
Implemente uma função que receba um grafo representado por uma lista de adjacência e o converta para uma matriz de adjacência.

**Input Format:**

A primeira linha contém o número de vértices seguida pela respectiva lista de adjacência.

Nas próximas linhas, onde cada uma é referente a um vértice v_i, enquanto o número "-1" (menos um) não for lido, ler os vértices adjacentes.

Por exemplo, suponha que o i-ésimo vértice seja adjacente aos vértices 2 e 5, então a leitura deve seguir o seguinte formato:

2 5 -1

Caso o vértice não tenha adjacentes, basta ler -1 (menos 1). Exemplo:

-1

**Output Format:**

Matriz de adjacência impressa.

# Grafos - direcionado ou não direcionado
Implemente uma função que receba um grafo representado por uma lista de adjacência e verifique se é direcionado ou não.

**Input Format:**

A primeira linha contém o número de vértices seguida pela respectiva lista de adjacência. Cada uma das seguintes linhas será referente a um vértice v_i, onde os vértices adjacentes devem ser lidos. Para cada linha, enquanto o número "-1" (menos um) não for lido, um vértice adjacente deve ser lido. Por exemplo, suponha que o i-ésimo vértice seja adjacente aos vértices 2 e 5, então a leitura deve seguir o seguinte formato:

2 5 -1

Caso o vértice não tenha adjacentes, basta ler -1 (menos 1). Exemplo:

-1

**Output Format:**

Imprimir direcionado ou nao direcionado

# Grafos - busca em largura (listas de adjacências)
Implemente o algoritmo de busca em largura para grafos. Esse algoritmo deve ter dois parâmetros: um grafo e um número inteiro, sendo este último o vértice raiz da árvore de busca em largura, ou seja, é o vértice a partir de onde deve ser iniciado a exploração do grafo. Após, para cada vértice, imprima os respectivos pai e distância.

Para a implementação, considere o grafo representado por lista de adjacências, conforme as estruturas apresentadas abaixo:

    typedef struct {
        int V; // número de vértices
        int A; // número de arestas
        Lista **adj; // lista de adjacências
    }GrafoLA;

    typedef struct Cell Cell;

    struct Cell{
        int key;
        Cell *next;
    };
    
    typedef struct{
        Cell *head;
    }Lista;
**Input Format:**

A primeira linha contém o número de vértices seguida pela respectiva lista de adjacência. Cada uma das seguintes linhas será referente a um vértice v_i, onde os vértices adjacentes devem ser lidos. Para cada linha, enquanto o número "-1" (menos um) não for lido, um vértice adjacente deve ser lido. Por exemplo, suponha que o i-ésimo vértice seja adjacente aos vértices 2 e 5, então a leitura deve seguir o seguinte formato:

2 5 -1

Caso o vértice não tenha adjacentes, basta ler -1 (menos 1). Exemplo:

-1

Na última linha deve ser lido um número inteiro que representa um vértice do grafo para iniciar a aplicação do algoritmo de busca em largura.

**Constraints:**

O não uso do TAD de lista de adjacências acerratará em 75% de desconto da nota, já que a versão com matriz de adjacências é implementada em aula.

**Output Format:**

Na primeira linha deve ser impressa a seguinte sequência de caracteres: "v d p".

A partir da próxima linha, imprimir o vértice, o pai e a distância.

Para cada vértice que não tem pai, deve ser impresso "-" em sua respectiva linha.

Para cada vértice que não foi possível ser descoberto a partir do "vértice raiz", também deve ser impresso o caractere "-". Por exemplo: se o vértice x não pode ser descoberto, na sua linha deve ser impresso "x - -"

# Grafos - busca em profundidade (listas de adjacências)
Implemente o algoritmo de busca em profundidade para grafos. Para a representação do grafo, você pode usar matriz ou lista de adjacências. A aplicação do algoritmo deve começar pelo vértice 0.

Para a implementação, considere o grafo representado por lista de adjacências, conforme as estruturas apresentadas abaixo:

    typedef struct {
        int V; // número de vértices
        int A; // número de arestas
        Lista **adj; // lista de adjacências
    }GrafoLA;

    typedef struct Cell Cell;

    struct Cell{
        int key;
        Cell *next;
    };
    
    typedef struct{
        Cell *head;
    }Lista;
**Input Format:**

A primeira linha contém o número de vértices seguida pela respectiva lista de adjacência. Cada uma das seguintes linhas será referente a um vértice v_i, onde os vértices adjacentes devem ser lidos. Para cada linha, enquanto o número "-1" (menos um) não for lido, um vértice adjacente deve ser lido. Por exemplo, suponha que o i-ésimo vértice seja adjacente aos vértices 2 e 5, então a leitura deve seguir o seguinte formato:

2 5 -1

Caso o vértice não tenha adjacentes, basta ler -1 (menos 1). Exemplo:

-1

**Constraints:**

O não uso do TAD de lista de adjacências acerratará em 75% de desconto da nota, já que a versão com matriz de adjacências é implementada em aula.

**Output Format:**

Na primeira linha deve ser impressa a seguinte sequência de caracteres: "v d f p".

Para cada uma das próximas linhas, imprimir um vértice (em ordem crescente), o momento da sua descoberta, o momento da sua finalização e o seu respectivo pai.

Para cada vértice que não tem pai, deve ser impresso "-" em sua respectiva linha.

# Grafos - árvore geradora mínima (listas de adjacência)
Implemente o algoritmo de Prim. A função deve receber um grafo representado por uma lista de adjacência e construir uma árvore geradora mínima, que deve ser construída a partir do vértice "0".

Para a implementação, considere o grafo representado por lista de adjacências, conforme as estruturas apresentadas abaixo:
   
    typedef struct {
        int V; // número de vértices
        int A; // número de arestas
        Lista **adj; // lista de adjacências
    }GrafoLA;

    typedef struct Cell Cell;

    struct Cell{
        int key;
        Cell *next;
    };
    
    typedef struct{
        Cell *head;
    }Lista;
**Input Format:**

A primeira linha contém o número de vértices. A segunda linha contém a quantidade de arestas (A). Para cada uma das "A" próximas linhas devem der lidos dois números inteiros. sendo os 2 primeiros, a aresta, e o último, o peso da aresta.

**Constraints:**

O não uso do TAD de lista de adjacências acerratará em 75% de desconto da nota, já que a versão com matriz de adjacências é implementada em aula.

**Output Format:**

Imprimir a árvore geradora mínima. Cada linha deve ser impressa no seguinte formato: "v_i: pai[v_i]".

Para o vértice da árvore que não tiver "pai", deve ser impresso o caractere "-" (traço/sinal de menos). Como o algoritmo deve ser iniciada a partir do vértice "0", então a primeira linha sempre será "0: -"

# Grafos - caminhos mínimos (listas de adjacência)
Implemente o algoritmo de Dijkstra. A função deve receber um grafo representado por uma lista de adjacência e construir uma árvore de caminhos mínimos, que deve ser construída a partir do vértice "0".

Para a implementação, considere o grafo representado por lista de adjacências, conforme as estruturas apresentadas abaixo:
   
    typedef struct {
        int V; // número de vértices
        int A; // número de arestas
        Lista **adj; // lista de adjacências
    }GrafoLA;

    typedef struct Cell Cell;

    struct Cell{
        int key;
        Cell *next;
    };
    
    typedef struct{
        Cell *head;
    }Lista;
**Input Format:**

A primeira linha contém o número de vértices. A segunda linha contém a quantidade de arestas (A). Para cada uma das "A" próximas linhas devem der lidos dois números inteiros. sendo os 2 primeiros, a aresta, e o último, o peso da aresta.

**Constraints:**

O não uso do TAD de lista de adjacências acerratará em 75% de desconto da nota, já que a versão com matriz de adjacências é implementada em aula..

**Output Format:**

Imprimir a árvore de caminhos mínimos. Cada linha deve ser impressa no seguinte formato: "v_i: pai[v_i]".

Para o vértice da árvore que não tiver "pai", deve ser impresso o caractere "-" (traço/sinal de menos). Como o algoritmo deve ser iniciada a partir do vértice "0", então a primeira linha sempre será "0: -"
