# LAED_Lista1
Códigos da lista 1 da cadeira de LAED com o professor Thiago Bessa

/*1) Bubble Sort (básico) (0.5 valor)
Implemente void bubbleSort(int v[], int n) para ordenar em ordem crescente. Use troca com variável
temporária (swap). (Dica: cuidado com os limites do laço interno para não acessar v[j+1]fora do vetor.)*/

#include <stdio.h>
#include <stdlib.h>

void bubbleSort(int v[], int n) {
    int i, j;

    for(i= 0; i<n-1; i++){
        for(j=0; j<n-i-1; j++){
            if(v[j] > v[j+1]){
                int aux = v[j];
                v[j] = v[j+1];
                v[j+1] = aux;
            }
        }
    }
}
void imprimirVetor(int v[], int n) {
    for(int i = 0; i < n; i++){
        printf("%d ", v[i]);
    printf("\n");
 }
}
int main()
{
    int dados[] = {64, 34, 25, 12, 22, 11, 90};
    int n = 7;

    printf("Vetor original: ");
    imprimirVetor(dados, n);

    bubbleSort(dados, n);

    printf("Vetor ordenado: ");
    imprimirVetor(dados, n);

    return 0;
}

