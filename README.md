# Soluções do Beecrowd para a Disciplina de Desafios de Programação

Este repositório contém a documentação de algumas soluções para os problemas de programação do Beecrowd, os quais foram aplicados na disciplina de **Desafios de Programação**. O objetivo deste projeto é resolver desafios propostos pela plataforma Beecrowd.

## Índice

- [Sobre](#sobre)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Estrutura do Repositório](#estrutura-do-repositório)
- [Contribuições](#contribuições)
- [Como Rodar as Soluções](#Como-Rodar-as-Soluções)

## Sobre

O Beecrowd é uma plataforma online que oferece uma vasta gama de problemas de programação, desafiando programadores a resolverem problemas utilizando diversas abordagens de algoritmos e estruturas de dados. Neste repositório, estão armazenadas as soluções que desenvolvi para os desafios dessa plataforma, com foco no aprendizado de conceitos de programação, como:

- Algoritmos de ordenação
- Estruturas de dados (listas, pilhas, filas, árvores)
- Algoritmos de busca
- Programação dinâmica
- Grafos e teorias relacionadas

O objetivo é documentar e compartilhar o processo de resolução desses problemas para ajudar outros alunos a melhorar suas habilidades.

## Tecnologias Utilizadas

As soluções estão sendo desenvolvidas em várias linguagens de programação, a depender da complexidade do desafio. Algumas delas incluem:

- **Python**
- **C**
- **Java**

## Como Rodar as Soluções

Para rodar as soluções deste repositório, siga as instruções abaixo, dependendo da linguagem em que o problema foi resolvido. **Todos os arquivos de código precisam ser renomeados** para o nome do problema ou da função para facilitar o acesso e organização, principalmente para os códigos em **Java** e **C**.

### Renomeando os Arquivos

- **Java**: O nome da classe **deve ser o nome do arquivo** para que o código compile corretamente. Se o nome da classe for `Main`, o arquivo **deve ser renomeado para `Main.java`**.
- **C**: O nome do arquivo de código **deve ser renomeado para `main.c`**, a menos que o problema tenha um nome específico que ajude a identificar a solução.
- **Python**: O arquivo pode manter qualquer nome, no entanto, é uma boa prática renomear os arquivos para que evite espaços entre as palavras.

### Exemplos na Renomeação

1. **C**:

   Suponha que o nome do problema seja **"1021 - Notas e Moedas"**. O código em **C** seria renomeado para:

   - **Arquivo**: `1021 - Notas e Moedas.c`
   - **Renomeado para**: `main.c`

   Exemplo de código em C (`main.c`):

   ```c
   #include <stdio.h>

   int main() {
       double dinheiros;
       int n, i;
       
       int notas[] = {10000, 5000, 2000, 1000, 500, 200};  
       double v[] = {100.00, 50.00, 20.00, 10.00, 5.00, 2.00, 1.00, 0.50, 0.25, 0.10, 0.05, 0.01}; 
       int result[12] = {0}; 

       scanf("%lf", &dinheiros);
       
       n = (int)(dinheiros * 100 + 0.5);  

       printf("NOTAS:\n");
       for(i = 0; i < 6; i++) { 
           result[i] = n / notas[i];
           n = n % notas[i];
           printf("%d nota(s) de R$ %.2f\n", result[i], v[i]);
       }
       
       printf("MOEDAS:\n");
       for(i = 6; i < 12; i++) { 
           result[i] = n / (int)(v[i] * 100);
           n = n % (int)(v[i] * 100);
           printf("%d moeda(s) de R$ %.2f\n", result[i], v[i]);
       }

       return 0;
   }

-----------------

## Estrutura do Repositório

A estrutura deste repositório é organizada de acordo com as linguagens usadas, cada uma em sua respectiva pasta:

beecrowd-solutions/
│
├── c/
│   ├── 1001_Soma_Simples/
│   ├── etc
│   └── etc
│
├── java/
│
├── python/
|
└── README.md
