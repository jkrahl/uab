---
title: Medida de la información
---
# Función de incerteza
Supongamos un experimento o situación que, primero, no se ha realizado antes, o segundo, sus resultados tienen un carácter aleatorio. Al realizar el experimento, se obtiene un resultado, proporcionando una cantidad de información.

Esta cantidad de información depende de:
1. El número de posibles resultados. Más posibles resultados → Más información.
2. La probabilidad de obtener ese resultado. Más improbable → Más información.

Considerando la incerteza como la falta de certeza ante un experimento así, la cantidad de información que se obtiene tras realizar el experimento es igual a la cantidad de incerteza antes de hacerlo. ^579020

Denominamos $I(n)$ a la incerteza sobre $n$ resultados posibles i **equiprobables**.

Los requisitos para la función de incerteza son:
1. $I(1)=0,\; \text{i } I(n)<I(n+1),\; \forall n \in \mathbb{N},$
2. $I(nm)=I(n)+I(m),\; \forall {n,m} \in \mathbb{N},$
3. $I(n^k)=k\cdot I(n),\; \forall{n,k} \in \mathbb{N}.$

### Medida de Hartley
En 1928, Hartley propuso $I(n)=\log n$ cumpliendo con los anteriores requisitos, pero no se tienen en cuenta las probabilidades de cada resultado si son distintas.
### Medida de Shannon
Si los eventos menos probables dan más información, entonces la información debe crecer respecto a la inversa de las probabilidades, que se traduce como $I(A) = f\left( \frac{1}{p(A)}\right)$ donde $f$ es una función creciente, y $A$ es un [[Conceptos previos EST#Evento|evento]] con una probabilidad $p(A)$.

En 1948, Shannon propuso la siguiente expresión como medida de la incerteza de un evento $A$ con una probabilidad $p(A)$:
$$
I(A)=\log {\frac{1}{p(A)}}=-\log {p(A)}
$$

Esta formula coincide con la medida de Hartley cuando los eventos son equiprobables.

# Información de una fuente

Una fuente es todo aquello que emite [[T1S3 Privacidad Autenticidad|mensajes]], por ejemplo, una fuente podría ser un ordenador y los archivos son los mensajes. La fuente es en sí un conjunto finito de mensajes, con todos los posibles mensajes que puede emitir.

Si una fuente de información produce unos símbolos $a_1,a_2,\dots ,a_n$ con las respectivas probabilidades $p(a_1),p(a_2),\dots ,p(a_n)$, la información asociada a cada uno de los símbolos dependerá de su probabilidad.

Teniendo en cuenta que [[T2S1 Medida Info#^579020|la cantidad de información (posterior) es igual a la cantidad de incerteza (anterior)]], definimos la información de la fuente como la media ponderada de la información de todos los símbolos:
$$
\sum_{i=1}^n{p(a_i)I(a_i)} = \sum_{i=1}^n{p(a_i)\log {\frac{1}{p(a_i)}}}
$$
Además coincide con la incerteza media que se tiene del resultado.

### Unidades de medida de la información
Se denomina **bit** a la unidad de información más pequeña, asociada a dos eventos equiprobables $a_1\text{ i } a_2 \left( p(a_1) = p(a_2) = \frac{1}{2} \right)$. 