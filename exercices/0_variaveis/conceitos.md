## Variáveis e Estruturas de dados

---

### Tipo de dados
Os dados ou informações, são classificados pelo computador de acordo com
seus tipos.
E esta classificação segue a tabela abaixo:

dado|tipo|exemplo
---|---|---
palavras (string)|str|"Jesus" ou 'Jesus'
qualquer texto|str|"Tudo é difícil até fácil se tornar."
números naturais| int|0, 1, 2, 3, 4, 5, 6, 7, 8
números inteiros| int| -99, -5, -3, -1, 0, 1, 3, 5, 99
números reais| float| 1.5, 3.1415, 2.67
valores lógicos| bool| True, False

### Variáveis

Uma variável é uma estrutura simples de valor único, em que podemos guardar
informações durante a execução do programa.

Exemplos:
```python
pais = "Brasil"   # variável do tipo texto
pi = 3.1415    # variável do tipo float
ano = 2022    # variável do tipo int
continuar = False    # variável do tipo bool
```

**Como descobrir o tipo de uma variável?**

No Python há o comando `type`, que exibe o tipo da variável.
```python
pais = "Brasil"   # variável do tipo texto
type(pais)
# <class 'str'>
```

### Estrutura de dados
A estrutura de dados é multivalorada e pode conter varios valores distintos,
em que podemos guardar informações durante a execução do programa. No Python
temos:
- [list](#list),
- [dict](#dict),
- [tuple](#tuple) e
- [set](#set).


## list
Permitem armazenar várias informações em uma mesma variável. É uma
estrutura de dados que pode conter itens. No Python nos é fornecido um
objeto do tipo list e todos elementos que estiverem delimitados por
colchetes, será interpretado pela linguagem, como um conjunto de itens
pertencentes a uma lista. Sintaxe:

```
<variável> = [info1, info2, info3]
```

Exemplos:
```python
a = ['String', 9, True]
a

b = [['Nome', 99999], True]
b

type(b)
```

### Acessando itens da lista
Índice em uma lista: número que indica a posição de cada caractere na string. O número será 0 (zero) para o primeiro caractere na string, 1 para o segundo, 2 para o terceiro, etc. Sintaxe:

```
<lista>[número]
```

Exemplos:
```python
['a', 2, True, [1], 'GruPy Blumenau']
```

'a' | 2 | True | [1] | 'GruPy Blumenau'
----|---|------|-----|-----------------
  0 | 1 |  2   |  3  |       4

```python
a = ['a', 2, True, [1], 'GruPy Blumenau']

a[0]

a[3]

a[2]
```

### Partes de uma lista (slicing)
Retorna parte da lista, começando pelo primeiro índice e terminando no anterior ao segundo. Sintaxe:

```
<lista>[índice1:índice2]
```

**OBS: Quando omitimos um índice, é mostrado o caractere do extremo correspondente**

Exemplos:
```python
['a', 2, True, [1], 'GruPy Blumenau']
```

'a' | 2 | True | [1] | 'GruPy Blumenau'
----|---|------|-----|-----------------
  0 | 1 |  2   |  3  |       4

```python
a = ['a', 2, True, [1], 'GruPy Blumenau']

a[0:2]

a[2:]

a[:3]
```

### Incremento de fatia (slicing)
Permite resgatar índices alternados, e até mesmo inverter uma lista. Sintaxe:

```
<lista>[índice1:índice2:<incremento>]
```
Exemplos:
```python
['a', 2, True, [1], 'GruPy', 1, 2]
```

'a' | 2 | True | [1] | 'GruPy' | 1 | 2
----|---|------|-----|---------|---|---
  0 | 1 |  2   |  3  |   4     | 5 | 6

```python
a = ['a', 2, True, [1], 'GruPy', 1, 2]

a[::2]

a[::-1]

a[5:0:-2]
```

### Tamanho da sua Lista
Para saber o tamanho da sua lista, basta pedir para o Python a partir da comando "len". Sintaxe:

```
len(<lista>)
```

Exemplos:
```python
a = [1, 2, 3]
len(a)
```

### Adicionando itens a minha lista (<list>.append(VALOR))
Existem duas formas de fazer isso:
- "concatenando" listas
- adicionado o item com a comando append.

Sintaxe:

```
<lista>.append(<item para adicionar>)

ou

<lista1> + <lista2>
```

Exemplos:
```python
a = [1, 2]

a.append(3)

a

b = [4, 5]

a + b
```

### Listas de Letras (vulgo strings)
O Python, como a maioria das linguagem, entende que a string é uma lista de letras, logo, você pode aplicar alguns comandos das listas em strings \o/

Exemplos:
```python
a = 'Pyladies'

a[:2]

a[0:5:2]

a[::-1]

a[5:0:-2]

len(a)
```

### Transformando uma lista em uma string
Join: gruda os elementos de uma sequência de strings, usando uma string fornecida, que será usada para "dividir os itens da lista". Sintaxe:

```
'string'.join(<lista>)
```

Exemplos:
```python
a = ['banana', 'limão', 'maçã']

','.join(a)
```

[:arrow_up: Voltar para submenu](#estrutura-de-dados)

## tuple
Tupla é uma Lista imutável. Ou seja tuplas se comportam como listas estáticas e ocupam menos espaço na memória comparadas a listas. No Python nos é fornecido um objeto do tipo tuple e todos elementos que estiverem delimitados por parênteses, será interpretado pela linguagem, como um conjunto de itens pertencentes a uma tupla.

Exemplos:
```python
a = ('banana', 'limão', 'maçã')

type(a)

# tuples não tem o metodo .append justamente porque são imutáveis
a.append('melancia') # vai gerar uma exceção

```

**OBS: As tuplas podem conter itens mutáveis.**

Exemplos:
```python
a = ('banana', 'limão', 'maçã', ['melancia'])

type(a)

id(a) # retorna o identificador único desse objeto no python

a[3].append('uva') # estamos adicionando um novo valor na lista que existe no indice 3 dessa tupla

a

id(a)
```

### Acessando itens da tupla
Como nas listas, podemos acessar os valores acessando diretamente o indice da tupla. Sintaxe:

```
<tupla>[número]
```

Exemplos:
```python
a = ('banana', 'limão', 'maçã')

a[2]
```

[:arrow_up: Voltar para submenu](#estrutura-de-dados)

## dict
Dicionário é uma lista de chaves e valor.

Exemplos:
```python
a = {'chave_1': 'valor 1', 'chave_2': 2, 'chave_3': ['melancia'], 'chave_4': ('banana', 'limão', 'maçã')}

a

type(a)
```

### Acessando itens do dicionário
Para acessar os dados de um dicionário precisamos passar a chave ou utilizar o método <dict>.get. Sintaxe:

```
<dict>[chave_do_dicionário]

ou

<dict>.get(chave_do_dicionário)
```

Exemplos:
```python
a = {'chave_1': 'valor 1', 'chave_2': 2, 'chave_3': ['melancia'], 'chave_4': ('banana', 'limão', 'maçã')}

a['chave_1']

a.get('chave_1')
```

**OBS: Usando método <dict>.get não retornamos uma exceção caso a chave não exista.**

Exemplos:
```python
a = {'chave_1': 'valor 1', 'chave_2': 2, 'chave_3': ['melancia'], 'chave_4': ('banana', 'limão', 'maçã')}

a['chave_10'] # vai retornar uma exceção

a.get('chave_10') # vai retornar um valor None

a.get('chave_10', 10) # assim definimos um valor padrão caso a chave não exista
```

[:arrow_up: Voltar para submenu](#estrutura-de-dados)

## set
É um conjunto de dados sem valores repetidos. No Python nos é fornecido um objeto do tipo set e todos elementos que estiverem delimitados por chaves, será interpretado pela linguagem, como um conjunto de itens pertencentes a um conjunto. Sintaxe:

```
{valor_1, valor_2}
```

Exemplos:
```python
a = {1, 2, 3}

type(a)
```

[:arrow_up: Voltar para submenu](#estrutura-de-dados)

