Selection Sort em Java

Este projeto apresenta uma implementação do algoritmo de ordenação Selection Sort utilizando a linguagem Java.

O objetivo do programa é demonstrar como funciona o algoritmo de forma simples e didática, ordenando um array de números inteiros em ordem crescente.

📌 Sobre o Algoritmo Selection Sort

O Selection Sort é um algoritmo de ordenação simples que funciona selecionando repetidamente o menor elemento da parte não ordenada do array e colocando-o na posição correta.

O processo ocorre da seguinte forma:

Percorre o array procurando o menor elemento.

Troca o menor elemento encontrado com a posição atual.

Repete o processo para a próxima posição.

Continua até que todo o array esteja ordenado.

Embora seja fácil de entender e implementar, o Selection Sort não é eficiente para grandes volumes de dados.

⚙️ Complexidade do Algoritmo
Caso	Complexidade
Melhor caso	O(n²)
Caso médio	O(n²)
Pior caso	O(n²)

Isso ocorre porque o algoritmo sempre percorre o restante do array para encontrar o menor elemento.

🧠 Lógica do Algoritmo

O algoritmo utiliza dois laços de repetição:

Primeiro laço (for)
Percorre cada posição do array.

Segundo laço (for)
Procura o menor elemento na parte ainda não ordenada.

Quando o menor elemento é encontrado, ele é trocado com o elemento da posição atual.

💻 Código
package atividade.selectionsort;

public class SelectionSort {

    public static void main(String[] args) {

        int[] array = {5, 3, 8, 1, 4};
        
        System.out.print("Array Original:" );
        for(int num : array)
        {
            System.out.print(num + " ");
        }
        System.out.println("");
        
        
        selectionSort(array);
        System.out.print("Array Ordenado: ");
        for (int num : array) {
            System.out.print(num + " ");
        }
    }

    public static void selectionSort(int[] array) {

        for (int i = 0; i < array.length - 1; i++) {

            int smallestIndex = i;

            for (int j = i + 1; j < array.length; j++) {

                if (array[j] < array[smallestIndex]) {
                    smallestIndex = j;
                }
            }

            if (smallestIndex != i) {
                int temp = array[i];
                array[i] = array[smallestIndex];
                array[smallestIndex] = temp;
            }
        }
    }
}
▶️ Exemplo de Execução
Entrada
Array Original: 5 3 8 1 4
Saída
Array Ordenado: 1 3 4 5 8
📚 Objetivo do Projeto

Este projeto tem como objetivo:

Demonstrar o funcionamento do algoritmo Selection Sort

Praticar lógica de programação

Trabalhar com arrays e estruturas de repetição em Java

Entender conceitos básicos de algoritmos de ordenação
