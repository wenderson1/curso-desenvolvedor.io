# Anotações de Fundamentos C#

## Lógica de Programação

Lógica de programação é uma sequência de passos para executar algo em um programa.

## O que é uma linguagem de programação?

É uma forma de escrever instruções para que o computador possa interpretar e executar. Todo conjunto de instruções que escrevemos é chamado de código fonte e esse código pode ser interpretado ou compilado.

## O que é o .NET?

O .NET é uma plataforma de código aberto, ou seja, roda no Windows, Linux e macOS, criada pela Microsoft para construção de diferentes tipos de aplicação.

A plataforma do .NET fornece para gente um conjunto de bibliotecas otimizadas para acelerar o desenvolvimento, além da possibilidade de desenvolver nossas aplicações em várias linguagens: C#, F#, C++, VB.NET.

## O que é CLR?

CLR ou Common Language Runtime é a base principal do .NET, sendo o responsável por executar sua aplicação e conversar com o hardware. Aqui é onde fica o Garbage Collector.

## O que é um projeto?

Um projeto é uma forma de você organizar todo o código fonte de sua aplicação, seja por arquivos ou até mesmo pastas. No projeto é onde ficam todos os arquivos que serão compilados. Além disso, você pode adicionar informações sobre sua aplicação, como por exemplo o nome da sua aplicação, versão, versão do .NET e o tipo do binário que será gerado, se é um exe ou dll.

## O que é uma solução?

Uma solução, de maneira resumida, é uma forma de você agrupar vários projetos. No momento de compilar sua aplicação, em vez de compilar projeto por projeto, você compila a solução e os binários de cada projeto serão gerados individualmente de uma única vez.

## Comando em .NET

```
dotnet new --list => para listar todos os templates de projeto
dotnet new sln -n NomeDaSolution -> para criar a solução, -n serve para colocar o bone
dotnet new console -n NomeDoProjeto -f VersaoFramework -o ./Diretorio -> para criar o projeto do tipo console, o -n serve para colocar o nome, o -f para indicar a versão do framework, e -o para colocar onde vai ficar disponível a pasta do projeto.
```

## Tipos de dados do C#

```
Inteiros:
byte,
short,
int,
long

Pontos Flutuantes:
float,
double,
decimal

Booleano:
bool

Caracteres:
char,
string

Outros tipos:
Classes,
Interfaces,
struct,
object,
dynamic
```

# O que é uma váriavel?

Sua principal função é armazenar dados na memória para serem usados posteriormente.

# Oque é uma constante?

Constante é uma váriavel que não pode ser alterada o seu valor ao longo do algoritmo

#Operadores Aritméticos
Os operadores aritméticos em C# são usados para realizar operações matemáticas básicas. Aqui estão alguns dos operadores aritméticos mais comuns:

## Operadores Relacionais

Os operadores relacionais em C# são usados para comparar valores e retornam um valor booleano (true ou false) com base na comparação. Aqui estão alguns dos operadores relacionais mais comuns:

```
== : Igual a
!= : Diferente de
> : Maior que
> : Menor que
>=:  Maior ou igual a
<= : Menor ou igual a
```

## Operadores lógicos

Operadores lógicos
Os operadores lógicos em C# são usados para combinar expressões booleanas e retornam um valor booleano (true ou false). Aqui estão alguns dos operadores lógicos mais comuns:

```
&& : E lógico (AND)
|| : OU lógico (OR)
! : NÃO lógico (NOT)
```

## Operador ternário em C#

O operador ternário em C# é uma maneira concisa de escrever uma expressão condicional. Ele é composto por três partes: uma condição, uma expressão a ser avaliada se a condição for verdadeira e uma expressão a ser avaliada se a condição for falsa. A sintaxe é a seguinte:

```

condição ? expressão_se_verdadeira : expressão_se_falsa;

```

Por exemplo, se você quiser atribuir um valor a uma variável com base em uma condição, você pode usar o operador ternário:

```csharp
int a = 10;
int b = 20;
int maior = (a > b) ? a : b; // maior será 20

```

## O que são função em C#

Em C#, uma função é um bloco de código que realiza uma tarefa específica e pode ser chamada de qualquer lugar do programa. As funções ajudam a organizar e reutilizar o código, tornando-o mais modular e fácil de manter. Aqui está um exemplo básico de uma função em C#:

```csharp
using System;
class Program
{
    static void Main()
    { // Chama a função
        Saudacao();
    }
    // Define a função
    static void Saudacao()
    {
         Console.WriteLine("Olá, mundo!");
    }
}
```
