#Jogo da adivinhação 

Criar um jogo que escolhe um número aleatório entre 1 e 100, e desafia o jogador a adivinhá-lo.
#Fase 1

Criar o jogo, onde o jogo precisa ser iterativo na linha de comando.
Ele vai ter o valor 42 como número fixo para adivinhação, o valor do chute vai receber através do terminal digitando no teclado.

Caso o jogador de um valor menor, exibir a mensagem "O número é maior!", caso o jogador de um valor maisalto, exibir a mensagem "O número é menor!" e caso ele coloque o número correto exibir a mensagem "Parábens você venceu!".

Quando terminar um jogo o programa precisa encerrar.


## Fase 2
Criar testes para o jogo usando alguma framework de testes dependendo da linguagem.

Casos de testes:

1 - Colocar o número 40 e receber a mensagem "O número é maior!"

2 - Colocar o número 45 e receber a mensagem "O número é menor!"

3 - Colocar o número 42 e receber a mensagem "Parábens você venceu!"


## Fase 3
Criar um menu em texto com as opções:

1 - Mudar número secreto

2 - Jogar

3 - Sair

Só sair quando criar a opção 3 ou seja criar um loop.

Limpar a tela quando finalizar um jogo.

Mover a lógica do jogo para uma função pra ficar fora da função do loop.

Casos de testes:

- Testar a lógica do jogo passando um número secreto por parametro.

## Fase 4
Criar tela de bem vindo antes de exibir o menu do jogo conforme mensagem abaixo:

"Bem-vindo	ao	jogo	da	adivinhação"


Quando iniciar um jogo pedir o nome conforme a mensagem abaixo:

"Por favor digite o seu nome"
Receber o nome do jogador


Exibir a mensagem de inicialização do jogo:

"Vamor começar o jogo pra você {nome do jogador}"


Para cada tentativa exibir uma mensagem com o numero da tentativa.

"Tentativa 1"

"Tentativa 2"

"Tentativa 3"

## Fase 5 - Arrays

Colocar um limite de tentativas de acertar o número para 5. Por conta disso vamos verificar se um número já foi digitado anteriormente naquele jogo.

Casos de teste:
- Testar a função do jogo para fazer 5 tentativas caso não acertar retornar o game over do jogo.
- Tentar inserir duas vezes o mesmo número do jogo, deve retornar um erro de tentativas.

Requerimentos:
- Guardar tentativas num array ou similar
- A função de lógica do jogo só deve retornar o resultado do jogo ou alguma excessão.

## Fase 6 - Pontuação

O jogo vai inicar com 200 pontos, para cada tentativa que o usuário fizer e não acertar ele perde parte desses pontos.

Por	exemplo, se o número é o 75 e ele chuta	15,	ele	errou por 60, então	o jogador perde	30 pontos. Isto	é, ele perde a diferença entre os dois números dividida	por	dois.
A cada novo	chute, calculamos a	diferença que erramos, chute menos o numero_secreto:
```
pontos_a_perder	= chute	- numero_secreto
```
Agora queremos dividir (/) este	valor por 2:
```
pontos_a_perder	= chute	- numero_secreto / 2
```
Por	fim, tiramos dos pontos	até	agora os pontos	a perder:
```
pontos_ate_agora = pontos_ate_agora	- pontos_a_perder
```
Quando o usuário acertar o número, mostrar a pontuação que ele conseguiu.

Caso de testes:
- Definir o número 75 como número secreto e chutar o número 15 e verificar se a pontuação diminuiu para 140. 
- Definir o número 75 como número secreto e chutar o número 76 e verificar se a pontuação diminuiu para 199.5. 
- Definir o número 75 como número secreto e chutar o número 74 e verificar se a pontuação diminuiu para 199.5. 
- Definir o número 75 como número secreto e chutar o número 75 e verificar a mensagem de fim de jogo com a pontuação 200.
- Definir o número 75 como número secreto e chutar o respectivamente o número 65 e 75 e verificar a mensagem de fim de jogo com a pontuação 190.

Requerimentos:
- A pontuação tem que aceitar ponto flutante (ex:. 199.5, 144.75 e etc) 
- A perda de pontos para um chute maior ou menor sempre tem que ser a diferença ou seja se ele perde 10 pontos independente se o chute foi pra um número maior ou menor.
