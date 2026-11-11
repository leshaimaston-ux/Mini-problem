#include <studio.h>
void countdown(int n) {

    // Base Case

    if (n <= 0) {

        return;

    }

    // Phase 1: Countdown

    printf("%d ", n);

    // Recursive Call (moving toward base case)

    countdown(n - 1);

    // Phase 2: Count Up (executes as stack unwinds)

    printf("%d ", n);

}

int main() {

    int num;

    // Menu/Input logic (allowed in main)

    printf("Enter a number: ");

    if (scanf("%d", &num) != 1 || num < 1) {

        printf("Please enter a valid positive integer.\n");

        return 1;

    }

    // Executing the recursive function

    printf("Output: ");

    countdown(num);

    printf("\n");

    return 0;

    include <stdio.h>

/**

  sumDigits: Calculates the sum of digits using recursion.

  1. Base Case: If n < 10, the sum is just the number itself.

  2. Recursive Case: Add the last digit (n % 10) to the result
  of sumDigits(n / 10).

 */

int sumDigits(int n) {

    // Base Case

    if (n < 10) {

        return n;

    }

    // Recursive Case

    // n % 10 isolates the last digit

    // n / 10 removes the last digit

    return (n % 10) + sumDigits(n / 10);

}

int main() {

    // Test cases

    printf("5832 -> %d\n", sumDigits(5832)); // Expected: 18

    printf("1005 -> %d\n", sumDigits(1005)); // Expected: 6

    printf("7    -> %d\n", sumDigits(7));    // Expected: 7

    printf("0    -> %d\n", sumDigits(0));    // Expected: 0

    return 0;

}



}

