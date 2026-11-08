# Shivam-4
Diwali
#include <stdio.h>

int main(void) {
    int n = 5;
    int i, j;
    char greeting[] = "HAPPY DIWALI";

    /* --- Part 1: Top Pyramid (Upper Lantern Body) --- */
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= n - i; j++) {
            putchar(' ');
            putchar(' ');
        }
        for (j = 1; j <= 2 * i - 1; j++) {
            putchar('*');
            putchar(' ');
        }
        putchar('\n');
    }

    /* --- Part 2: Inverted Pyramid (Lower Lantern Body) --- */
    for (i = n - 1; i >= 1; i--) {
        for (j = 1; j <= n - i; j++) {
            putchar(' ');
            putchar(' ');
        }
        for (j = 1; j <= 2 * i - 1; j++) {
            putchar('*');
            putchar(' ');
        }
        putchar('\n');
    }

    /* --- Part 3: Hanging Streamers / Tassels --- */
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= (2 * n - 1); j++) {
            if (j % 2 != 0) {
                putchar('*');
            } else {
                putchar(' ');
            }
            putchar(' ');
        }
        putchar('\n');
    }

    /* --- Part 4: Print HAPPY DIWALI using a loop --- */
    putchar('\n');
    for (i = 0; greeting[i] != '\0'; i++) {
        putchar(greeting[i]);
    }
    putchar('\n');

    return 0;
}
