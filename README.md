# ApiRestRobot
Projeto Api Rest Robot:
  Api que simula a movimentação de um robo.

Desenvolvimento:
  - Projeto desenvolvido em aspnet core com C#
  - Teste da api

Utilização da api:
 - GET: http://localhost:8080/rest/mars
 - POST: http://localhost:8080/rest/mars/MML

Decrição dos métodos:
 - Esta api possui dois métodos um get e um post
    # Método get somente apresentação.
    # Método post para movimentação.

Movimento do robo:
 - Ele se movimenta num espaço de 5x5
 - Saindo desde espaço api retorna o erro 400
 - Usando os comandos:
    # M para a movimentação de um 'passo' na direção da face;
    # R ou L para a direção de rotação.
 - A execução dos comando é realizada conforme a ordem informada.
 - Cada chamada do Post, se estiver correto os comandos, retorna a localização do robo (x, y, F). F = face
 - O ínicio sempre será (0 ,0 , N)
 - O robo anda somete pra frete, caso queira mudar a direção, deve mudar a face. Para mudar a face use os comandos de direção (R ou L)  
 - Informar comandos não aceitos retorna o erro 400
 
 Alguns exemplos POST:
  - Chamada: http://localhost:8080/rest/mars/MMMMRMM
  - Retorno: (2, 4, E)
  
  - Chamada: http://localhost:8080/rest/mars/MMRMML
  - Retorno: (2, 2, N)
  
  - Chamada: http://localhost:8080/rest/mars/LMM
  - Retorno: 400 Bad Request
  
  - Chamada: http://localhost:8080/rest/mars/MMRMMLMMMM
  - Retorno: 400 Bad Request
  
 
 
