#include <stdio.h>

#define TAM_TABULEIRO 10
#define TAM_NAVIO 3

int main() {

    // Declaração do tabuleiro 10x10, inicializado com 0 (representa água)
    int tabuleiro[TAM_TABULEIRO][TAM_TABULEIRO] = {0};

    // Declaração dos navios como vetores unidimensionais com tamanho fixo 3
    int navio_horizontal[TAM_NAVIO] = {3, 3, 3}; // valor 3 representa parte do navio
    int navio_vertical[TAM_NAVIO] = {3, 3, 3};

    // Coordenadas iniciais dos navios
    int linha_horizontal = 2;
    int coluna_horizontal = 4;

    int linha_vertical = 5;
    int coluna_vertical = 7;

    // Validação: garantir que os navios cabem no tabuleiro
    if (coluna_horizontal + TAM_NAVIO <= TAM_TABULEIRO &&
        linha_horizontal < TAM_TABULEIRO) {
        // Posiciona o navio horizontal
        for (int i = 0; i < TAM_NAVIO; i++) {
            // Verifica se há sobreposição com outro navio
            if (tabuleiro[linha_horizontal][coluna_horizontal + i] != 0) {
                printf("Erro: sobreposição de navios na posição (%d, %d).\n", linha_horizontal, coluna_horizontal + i);
                return 1; // encerra o programa
            }
            tabuleiro[linha_horizontal][coluna_horizontal + i] = navio_horizontal[i];
        }
    } else {
        printf("Erro: navio horizontal não cabe no tabuleiro.\n");
        return 1;
    }

    if (linha_vertical + TAM_NAVIO <= TAM_TABULEIRO &&
        coluna_vertical < TAM_TABULEIRO) {
        // Posiciona o navio vertical
        for (int i = 0; i < TAM_NAVIO; i++) {
            // Verifica se há sobreposição com outro navio
            if (tabuleiro[linha_vertical + i][coluna_vertical] != 0) {
                printf("Erro: sobreposição de navios na posição (%d, %d).\n", linha_vertical + i, coluna_vertical);
                return 1; // encerra o programa
            }
            tabuleiro[linha_vertical + i][coluna_vertical] = navio_vertical[i];
        }
    } else {
        printf("Erro: navio vertical não cabe no tabuleiro.\n");
        return 1;
    }

    // Exibe o tabuleiro
    printf("\n=== Tabuleiro ===\n");
    for (int i = 0; i < TAM_TABULEIRO; i++) {
        for (int j = 0; j < TAM_TABULEIRO; j++) {
            printf("%d ", tabuleiro[i][j]);
        }
        printf("\n");
    }

    return 0;
}
