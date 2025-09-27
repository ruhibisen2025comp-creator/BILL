#include <stdio.h>
int main() {
    int customerID, units;
    char customerName[50];
    float bill;
    printf("Enter Customer ID: ");
    scanf("%d", &customerID);
   printf("Enter Customer Name: ");
    scanf("%s", customerName);

    printf("Enter Units Consumed: ");
    scanf("%d", &units);
    if (units <= 100) {
        bill = units * 1.50;
    }
    else if (units <= 300) {
        bill = (100 * 1.50) + (units - 100) * 2.50;
    }
    else {
        bill = (100 * 1.50) + (200 * 2.50) + (units - 300) * 4.00;
    }
    printf("\n----- Electricity Bill -----\n");
    printf("Customer ID   : %d\n", customerID);
    printf("Customer Name : %s\n", customerName);
    printf("Units Consumed: %d\n", units);
    printf("Total Bill    : Rs. %.2f\n", bill);
    printf("----------------------------\n");
 return 0;
}
