#사용자로부터 모래시계의 높이(홀수 N)를 입력받아, 입력한 크기에 맞는 모래시계 모양을 콘솔 화면에 출력하는 C언어 프로그램#

```c
#include <stdio.h>

int main() {
    int n;
    int i, j;

    scanf_s("%d", &n);

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
