# Estudos-C

#exercicies about C 

##A program that asks for a person's name, address, telephone number and age and creates a string 
```c
34)
#include <stdio.h>

int main() {

   int age,number;
  char name[50],address[150];
  printf("what your name \n");
  scanf("%s", &name );
  printf("what your address \n");
  scanf("%s", &address);
  printf("what your age \n");
  scanf("%d", &age);
  printf("what your number \n");
  scanf("%d", &number);
  printf("your name is %s, you have %d years old, lives on the street %s, you number is %d", name,age,address,number);
  return 0;
}
```

## Create a program that asks for a value in degrees Fahrenheit and prints
the corresponding value in degrees Celsius on the video using the formulas

```
25)
#include <stdio.h>

int main() {
  float fahrenheit, celsius;
  printf("What value in degrees Fahrenheit do you want to convert to degrees Celsius?\n");
  scanf("%f", &fahrenheit);
  celsius = (fahrenheit - 32) * 5 / 9;
  printf("The value in degrees Celsius is: %.2f\n", celsius);
  return 0;
}
```
##Make a program that reads the price of a product and inflates that price by 10% if it is less than 100 and by 20% if it is greater than or equal to 100.

```
27)
#include <stdio.h>

int main() {
  float price = 0.0, inflation = 0.0;
printf("what is the price of the product?\n");
  scanf("%f", &price);
  if (price<100){
    inflation = ((price * 0.1) + price);
  printf("The inflated price of the product is: %.2f\n", inflation);
    }
  if(price>=100){
    inflation = ((price * 0.2) + price);
    printf("The inflated price of the product is: %.2f\n", inflation);
     
  }
}
```

##a program that requests the total amount spent by a customer in a store, prints the payment options, requests the desired option and prints the total amount of the installments

```
int main(void) {
  float price;
  int option, installment;

  printf("Enter the total purchase price: \n\n");
  scanf("%f", &price);

  printf("Choose a payment option:\n 1:The view with 10%% discount \n "
         "2: Pay in two installments at sticker price\n 3: Installment of three "
         "ten months with 3%% interest\n");
  scanf("%d", &option);

  if (option == 1) {
    printf("the final price is %.2f\n", price * 0.9);
  } else if (option == 2) {
    printf("the final price is: %.2f\n", price);
  } else if (option == 3) {
    if (price >= 100) {
      printf("How many installments do you want to pay in?\n");
      scanf("%d", &installment);
      if (installment < 3 || installment > 10) {
        printf("Invalid option\n");
      } else {
        price = ((price/installment) * 1.03) * installment;
        printf("the final price is: %.2f\n", price);
        printf("Each installment will be: %.2f\n", price / installment);
      }
    } else {
      printf("Invalid option\n");
    }
  }

  return 0;
}
```
