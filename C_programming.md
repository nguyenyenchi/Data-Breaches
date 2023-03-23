
# Scan "Tom Hanks" as input and print out

char fstring1[20];
char fstring2[20];

scanf("%s%s", fstring1, fstring2);
printf("Hello %s %s",fstring1, fstring2)

# Solve HackerRank Functions

#include <stdio.h>

int max_of_two(int a, int b){
    if (a > b){
        return a;
    }
    else {
        return b;
    }
}
int max_of_four(int a, int b, int c, int d) {

    int first = max_of_two(a, b);
    int second =  max_of_two(first, c);
    int third = max_of_two(second, d);
    return third;
}

int main() {
    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    int ans = max_of_four(a, b, c, d);
    printf("%d", ans);

    return 0;
}

# Struct
struct Student{
    char name[50];
    char major[50];
    int age;
    double gpa;

};

int main() {

    struct Student student1;

    student1.age = 22;
    student1.gpa = 9.0;

    strcpy(student1.name, "Jim");
    printf("%s", student1.name);

}

# While loop
int main() {
  int index = 1;
  while (index<=5){
      printf("%d\n", index);
      index++;
}

# For loop
int main() {
  int index = 5;

  for(i=1; i<=5; i++){
      printf("%d\n", i);
  }
}

# 2D array & Nested Loop
int main() {
  int nums[3][2] = {
        {1,2},
        {3,4},
        {5,6}
    };

    printf("%d\n", nums[2][1]);

    int i, j;
    for(i=0; i<3; i++){
    for(j=0;j<2;j++){
        printf("%d,", nums[i][j]);
    }
    printf("\n");
    };
  return 0;
}

# Memory addresses
printf("%p", &index);
When C wants to access the information in the variable,
-> Go to that memory address of that variable, and you'll see the value of variable 'index'
-> Print out the address of a variable index stored in the memory (RAM) of a computer

# Pointers - a type of data - a memory address inside the RAM of computer
&index is a pointer, a data type and is a memory address of the variable 'index'
It's like:
int is an integer type of data in our program, and it happens to be a whole number
double is a type of data, and it's a decimal number

how to store a pointer inside a pointer variable?
int *pAge = &age;

# Deferencing pointers in C - Go to that address and get the value the pointer is pointing to
&index is a pointer
Dereference a pointer: *&index -> Get value of index

int *pIndex = &index;
printf("%d", *pIndex);

# Arrays & Strings HackerRank

#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    

    char str[1000];
    scanf("%s", str);

    int arrInt[10];

    int i, j;

    for(j=0; j<10;j++){
        arrInt[j] = 0;
    };


    char ch;
    /* Loop through the scanned string */
    for(i=0; i<strlen(str);i++){

        ch = str[i];
        if (ch >= '0' && ch <= '9'){

            /*If we subtract two characters, subtraction will happen between ASCII of                                 characters*/
            int num = ch - '0';
            arrInt[num]++;
        }
    };
    for(j=0; j<10;j++){
        printf("%d ", arrInt[j]);
    };


    return 0;
}
