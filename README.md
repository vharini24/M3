# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM

```c
#include <stdio.h>
#include <math.h>   


void calculateEMI(float principal, float rate, int time);

int main()
{
    float principal, rate;
    int time;

    printf("Enter principal amount: ");
    scanf("%f", &principal);

    printf("Enter annual rate of interest (in %%): ");
    scanf("%f", &rate);

    printf("Enter time period in months: ");
    scanf("%d", &time);


    calculateEMI(principal, rate, time);

    return 0;
}
I
void calculateEMI(float principal, float rate, int time)
{
    float monthlyRate, emi;

    monthlyRate = rate / (12 * 100);


    emi = (principal * monthlyRate * pow(1 + monthlyRate, time)) /
          (pow(1 + monthlyRate, time) - 1);

    
    printf("Principal Amount : %.2f\n", principal);
    printf("Rate of Interest : %.2f%%\n", rate);
    printf("Time Period      : %d months\n", time);
    printf("Monthly EMI      : %.2f\n", emi);

}
```




## OUTPUT

<img width="437" height="298" alt="image" src="https://github.com/user-attachments/assets/f96a19b5-3a2e-49e4-a36a-ac64715f7ead" />




## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

int main() {
    int n = 6;
    int a = 0, b = 1, c;

    printf("Fibonacci Series for %d terms:\n", n);

    for (int i = 1; i <= n; i++) {
        if (i == 1) {
            printf("%d ", a);
            continue;
        }
        if (i == 2) {
            printf("%d ", b);
            continue;
        }
        c = a + b;

        printf("%d ", c);

        a = b;
        b = c;
    }

    printf("\n");
    return 0;
}
```









## OUTPUT

<img width="371" height="163" alt="image" src="https://github.com/user-attachments/assets/eb26b45d-54ed-49ff-a69b-e135cb497ca6" />







## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM

```c

#include <stdio.h>

int main() {
    int n;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n]; 

    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("The last element is: %d\n", arr[n - 1]);

    return 0;
}
```




## OUTPUT









## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM

```c

#include <stdio.h>

int main() {
    int n, count = 0;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    for (int i = 0; i < n; i++) {
        if (arr[i] > 0) {
            count++;
        }
    }

    printf("Total number of positive elements: %d\n", count);

    return 0;
}
```


## OUTPUT





## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
```c

#include <stdio.h>

int main() {
    int n;

   
    printf("Enter the size of the array: ");
    scanf("%d", &n);

    int arr[n]; 
    printf("Enter %d elements:\n", n);

    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {
            arr[i] = 'E';
        }
    }

    printf("Updated array:\n");
    for (int i = 0; i < n; i++) {
        if (arr[i] == 'E') {
            printf("%c ", arr[i]);
        } else {
            printf("%d ", arr[i]);
        }
    }

    printf("\n");
    return 0;
}
```






## Output:
 


## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



