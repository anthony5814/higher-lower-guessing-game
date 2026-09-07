#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int checker(int guess, int secretNumber);
int user_input(int max, int min);
int main (void)
{
    srand(time(NULL));
    int n = 100;
    int secret_number = (rand() % n) + 1;
    int num;
    int result = 0;
    do{
    num = user_input(n, 1);
        result = checker(num, secret_number);
    }
    while (result != 1);
    return 0;
}
int checker(int guess, int secretNumber)
{
    if (guess > secretNumber){
        printf("Wrong, number is too high\n");
        return 0;
    }
    else if (guess < secretNumber){
        printf("Wrong, number is too low\n");
        return 0;
    }
    else{
        printf("Correct.\n");
        return 1;
    }
}

int user_input(int max, int min)
{
    int guess;
    int status;
    do {
        printf("Number (%d - %d): ", min, max);
        status = scanf("%d", &guess);
        
        if (status != 1) {
            while (getchar() != '\n'); 
            guess = min - 1; 
        }
        
        if (guess < min || guess > max)
            printf("Invalid\n");
    }
    while (guess < min || guess > max);

        return guess;
}
