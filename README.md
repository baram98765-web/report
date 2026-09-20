```c
#include <stdio.h>

int main() {
    int n;
    int i, j;

    scanf_s("%d", &n);

    // [선택 사항] 3 미만이거나 짝수인 경우를 방지하는 예외 처리 구문
    if (n < 3 || n % 2 == 0) {
        return 0;
    }

    for (i = 0; i <= n / 2; i++) {
        for (j = 0; j < i; j++) {
            printf(" ");
        }

        for (j = 0; j < n - 2 * i; j++) {
            printf("*");
        }

        printf("\n");
    }

    for (i = n / 2 - 1; i >= 0; i--) {
        for (j = 0; j < i; j++) {
            printf(" ");
        }

        for (j = 0; j < n - 2 * i; j++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}
```
