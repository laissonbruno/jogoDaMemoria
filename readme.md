# Explicação do código

O código é um jogo de memória, onde o objetivo é encontrar todos os pares de cartas iguais. O jogo foi desenvolvido em JavaScript, HTML e css.

## Variáveis

No início do código, são declaradas algumas variáveis: 
- `grid`: variável que armazena o elemento HTML com a classe `grid`; 
- `spanPlayer`: variável que armazena o elemento HTML com a classe `player`; 
- `timer`: variável que armazena o elemento HTML com a classe `timer`; 
- `characters`: array que contém os nomes dos personagens do jogo; 
- `firstCard` e `secondCard`: variáveis que armazenam as duas cartas selecionadas pelo jogador. 

 ## Funções

 Além das variáveis, são declaradas algumas funções no código: 

 - **createElement**: função responsável por criar um elemento HTML com uma determinada tag e classe; 

 - **checkEndGame**: função responsável por verificar se todas as cartas foram descobertas pelo jogador. Se sim, exibe uma mensagem de parabéns e recarrega a página; 

 - **checkCards**: função responsável por verificar se as duas cartas selecionadas pelo jogador são iguais. Se sim, ela adiciona a classe `disabled_card`, caso contrário remove a classe `reveal_card`. Esta função também chama a função checkEndGame para verificar se todas as cartas foram descobertas; 

 - **revealCard**: função responsável por revelar as cartas quando ela é clicada pelo jogador. Ela também adiciona a classe `reveal_card`. Se já houver duas cartas reveladas, ela chama a função checkCards para verificar se elas são iguais;  

 - **createCard**: função responsável por criar uma carta com um determinado personagem. Ela recebe com parâmetro o nome do personagem e retorna um elemento HTML contendo uma div com duas faces (front e back). A face front possui uma imagem referente aquele personagem;  

 - **loadGame**: função responsável por carregar o jogo na tela. Ela duplica os personagens no array characters e embaralha os itens usando sort(). Em seguida, percorre o array embaralhado e chama a função createCard para criar as cartas na tela;  

 - **startTime**: função responsável por iniciar o timer do jogo. Ela usa setInterval() para incrementar o tempo em 1 segundo (1000 milisegundos).  

 ## window.onload  

 Por fim, temos window.onload(), que é executado quando todos os elementos da página foram carregados. Esta função atribui à variável spanPlayer o nome do jogador salvo no localStorage (localStorage.getItem('player')), inicia o timer (startTime()) e carrega o jogo na tela (loadGame()).