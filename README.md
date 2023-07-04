#include <stdio.h>
#include <stdlib.h>

int minimal_steps(int x, int y) {
    int steps = 0;

    while (y > x) {
        if (y % 2 == 0) {
            y /= 2;
        } else {
            y += 1;
        }
        steps++;
    }

    steps += x - y;

    return steps;
}

int main() {
    int x, y;
    printf("Введіть значення x: ");
    scanf("%d", &x);
    printf("Введіть значення y: ");
    scanf("%d", &y);

    int result = minimal_steps(x, y);
    printf("Мінімальна кількість кроків: %d\n", result);

    return 0;
}
