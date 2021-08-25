******
Aula 1
******

Condicionais
============

Estrutura IF
------------

Executa o bloco de comandos indentados (tabullados - tab) se a condição (expressão lógica) é verdadeira (1 / True).

.. code-block:: python

    if condicao:
        |
        | bloco de comandos
        |

Note que o uso do **else** não é obrigatório!

Estrutura IF-ELSE
-----------------

Se a condição for verdadeira (= 1 / True) executa apenas o bloco de comandos $0$. Se a condição for falsa (0 / False) executa apenas o bloco de comandos $1$.

.. code-block:: python

    if condicao:
        |
        | bloco de comandos 0
        |
    else:
        |
        | bloco de comandos 1
        |


Estrutura IF-ELIF-ELSE
----------------------

As condições são testadas em ordem, uma após outra. Apenas o bloco de comandos correspondente a primeira condição que for verdadeira será executado. O bloco de comandos associados ao `else` será executado apenas se todas as condições anteriores forem falsas. Não é obrigatório que haja um `else` ao final. O `elif` funciona como um novo `if` dentro do `else`, em que o Python combina **else** e **if** e o torna uma declaração condicional **elif**. 


.. code-block:: python

    if condicao_0:
        |
        | bloco de comandos 0
        |
    elif condicao_1:
        |
        | bloco de comandos 1
        |
    elif condicao_2:
        |
        | bloco de comandos 2
        |

    elif ...:

    elif condição_k:
        |
        | bloco de comandos k
        |
    else:
        |
        | bloco de comandos k+1
        |


.. LeetCode
.. ========

.. Happy Number
.. ------------

.. How to Approach such Problem
.. ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. `Happy number <https://leetcode.com/problems/happy-number/>`_ is a medium leetcode problem, 
.. please invest some time in understanding the problem at leetcode.


.. If we go for a recursive approach, we need a base case .. what if we have 10 :math:`1^2+0^2=1`
.. so in this case, we will get 1 .. what if we have 13, well that means we need to sum the square of 1 and the square 
.. of 3 which will add up to 10 which can get us to the base case

.. .. math::

..     1^2 + 3^2 = 10

.. .. math::

..     1^2 + 0^2 = 1
    
.. xxxxxxxx

.. Python
.. """"""
.. .. -------------------------------------
.. .. code-block:: python

..    Z = np.zeros(9)
   
.. .. code::
..    :class: output
  
..    ┌───┬───┬───┬───┬───┬───┬───┬───┬───┐
..    │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │ 0 │
..    └───┴───┴───┴───┴───┴───┴───┴───┴───┘
.. .. -------------------------------------



