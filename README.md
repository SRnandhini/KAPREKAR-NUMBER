#include<stdio.h>
#include<math.h>  

int main() {
    int n, sum = 0, digit = 0, a;
    printf("Enter the number: ");
    scanf("%d", &n);
  
    int sq = n * n;
    a=n;
    while (a != 0) {
        a/=10;
        digit++;
    }
    int divisor = pow(10,digit )  ;
    int leftPart = sq / divisor;
    int rightPart = sq % divisor;
    if (leftPart + rightPart == n) {
        printf("%d is a Kaprekar number.\n", n);
    } else {
        printf("%d is not a Kaprekar number.\n", n);
    }
    
    return 0;
}

