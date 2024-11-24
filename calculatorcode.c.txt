#include <stdio.h>

float add(float x, float y) {
    return x + y;
}

float subtract(float x, float y) {
    return x - y;
}

float multiply(float x, float y) {
    return x * y;
}

float divide(float x, float y) {
    if (y == 0) {
        printf("Cannot divide by zero.\n");
        return 0;
    }
    return x / y;
}

int main() {
    int choice;
    float num1, num2;

    printf("Select operation:\n");
    printf("1. Add\n");
    printf("2. Subtract\n");
    printf("3. Multiply\n");
    printf("4. Divide\n");
    printf("Enter choice (1/2/3/4): ");
    scanf("%d", &choice);

    printf("Enter first number: ");
    scanf("%f", &num1);
    printf("Enter second number: ");
    scanf("%f", &num2);

    switch (choice) {
        case 1:
            printf("Result: %.2f\n", add(num1, num2));
            break;
        case 2:
            printf("Result: %.2f\n", subtract(num1, num2));
            break;
        case 3:
            printf("Result: %.2f\n", multiply(num1, num2));
            break;
        case 4:
            printf("Result: %.2f\n", divide(num1, num2));
            break;
        default:
            printf("Invalid input\n");
    }

    return 0;
}
