/* P1 
\*
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
 /* P2
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

 /*P3
 \*
# include <stdio.h>

# include <string.h>

int isPalindrome(const char str[], int start, int end) {

    if (start >= end) {

        return 1;

    }



    if (str[start] != str[end]) {

        return 0;

    }

    return isPalindrome(str, start + 1, end - 1);

}

/* P4
\*

int countChar(const char str[], char target) {

    // Base case: end of string

    if (str[0] == '\0') {

        return 0;

    }

    // Recursive case: check current and move to the next character

    int found = (str[0] == target) ? 1 : 0;

    return found + countChar(str + 1, target);

}

/*P5
\*

int recursiveMax(const int arr[], int size) {

    // Base case: only one element

    if (size == 1) {

        return arr[0];

    }



    // Recursive case: compare current with the max of the rest

    int maxOfRest = recursiveMax(arr + 1, size - 1);

    return (arr[0] > maxOfRest) ? arr[0] : maxOfRest;

}

/*P6
\*
int recursiveMax(const int arr[], int size) {

    // Base case: only one element

    if (size == 1) {

        return arr[0];

    }



    // Recursive case: compare current with the max of the rest

    int maxOfRest = recursiveMax(arr + 1, size - 1);

    return (arr[0] > maxOfRest) ? arr[0] : maxOfRest;

}

/*P7
\*

int binarySearch(const int arr[], int left, int right, int target) {

    if (left > right) {

        return -1;

    }

    int mid = left + (right - left) / 2;

    if (arr[mid] == target) {

        return mid;

    }

    if (arr[mid] > target) {

        return binarySearch(arr, left, mid - 1, target);

    } else {

        return binarySearch(arr, mid + 1, right, target);

    }

}

/*P8
\*

int countNodes(const Node *head) {

    // Base case: empty list

    if (head == NULL) return 0;

    // Recursive case: 1 + count of rest of list

    return 1 + countNodes(head->next);

}

/* Task B
\*

int sumNodes(const Node *head) {

    // Base case: empty list

    if (head == NULL) return 0;

    // Recursive case: current data + sum of rest

    return head->data + sumNodes(head->next);

}

/* Task C
\*
void printReverse(const Node *head) {

    // Base case: empty list

    if (head == NULL) return;

    // Recursive step: call on next first to reach end

    printReverse(head->next);

    // Print after the recursive call returns (backtracking)

    printf("%d ", head->data);

}

/*P9
\*

# include <stdio.h>

# include <string.h>

int isPalindrome(const char str[], int start, int end) {

    if (start >= end) {

        return 1;

    }

    if (str[start] != str[end]) {

        return 0;

    }

    return isPalindrome(str, start + 1, end - 1);

}
\*

