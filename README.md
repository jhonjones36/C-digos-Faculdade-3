#include <stdio.h>

// Função para encontrar o maior e o menor valor
void encontrarMaiorMenor(int valores[], int *maior, int *menor) {
    *maior = valores[0];
    *menor = valores[0];

    for (int i = 1; i < 5; i++) {
        if (valores[i] > *maior) {
            *maior = valores[i];
        }
        if (valores[i] < *menor) {
            *menor = valores[i];
        }
    }
}

int main() {
    int valores[5];
    int maior, menor;

    printf("Digite cinco valores inteiros:\n");

    // Lê os cinco valores
    for (int i = 0; i < 5; i++) {
        printf("Valor %d: ", i + 1);
        scanf("%d", &valores[i]);
    }

    // Chama a função para encontrar o maior e o menor
    encontrarMaiorMenor(valores, &maior, &menor);

    // Imprime os resultados
    printf("\nO maior valor é: %d\n", maior);
    printf("O menor valor é: %d\n", menor);

    return 0;
}
