### Exercício

Suponha um índice baseado em Árvore B:<br>
&#x26BE; O campo de indexação é um campo-chave.<br>
&#x26BE; O campo de indexação não é o campo de ordenação (caso exista).<br>
&#x26BE; O campo de indexação ocupa 10 bytes.<br>
&#x26BE; O tamanho de bloco é B = 512 bytes.<br>
&#x26BE; A dimensão do nó é a mesma dimensão do bloco.<br>
&#x26BE; Um ponteiro de dados (ponteiro de registro) ocupa 7 (sete) bytes.<br>
&#x26BE; Um ponteiro de árvore (ponteiro de bloco) ocupa 6 (seis) bytes.<br>
&#x26BE; Cada nó da árvore está 69% cheio (suposição).<br>
Determine:

(a) A </ins>ordem **p**</ins> da árvore.<br>
(b) O <ins>número de entradas</ins> e <ins>número de ponteiros de árvore</ins> em cada nó, em média, segundo a suposição **69% cheio** para os nós da árvore.<br>
(c) O número total de entradas na árvore até o nível 3.

A) (p * tam_ptr_de_bloco)+((p-1)*tam_valor_de_busca)+((p-1)*tam_pont_reg)<=512

6p+10p-10+7p-7<=512

23p<=512+10+7

p<=529/23

p<=23

p=23

----------------------------------------------------------------------------------------------
B) 0,69*p=15,87==>os nos em media tem 15 descendentes
----------------------------------------------------------------------------------------------
C)
| Nível | Nós  | Número Descendentes | N Entradas | Número Entradas Acumuladas |
|-------|------|---------------------|------------|---------------------------|
| 0     | 1    | 15                  | 14         | 14                        |
| 1     | 15   | 15 * 15 = 225       | 14 * 15 = 210 | 224                     |
| 2     | 225  | 225 * 15 = 3375     | 225 * 14 = 3150 | 3374                   |
| 3     | 3375 | 3375 * 15 = 50625   | 3375 * 14 = 47250 | 50624               |
