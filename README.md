#include <stdio.h>

void checkPrimeNum();

int main() {
    checkPrimeNum();
    return 0;
}

void checkPrimeNum() {
    int n, i, flag = 0;
    printf("Enter your num: ");
    scanf("%d", &n);

    // ০ এবং ১ প্রাইম নাম্বার নয়
    if (n == 0 || n == 1) {
        flag = 1; // flag ১ করে দিলাম যাতে নিচে 'not prime' দেখায়
    } else {
        // ২ থেকে শুরু করে n/2 পর্যন্ত ভাগ করে দেখা
        for (i = 2; i <= n / 2; ++i) {
            if (n % i == 0) {
                flag = 1; // ভাগ মিলে গেলে প্রাইম নয়
                break;
            }
        }
    }

    // আউটপুট প্রিন্ট করা
    if (flag == 1) {
        printf("%d is NOT a prime num\n", n);
    } else {
        printf("%d is a prime num\n", n);
    }
}
