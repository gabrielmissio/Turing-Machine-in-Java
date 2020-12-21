# Turing-Machine-in-Java
<br>
<br>
*Sintax padrão*

<br><p>Caracter '$' é reservado para informar a maquina a continuar com o valor atual
<br><p>Sempre apos passar uma sequencia de parametros e acoes é necessario colocar '&' no final da linha
<br><p>Apos a escrita de um estado é necessario colocar ';' no final da linha
<br><p>exemplo de codigo:<br>
<br>NomeDoEstado:
	<br><parametro1, parametro2> write caractere, proximo_movimento, proximo_estado&
	<br><parametro3, parametro4> write $_mantem_caractere_ataual, proximo_movimento, proximo_estado&;

<br>
<br>
*Codigo para somar 1 a um numero binario*
<br>Imput: numero binario (ex.: 1011)
<br>Estado inicial: estadoIrParaDireita
<br>Posicao inicial: 0
<br>Codigo:

<br>estadoIrParaDireita:
<br>	<1,0> write $, direita, estadoIrParaDireita&
<br>	< > write *, esquerda, estadoCarregar&;
<br>
<br>estadoCarregar:
<br>	<0, > write 1, esquerda, terminei&
<br>	<1> write 0, esquerda, estadoCarregar&;
