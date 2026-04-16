
#include <stdio.h>

int main() {
    int n, i, j;
    int check;
    long long sum = 0;

    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        check = 1;

        if (i < 2) {
            check = 0;
        } else {
            for (j = 2; j < i; j++) {
                if (i % j == 0) {
                    check = 0;
                    break;
                }
            }
        }

        if (check == 1)
            sum = sum + i;
        else
            sum = sum - i;
    }

    printf("%lld", sum);

    return 0;
}
