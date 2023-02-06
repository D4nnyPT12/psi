# Introdução

O conceito de "string" é bastante simples. Uma string é uma sequência de carateres. 

Em Python as strings são imutáveis. 

Exercício: O que é um objeto imutável?


# Slice

Podemos cortar uma "fatia" de uma string utilizando a notação [a:b:c]. 

- a: posição de início da "fatia";
- b: posição final da "fatia";
- c: passo entre o início e o final.

O passo (stride) pode ser negativo, retornando os itens em "reverse".

```
>>> s = 'bicycle'
>>> s[::3]
'bye'
>>> s[::-1]
'elcycib'
>>> s[::-2]
'eccb'
```

## replace

O método ```replace()``` substitui uma frase por outra frase.

```
string.replace(valor_antigo, novo_valor, conta)
```

- valor_antigo - Obrigatório. A string a ser procurada.
- novo_valor - Obrigatório. A string que irá substituir
- count - O número de vezes a substituir a string. Se não for especificado, todas as ocorrências irão ser substituídas.

## Grupos

- Grupo 1
    - Bernardo
    - Veiga
- Grupo 2
    - Hugo
    - Alves
- Grupo 3
    - Sousa
    - Beatriz
- Grupo 4
    - Afonso
    - Júnior
- Grupo 5
    - Cristiano
    - Filipe
- Grupo 6
    - Davi
    - Daniel

## Trabalho

- capitalize()	Converts the first character to upper case
- casefold()	Converts string into lower case
- center()	Returns a centered string
- count()	Returns the number of times a specified value occurs in a string
- encode()	Returns an encoded version of the string
- endswith()	Returns true if the string ends with the specified value
- expandtabs()	Sets the tab size of the string
- find()	Searches the string for a specified value and returns the position of where it was found
- format()	Formats specified values in a string
- format_map()	Formats specified values in a string
- index()	Searches the string for a specified value and returns the position of where it was found
- isalnum()	Returns True if all characters in the string are alphanumeric
- isalpha()	Returns True if all characters in the string are in the alphabet
- isascii()	Returns True if all characters in the string are ascii characters
- isdecimal()	Returns True if all characters in the string are decimals
- isdigit()	Returns True if all characters in the string are digits
----isidentifier()----
a = "_Teste"
b = "teste2"
c = "Teste 2"
d = "2Teste"

print (a.isidentifier()) #True
print (b.isidentifier()) #True
print (c.isidentifier()) #False
print (d.isidentifier()) #False

#Uma string é considerada "True" se contiver apenas letras alfanuméricas (a-z) e (0-9) ou sublinhados (_).
#Para a string ser válido não pode começar com um número ou conter espaços.
#As variaveis "c" e "d" são falsas porque contem espaços e ou começam com um numero.

----islower()----
a = 'ola pedro tens 17 anos!'
b = 'ola joana!'
c = 'ola João tens 17 anos!'
d = 'Ola Joana!'
print(a.islower()) #True
print(b.islower()) #True
print(c.islower()) #False
print(d.islower()) #False
#A função islower() retorna "True" se todos os caracteres estiverem em minúsculas, caso contrário, retorna "False".

----isnumeric()----
a = '123'
b = 'abc'
c = 'o0a4'
d = '6iv7'

print(a.isnumeric()) #True
print(b.isnumeric()) #False
print(c.isnumeric()) #False
print(d.isnumeric()) #False

----isprintable()----
exemplo1 = 'O meu nome é Davi'
exemplo2 = 'Olá! \n O meu nome é Davi'
exemplo3 = ' '

print(exemplo1.isprintable()) #True
print(exemplo2.isprintable()) #False
print(exemplo3.isprintable()) #True

----isspace()----
texto1 = "    "
texto2 = " a  "

x1 = texto1.isspace()
x2 = texto2.isspace()

print(x1) #True
print(x2) #False

#retorna true se o texto da string tiver apenas "espaço"

----istitle()----
txt1 = "Olá, E Bem Vindos Ao Meu Mundo!"
txt2 = "Olá e bem vindos ao Meu Mundo!"

x = txt1.istitle()
x2 = txt2.istitle()
print(x) #True
print(x2) #False

#retorna True se todas as palavras da string começam com uma letra maiúscula e
#o resto da string são letras minúsculas, caso contrário, False.

----isupper()----
txt1 = "THIS IS NOW!"
txt2 = "Bora Lá"

x = txt1.isupper() #True

x2= txt2.isupper() #False

print(x)
print(x2)

#Se a string conter apenas letras maiusculas dá "True" caso contrário "False"

---- join()----
tuplo = ("John", "Wick", "3")

x = "-".join(tuplo)

print(x) #JOhn-Wick-3

#Esta função adiciona o texto inserido entre as strings

- ljust()	Returns a left justified version of the string
- lower()	Converts a string into lower case
- lstrip()	Returns a left trim version of the string
- maketrans()	Returns a translation table to be used in translations
- partition()	Returns a tuple where the string is parted into three parts
- replace()	Returns a string where a specified value is replaced with a specified value
- rfind()	Searches the string for a specified value and returns the last position of where it was found
- rindex()	Searches the string for a specified value and returns the last position of where it was found
- rjust()	Returns a right justified version of the string
- rpartition()	Returns a tuple where the string is parted into three parts
- rsplit()	Splits the string at the specified separator, and returns a list
- rstrip()	Returns a right trim version of the string
- split()	Splits the string at the specified separator, and returns a list
- splitlines()	Splits the string at line breaks and returns a list
- startswith()	Returns true if the string starts with the specified value
- strip()	Returns a trimmed version of the string
- swapcase()	Swaps cases, lower case becomes upper case and vice versa
- title()	Converts the first character of each word to upper case
- translate()	Returns a translated string
- upper()	Converts a string into upper case
- zfill()	Fills the string with a specified number of 0 values at the beginning


## Avançado 

### Carateres

In 2021, the best definition of “character” we have is a Unicode character. Accordingly, the items we get out of a Python 3 str are Unicode characters, just like the items of a unicode object in Python 2—and not the raw bytes we got from a Python 2 str.

