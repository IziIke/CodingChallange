# CodingChallange

>Primeiramente quero agradecer a equipe Let´s Code por este desafio que me proporcionou uma experiencia unica de busca e crescimento.

__________________________________________________________________________________________________
# Falando um pouco sobre o sistema

>Usei a linguagem Java com o framework Spring Boot, pois achei a melhor forma de fazer uma api com segurança onde também consegui trabalhar a parte das permissões com o Spring Security. 

>Na classe SecurityConfiguration é onde acabo dando as permissões, por isso existe um numero grande de controllers, pois aproveitei essa ferramenta para dar prioridades.

>Não consegui infelizmente fazer a ligação de algumas tabelas, então as partes de comentário, like e nota ficou mais como uma demonstração.

__________________________________________________________________________________________________

# Como utilizar a API

>Observação 1: Eu utilizei o postman para poder fazer o teste da minha API

>Observaçâo 2 : como não tem o processo de cadastro estou subindo usuarios padrões, são:

.Administrador -> login: admin, senha: password

.Leitor -> login: leitor, senha: password

.Basico -> login: basico, senha: password

.Avançado -> login: avancado, senha: password
__________________________________________________________________________________________________

>Caso não seja feito o login não ira funcionar nenhum end point.

__________________________________________________________________________________________________

>Para pesquisa de filmes temos duas maneiras, utilizando o metodo GET:

.pesquisando toda a lista : http://localhost:8080/filme?nome= [nome do filme]

.essa outra maneira traz o primeiro filme da lista : http://localhost:8080/filme/primeiro?nome= [nome do filme]

>Essa pesquisa pode ser feita por qualquer usuario.

__________________________________________________________________________________________________
>Observação 3: Não consegui colocar chave estrangeira do filme as minhas tabelas, então deixei como uma simulação...


>Para verificar notas, pelo GET :  http://localhost:8080/api/rating 

>Para dar nota nota, pelo Post : http://localhost:8080/api/rating

EX:
{
    "filmname" : "StarWars iv",
    "rating" : 10
}

.sempre passando pelo formato .JSON

__________________________________________________________________________________________________

>Para verificar comentarios, pelo GET : http://localhost:8080/api/coment

>Para dar nota (com execção do usuario leitor), pelo Post : http://localhost:8080/add/coment
 Ex:
{
    "filmname":"Batman Begins",
    "coment": "Melhor serie de filme de heroi."
}

.sempre passando pelo formato .JSON

__________________________________________________________________________________________________

>Para verificar likes, pelo Get: http://localhost:8080/api/like
    onde true = gostei e false = não gostei

>Para dar likes ou dislikes, pelo Post: http://localhost:8080/add/like
Ex:
{
 "filmname":"Lord of the Rings",
  "ylike": true/false
}

.sempre passando pelo formato .JSON

    
__________________________________________________________________________________________________


>Caso queira excluir comentarios, pelo DELETE (exclusivo ADM): http://localhost:8080/del/coment/ [numero do id do comentario].

__________________________________________________________________________________________________

> caso queira ver o banco de dados entre no link : http://localhost:8080/h2-console

.JDBC URL: jdbc:h2:mem:test_job
.User Name: sa
__________________________________________________________________________________________________


Obrigado novamente pela a experiencia e por esse processo seletivo incrivel! 


__________________________________________________________________________________________________



