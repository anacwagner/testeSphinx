Aula 6
======

.. code:: ipython3

    # Importando as bibliotecas
    from math import *

.. code:: ipython3

    sqrt(639*8)-int(sqrt(639*8))




.. parsed-literal::

    0.49825172687791053



**EXERCÍCÍO 1:** Criar uma função para verificar se um número é
triangular ou não.

Um número “x” é triangular se o resultado da expressão

.. math:: \frac{\sqrt{8x+1}-1}{2}

é um número inteiro.

.. code:: ipython3

    def tri(x):
        n=(sqrt(8*x+1)-1)/2
        if n-int(n)==0:
            saida=True #é um número triangular
        else:
            saida=False #não é um número triangular
        return saida
        

.. code:: ipython3

    tri(4)




.. parsed-literal::

    False



**EXERCÍCÍO 2:**

No calendário Gregoriano, é possível usar fórmulas para saber o dia da
semana correspondente a uma data. Sendo :math:`d` o número
correspondente ao dia, :math:`m` o número correspondente ao mês e
:math:`a` o número correspondente ao ano (escrito com quatro
algarismos), o dia da semana :math:`DS` (1=segunda, 2=terça, …),
correspondente à data **dd/mm/aaaa** é dado pela seguinte sequência:

:math:`y=a-\frac{14-m}{12}`;

:math:`x=y+\frac{y}{4}-\frac{y}{100}+\frac{y}{400}`

:math:`k=m+12\cdot \frac{14-m}{12}-2`;

:math:`N=d+x+\frac{31\cdot k}{12}`

**DS** = resto da divisão de :math:`N` por 7

**Obs.:** Nestes cálculos, deve-se pegar apenas a parte inteira do
resultado de cada divisão!

.. code:: ipython3

    def diadasemana(d,m,a):
        y=a-(14-m)//12
        x=y+y//4-y//100+y//400
        k=m+12*((14-m)//12)-2
        n=d+x+(31*k)//12
        ds=n%7
        if ds==0:
            dia="Domingo"
        elif ds==1:
            dia="Segunda"
        elif ds==2:
            dia="Terça"
        elif ds==3:
            dia="Quarta"
        elif ds==4:
            dia="Quinta"
        elif ds==5:
            dia="Sexta"
        elif ds==6:
            dia="Sábado"
        return dia

.. code:: ipython3

    diadasemana(29,6,1965)




.. parsed-literal::

    'Terça'



.. code:: ipython3

    x=float(input("Digite um número: "))
    print(x)


.. parsed-literal::

    Digite um número: 1
    1.0


Comando de repetição: ``while``
-------------------------------

A estrutura ``while`` repete um bloco de instruções enquanto uma
condição for verdadeira. Quando o resultado dessa condição passa a ser
falso, a execução do *loop* é interrompida.

Estrutura: em Python, para indicarmos o bloco de intruções pertencentes
ao ``while``, devemos apenas indentar o código.

.. code:: python

   while condicao == verdadeira:
       # enquanto a condiçao é verdadeira, a seguinte sequência de comandos são executadas 
       <comando_1>
       <comando_2>
       ...
       <comando_n>

Para utilizar o comando ``while`` corretamente devemos:

1. Antes do comando, inicializar a variável de controle.

2. Criar uma condição que utiliza essa mesma variável de controle.
   Enquanto essa condição for verdadeira, as instruções dentro do
   ``while`` serão executadas. Atente-se ao fato de que é essa variável
   de controle que irá garantir que a condição se mantenha verdadeira
   pelo número correto de iterações necessárias.

3. Lembrar de modificar/atualizar a variável de controle para garantir
   uma condição de parada. A falta desta etapa faz com que o seu
   programa entre no que chamamos de *loop infinito*. Evite que isto
   aconteça, pois leva ao congelamento do programa e, no nosso caso,
   consequentemente do notebook (normalmente a célula fica com o
   seguinte símbolo do lado esqeurdo quando fica rodando **[*]**).

Por exemplo,

.. code:: python

   contador = 0 #1.variável de controle
   while contador < 5: #2.condição de parada
       print(contador)
       contador = contador + 1 #3.incremento da variável de controle

.. code:: ipython3

    def repeticao():
        x="inicio" 
        while x!="": 
            x=(input("Digite alguma coisa: "))
            print (x)

.. code:: ipython3

    repeticao()


.. parsed-literal::

    Digite alguma coisa: fdzbsfdfs
    fdzbsfdfs
    Digite alguma coisa: 
    


Na função ``repeticao()``, enquanto digitamos algo no ``input`` a função
fica se repetindo. Quando a condição de parada é atingida, ou seja,
quando no ``input`` você não digita nada e aperta ENTER, a função
termina de ser executada.

.. code:: ipython3

    def repeticao2():
        #Faz print dos números informados no input
        x=0
        digitou="sim"
        while digitou=="sim":
            n=input("Digite um número: ")
            if n!="":
                x=float(n)
                print(x)
            else:
                digitou="nao"

.. code:: ipython3

    repeticao2()


.. parsed-literal::

    Digite um número: 3
    3.0
    Digite um número: 


Na função ``repeticao2()``, você consegue identificar a variável de
controle e a condição de parada?

--------------

**DEVER DE CASA:**

Criar a função ``repeticao3()`` que modifica a função ``repeticao2()``
para fazer a soma dos números informados no ``input``. \__\_

