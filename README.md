# SharedTable

*1
  *no exemplo nomeado como sharedTable, a race condition ocorre de modo queo resultado gerado édiferente do esperado, isso ocorre porque no método addMark, os valores são inseridos de modo paralelo, o que causa uma inconsistência de dados, fazendo com que alguma parte deles, seja perdida, por exemplo, o programa pode estar tentando inserir A e B ao mesmo tempo, mas apenas um dos valores vai ser inserido, pra solucionar isso usamos a palavra reservada synchronized, para que naquele método quando ocorrer isso, apenas um insira por vez, evitando o conflito
  
  ![SharedTable errado](resultadoErrado.png)
  aqui vemos que no momento em que ocorre a concorrência ele insere um '-' em vez da letra, nesse caso ocorreu duas vezes, e tanto A quanto B ficaram com 19 ocorrências
  
  ![SharedTable errado](resultadoErrado.png)
  aqui foi usado o synchronized, ou seja, o resultado foi como o esperado

*2
 *Nunca tive um contato com programação concorrente, pensando em um sistema grande, não vejo de maneira simplescomo implementar essa parte, em um sistema que dependa de resultados gerados pela programção concorrente, como faço com que ela passe a ser sequencial a partir de um ponto.
