# pacman
Trabalho de Inteligencia Artificial
Aluno: Ibrai Jose Aguzzoli
Mat: 171030319

Objetivo do projeto é implementar tipos de buscas para o PAC-MAN encontrar comida e/ou melhor caminho em diferentes labirintos que são gerados a partir de comandos.

1-Comando para busca DFS

python pacman.py -l tinyMaze -p SearchAgent 

python pacman.py -l mediumMaze -p SearchAgent 

python pacman.py -l bigMaze -z .5 -p SearchAgent

Video DFS: https://drive.google.com/open?id=1ljKNqNtz37oLtCWDfBQFwVyko9XnuwAk

https://youtu.be/2BwKBsYswNs


2-Comando BFS

python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs 

python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5

Video BFS: https://drive.google.com/open?id=1CXJezEWesASz8jk5hcHm1BeRvF8bNAPy

https://youtu.be/kWG_gfqmuvA



3-Comando UCS

python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs

python pacman.py -l mediumDottedMaze -p StayEastSearchAgent 

python pacman.py -l mediumScaryMaze -p StayWestSearchAgent

Video UCS: https://drive.google.com/open?id=1dp6nRxGhwi01obiGJaBWEXKAEviMIk8X

https://youtu.be/g4IFroXmcD4


4-Comando A* search

python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic 

python pacman.py -l testSearch -p AStarFoodSearchAgent

Video A* search: https://drive.google.com/open?id=1u4Y2Q-EEaJPjmJWM0fZRTVW_MYb21XxP

https://youtu.be/_YYWro-0kPI

python pacman.py -l trickySearch -p AStarFoodSearchAgent

Video A* search: https://drive.google.com/open?id=18RqFTupt9AWCRe8miSTfxF67m63rGsXw

https://youtu.be/Pi0EAZWKIho


PERGUNTAS

Pergunta 1

A ordem de exploração foi de acordo com o esperado? 

R= Sim, para o labirinto grande. Já para o médio poderia ter encontrado um caminho mais curto/rápido e no pequeno
é indiferente o caminho.

O Pacman realmente passa por todos os estados explorados no seu caminho para o objetivo?

R = Não, ele define uma melhor rota de acordo com seus cálculos para seguir seu objetivo.

Pergunta 2

Essa é uma solução ótima? 

R= Não tendo em vista o labirinto médio.

Senão, o que a busca em profundidade está fazendo de errado?

R= Neste caso, do labirinto médio, ele usa a rota que mais ocorreu em resultado de busca, e não a mais curta.

Pergunta 3

A busca BFS encontra a solução ótima?

R= sim, em relação ao DFS, o mesmo executa uma rota com mais curta.

Senão, verifique a sua implementação. 


Pergunta 4

O que acontece em openMaze para as várias estratégias de busca? 

R= No DFS ele passa pela maioria dos estados explorados, no BFS já é mais eficiente. Em UCS, a orientação de seguir pela esquerda
ou direita faz com que otimize o caminho pela orientação dada. Pelo ASEARCH ele percorre distâncias mais  curtas (retas) até chegar
no seu objetivo.
