# snakeJS

Troisième projet réalisé (12/2022) lors de la formation JavaScript sur Dyma.fr. Ce projet utilise la WebApi 'Canvas'.

Fonctionnement: 
- Le Canvas (800px / 800px) est divisé en cellules de 40px / 40px.
- Les coordonnées sont des nombres entre 0 et 19, elles sont ensuite multipliées par 40 pour être représentées sur le canvas.
- Les coordonnées du snake sont stockées dans un tableau de tableaux de coordonnées (ex: [[X,Y], [X,Y], [X,Y]]).
- Les coordonnées de la pomme ([X,Y]) sont générées aléatoirement via une fonction Math.round(Math.random() * 19), si celle ci correspond à un des tableau présent dans le snake, alors la fonction est re-éxécutée.
- Le snake se déplace dès qu'une ArrowKey est utilisée, puis le jeu s'actualise toute les 800ms et est réduit de 5ms à chaque pomme mangée.
- La direction du snake est stockée dans un variable let qui est passée en argument de la fonction moveSnake(), cette fonction ajoute un nouvel élément au début du tableau de coordonnées de snake et les valeurs sont comparées à celle de la pomme et au corps de snake.
- Si les valeurs de la tête de snake correspondent à celle de la pomme, alors une nouvelle pomme est générée et l'actualisation s'accélère de 5ms.
- Si les valeurs de la tête de snake correspondent à la position d'un élément de son corps ou est en-dehors du canvas, alors Game Over, le jeu ne s'actualise plus et un click souris est nécessaire pour le ré-initialiser.
- Si les valeurs de la tête ne correspondent pas à la pomme ou au corps, alors le dernier élément du tableau de snake est retiré et le jeu continue.
