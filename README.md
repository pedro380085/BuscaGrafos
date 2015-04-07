Lab 02 - SCC0216 - ICMC-USP
==============

O conteúdo abaixo foi obtido diretamente do [run.codes](http://run.codes).

Esse trabalho é referente ao laboratório 2 de Modelagem de Grafos para a Turma SCC0216 do ICMC-USP. O mesmo descreve como realizar a busca em um grafo e obter o menor caminho entre diferentes pontos.


Especificação
==============
O laboratório consiste na implementação de busca em dígrafos não-ponderados. Deverá
ser utilizada a linguagem de programação C. As buscas consideradas são as buscas em largura
e em profundidade.
O programa principal deverá ler da entrada padrão a lista de arestas do dígrafo e representá-
lo em memória – matriz ou lista de adjacência, conforme desejar. Em seguida, o programa
deverá ler instruções, encontrar um caminho entre dois vértices através de determinada tipo de
busca e imprimir o resultado na saída padrão.
Na primeira linha da entrada, haverá o descritor do dígrafo contendo 2 números separados
por espaço. Os números indicam, nesta ordem, o número de vértices e de arestas do dígrafo.
Nas linhas seguintes, as arestas do dígrafo serão representadas por dois números indicando os
vértices de origem e de destino.
Por fim, as buscas serão representadas por duplas contendo o vértice de origem e o vértice
de destino. Para cada instrução, o programa deverá realizar a busca e imprimir o caminho
encontrado (se existir) entre os vértices de origem e de destino. O caminho deverá ser impresso
contendo o índice do vértice de origem, os índices dos vértices intermediários e, por fim, o índice
do vértice de destino. Caso não exista caminho entre os vértices, deixe a linha em branco.
Por exemplo, a entrada1
6 8 // 6 vé rtices e 8 arestas
0 1
0 5
1 2
1 3
2 3
2 4
3 4
3 5
4 0 // instru ções come çam aqui
0 0
0 4
0 5
1Os comentários são apenas descritivos. Estes não existirão nas entradas e nem deverão ser impressos como
saída.
1
resultará no dígrafo
●
●
●
●
● ●
0
1
2
3
4 5
Partindo o vértice 0, as árvores geradas, respectivamente, pelas buscas em largura e em
profundidade são
●0
●
● ●
●
1
2 3
4
●5
●
●
●
●
● ●
0
1
2
3
4 5
Deste modo, utilizando a busca em largura, o programa terá como saída
// de 4 para 0, não há caminhos
0 // de 0 para 0 , já est á no vé rtice de destino
0 1 2 4
0 5 // caminho de 0 para 5 encontrado na busca em largura
ou, utilizando a busca em profundidade, a saída
// de 4 para 0, não há caminhos
0 // de 0 para 0 , já est á no vé rtice de destino
0 1 2 3 4
0 1 2 3 5 // caminho de 0 para 5 encontrado na busca em profundidade
2
2 Submissão
O exercício deverá ser entregue pelo sistema run.codes2
. Os alunos deverão submeter seus
códigos no exercício 2 - Busca em Largura ou no exercício 2 - Busca em Profundidade
até o final da aula. Os alunos deverão escolher entre uma das buscas e submeter o código no
exercício correspondente.
Somente a última submissão será considerada. Todas as demais submissões
serão desconsideradas, incluindo aquelas dentro do período normal de submissão.
Os exercícios deverão submetidos em um arquivo .zip contendo código-fonte do programa e
um Makefile para compilação e teste do trabalho. Se necessário, incluam no .zip um arquivo
chamado readme com informações extras.
Os códigos deverão ser compilados pelo compilador gcc com a flag -std=c99. A não conformidade
das implementações com a versão C estabelecida acarretará em nota zero.
Atenção! Todos os códigos enviados passarão pelo sistema de veri-
ficação de plágio. Se forem identificados códigos duplicados, todos os
alunos envolvidos receberão nota zero.
3 Correção e Avaliação
As implementações serão avaliadas por meio de casos de testes, com peso 7, e pela legibilidade
e boas práticas de programação, com peso 3. Cada aluno poderá optar por implementar
apenas uma das buscas. Será considerado para correção apenas a submissão com maior pontuação
nos casos de teste.
Os seguintes casos implicarão em nota zero:
• não conformidade com a versão C99;
• programas não estruturados como um TAD; e
• exercícios plagiados.
4 Dicas
• Utilizem o vetor antecessor (consulte o material de aula) para encontrar o caminho até
um vértice.
• O sistema considerará que a expansão dos nós são feitas por ordem do índice, portanto,
se utilizarem lista de adjacência, mantenha a lista de vértices adjacentes ordenada.
• Utilizem o TAD fila (do semestre passado) para implementar a busca em largura.