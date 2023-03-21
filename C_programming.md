
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
