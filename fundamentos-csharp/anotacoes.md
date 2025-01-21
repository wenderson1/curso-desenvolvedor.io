# Anotações de Fundamentos C#

#### Lógica de Programação

Lógica de programação é uma sequência de passos para executar algo em um programa.

#### O que é uma linguagem de programação?

É uma forma de escrever instruções para que o computador possa interpretar e executar. Todo conjunto de instruções que escrevemos é chamado de código fonte e esse código pode ser interpretado ou compilado.

#### O que é o .NET?

O .NET é uma plataforma de código aberto, ou seja, roda no Windows, Linux e macOS, criada pela Microsoft para construção de diferentes tipos de aplicação.

A plataforma do .NET fornece para gente um conjunto de bibliotecas otimizadas para acelerar o desenvolvimento, além da possibilidade de desenvolver nossas aplicações em várias linguagens: C#, F#, C++, VB.NET.

#### O que é CLR?

CLR ou Common Language Runtime é a base principal do .NET, sendo o responsável por executar sua aplicação e conversar com o hardware. Aqui é onde fica o Garbage Collector.

#### O que é um projeto?

Um projeto é uma forma de você organizar todo o código fonte de sua aplicação, seja por arquivos ou até mesmo pastas. No projeto é onde ficam todos os arquivos que serão compilados. Além disso, você pode adicionar informações sobre sua aplicação, como por exemplo o nome da sua aplicação, versão, versão do .NET e o tipo do binário que será gerado, se é um exe ou dll.

#### O que é uma solução?

Uma solução, de maneira resumida, é uma forma de você agrupar vários projetos. No momento de compilar sua aplicação, em vez de compilar projeto por projeto, você compila a solução e os binários de cada projeto serão gerados individualmente de uma única vez.

#### Comando em .NET

```
dotnet new --list => para listar todos os templates de projeto
dotnet new sln -n NomeDaSolution -> para criar a solução, -n serve para colocar o bone
dotnet new console -n NomeDoProjeto -f VersaoFramework -o ./Diretorio -> para criar o projeto do tipo console, o -n serve para colocar o nome, o -f para indicar a versão do framework, e -o para colocar onde vai ficar disponível a pasta do projeto.
```

#### Tipos de dados do C#

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

#### O que é uma váriavel?

Sua principal função é armazenar dados na memória para serem usados posteriormente.

#### Oque é uma constante?

Constante é uma váriavel que não pode ser alterada o seu valor ao longo do algoritmo

#Operadores Aritméticos
Os operadores aritméticos em C# são usados para realizar operações matemáticas básicas. Aqui estão alguns dos operadores aritméticos mais comuns:

#### Operadores Relacionais

Os operadores relacionais em C# são usados para comparar valores e retornam um valor booleano (true ou false) com base na comparação. Aqui estão alguns dos operadores relacionais mais comuns:

```
== : Igual a
!= : Diferente de
> : Maior que
> : Menor que
>=:  Maior ou igual a
<= : Menor ou igual a
```

#### Operadores lógicos

Operadores lógicos
Os operadores lógicos em C# são usados para combinar expressões booleanas e retornam um valor booleano (true ou false). Aqui estão alguns dos operadores lógicos mais comuns:

```
&& : E lógico (AND)
|| : OU lógico (OR)
! : NÃO lógico (NOT)
```

#### Operador ternário em C#

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

#### O que são função em C#

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

# Estrutura de dados

#### ArrayList

ArrayList é uma estrutura de dados em C# que permite armazenar uma coleção de objetos de qualquer tipo. Diferente dos arrays tradicionais, que têm tamanho fixo, o ArrayList pode crescer e diminuir dinamicamente conforme necessário. Ele é parte do namespace System.Collections e oferece métodos para adicionar, remover e acessar elementos de forma eficiente.

```csharp
using System;
using System.Collections;

class Program
{
static void Main()
{
// Cria um novo ArrayList
ArrayList lista = new ArrayList();

        // Adiciona elementos ao ArrayList
        lista.Add(1);
        lista.Add("dois");
        lista.Add(3.0);

        // Acessa elementos pelo índice
        Console.WriteLine(lista[0]); // Saída: 1
        Console.WriteLine(lista[1]); // Saída: dois
        Console.WriteLine(lista[2]); // Saída: 3.0

        // Remove um elemento
        lista.Remove("dois");

        // Itera sobre os elementos
        foreach (var item in lista)
        {
            Console.WriteLine(item);
        }
    }
}
```

#### Arrays tipados

Arrays tipados em C# são coleções de elementos do mesmo tipo, armazenados em posições contíguas na memória. Eles são definidos com um tipo específico, o que significa que todos os elementos do array devem ser do mesmo tipo. Isso permite que o compilador verifique a segurança de tipos em tempo de compilação, evitando erros de tipo em tempo de execução.

```csharp
using System;

class Program
{
    static void Main()
    {
        // Declaração de um array de inteiros
        int[] numeros = new int[5];

        // Inicialização do array
        numeros[0] = 1;
        numeros[1] = 2;
        numeros[2] = 3;
        numeros[3] = 4;
        numeros[4] = 5;

        // Acessando elementos do array
        for (int i = 0; i < numeros.Length; i++)
        {
            Console.WriteLine(numeros[i]);
        }
        Array.Resize( ref numeros, 100) // para alterar o tamanho do array
    }
}
```

#### Lista Genérica

Uma lista genérica em C# é uma coleção fortemente tipada que permite armazenar e manipular elementos de um tipo específico. Elas são parte do namespace System.Collections.Generic e oferecem várias vantagens sobre as coleções não genéricas, como ArrayList, incluindo segurança de tipos em tempo de compilação e melhor desempenho.

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Cria uma nova lista genérica de inteiros
        List<int> numeros = new List<int>();

        // Adiciona elementos à lista
        numeros.Add(1);
        numeros.Add(2);
        numeros.Add(3);

        // Acessa elementos pelo índice
        Console.WriteLine(numeros[0]); // Saída: 1
        Console.WriteLine(numeros[1]); // Saída: 2
        Console.WriteLine(numeros[2]); // Saída: 3

        // Remove um elemento
        numeros.Remove(2);

        // Itera sobre os elementos
        foreach (int numero in numeros)
        {
            Console.WriteLine(numero);
        }
    }
}
```

#### Dicionários

Um dicionário em C# é uma coleção de pares chave-valor, onde cada chave é única e está associada a um valor. Eles são parte do namespace System.Collections.Generic e são extremamente úteis para armazenar e acessar dados de forma eficiente, especialmente quando você precisa fazer buscas rápidas por chave.

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Cria um novo dicionário com chaves do tipo string e valores do tipo int
        Dictionary<string, int> idadePessoas = new Dictionary<string, int>();

        // Adiciona elementos ao dicionário
        idadePessoas.Add("Alice", 30);
        idadePessoas.Add("Bob", 25);
        idadePessoas.Add("Charlie", 35);

        // Acessa elementos pelo chave
        Console.WriteLine("Idade de Alice: " + idadePessoas["Alice"]); // Saída: Idade de Alice: 30

        // Verifica se uma chave existe
        if (idadePessoas.ContainsKey("Bob"))
        {
            Console.WriteLine("Idade de Bob: " + idadePessoas["Bob"]); // Saída: Idade de Bob: 25
        }

        // Itera sobre os elementos do dicionário
        foreach (var pessoa in idadePessoas)
        {
            Console.WriteLine(pessoa.Key + " tem " + pessoa.Value + " anos.");
        }
    }
}
```

#### Queue

Uma Queue (fila) em C# é uma coleção que segue o princípio FIFO (First In, First Out), ou seja, o primeiro elemento a ser adicionado é o primeiro a ser removido. Isso é útil para cenários onde a ordem de processamento é importante, como em filas de tarefas ou mensagens.

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Cria uma nova fila de inteiros
        Queue<int> fila = new Queue<int>();

        // Adiciona elementos à fila
        fila.Enqueue(1);
        fila.Enqueue(2);
        fila.Enqueue(3);

        // Remove e retorna o elemento na frente da fila
        Console.WriteLine(fila.Dequeue()); // Saída: 1

        // Retorna o elemento na frente da fila sem removê-lo
        Console.WriteLine(fila.Peek()); // Saída: 2

        // Itera sobre os elementos da fila
        foreach (int numero in fila)
        {
            Console.WriteLine(numero);
        }
    }
}
```

#### Stacks

Uma Stack (pilha) em C# é uma coleção que segue o princípio LIFO (Last In, First Out), ou seja, o último elemento a ser adicionado é o primeiro a ser removido. Isso é útil para cenários onde você precisa acessar os elementos na ordem inversa à que foram adicionados, como em algoritmos de recursão ou na navegação de páginas da web (voltar e avançar).

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Cria uma nova pilha de inteiros
        Stack<int> pilha = new Stack<int>();

        // Adiciona elementos à pilha
        pilha.Push(1);
        pilha.Push(2);
        pilha.Push(3);

        // Remove e retorna o elemento no topo da pilha
        Console.WriteLine(pilha.Pop()); // Saída: 3

        // Retorna o elemento no topo da pilha sem removê-lo
        Console.WriteLine(pilha.Peek()); // Saída: 2

        // Itera sobre os elementos da pilha
        foreach (int numero in pilha)
        {
            Console.WriteLine(numero);
        }
    }
}
```

## Estrutura de Controle

#### IF/Else

A estrutura if/else permite que você execute diferentes blocos de código com base em condições específicas.

```csharp
int numero = 10;

if (numero > 0)
{
    Console.WriteLine("O número é positivo.");
}
else if (numero < 0)
{
    Console.WriteLine("O número é negativo.");
}
else
{
    Console.WriteLine("O número é zero.");
}
```

#### Switch

Claro! A estrutura switch em C# é usada para simplificar a tomada de decisões com base no valor de uma variável.

```csharp
int diaDaSemana = 3;

switch (diaDaSemana)
{
    case 1:
        Console.WriteLine("Segunda-feira");
        break;
    case 2:
        Console.WriteLine("Terça-feira");
        break;
    case 3:
        Console.WriteLine("Quarta-feira");
        break;
    case 4:
        Console.WriteLine("Quinta-feira");
        break;
    case 5:
        Console.WriteLine("Sexta-feira");
        break;
    case 6:
        Console.WriteLine("Sábado");
        break;
    case 7:
        Console.WriteLine("Domingo");
        break;
    default:
        Console.WriteLine("Dia inválido");
        break;
}
```

Neste exemplo:

- A variável diaDaSemana é comparada com cada case.
- Se diaDaSemana for igual a 3, a mensagem "Quarta-feira" será exibida.
- O break é usado para sair do switch após a execução de um case.
- O default é executado se nenhum dos cases corresponder ao valor da variável.
  A estrutura switch é útil quando você tem muitas condições para verificar e quer evitar múltiplos if/else

#### For

A estrutura for em C# é usada para executar um bloco de código repetidamente com base em uma condição. Aqui está um exemplo básico:

```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine("O valor de i é: " + i);
}
```

Neste exemplo:

- A inicialização int i = 0 define a variável de controle i com o valor inicial de 0.
- A condição i < 5 é verificada antes de cada iteração do loop. Se for verdadeira, o bloco de código dentro do for é executado.
- A expressão de incremento i++ é executada após cada iteração, incrementando o valor de i em 1.

O loop for é útil quando você sabe quantas vezes deseja repetir um bloco de código.

#### Foreach

A estrutura foreach em C# é usada para iterar sobre uma coleção de elementos, como arrays ou listas, de forma simples e direta. Aqui está um exemplo básico:

```csharp
int[] numeros = { 1, 2, 3, 4, 5 };

foreach (int numero in numeros)
{
    Console.WriteLine("O número é: " + numero);
}

foreach (var letra in "Wenderson Farias")
{
    Console.WriteLine(letra);
}
```

Neste exemplo:

- A variável numeros é um array de inteiros.
- O loop foreach itera sobre cada elemento do array numeros.
- Para cada iteração, a variável numero assume o valor do elemento atual do array.
- O bloco de código dentro do foreach é executado para cada elemento, exibindo o valor de numero.

A estrutura foreach é especialmente útil quando você precisa percorrer todos os elementos de uma coleção sem se preocupar com índices.

#### While/Do While

As estruturas while e do while em C# são usadas para executar um bloco de código repetidamente com base em uma condição. Aqui está um exemplo básico para cada uma:

###### while

A estrutura while executa o bloco de código enquanto a condição for verdadeira:

```csharp
int i = 0;

while (i < 5)
{
    Console.WriteLine("O valor de i é: " + i);
    i++;
}
```

Neste exemplo:

- A variável i é inicializada com 0.
- O bloco de código dentro do while é executado enquanto i for menor que 5.
- A cada iteração, i é incrementado em 1.

###### do while

A estrutura do while é semelhante ao while, mas garante que o bloco de código seja executado pelo menos uma vez, mesmo que a condição seja falsa:

```csharp
int i = 0;

do
{
    Console.WriteLine("O valor de i é: " + i);
    i++;
} while (i < 5);
```

Neste exemplo:

- A variável i é inicializada com 0.
- O bloco de código dentro do do é executado uma vez antes da condição ser verificada.
- Após a execução do bloco, a condição i < 5 é verificada. Se for verdadeira, o bloco é executado novamente.

A principal diferença entre while e do while é que do while garante que o bloco de código seja executado pelo menos uma vez, enquanto while pode não executar o bloco de código se a condição inicial for falsa.
