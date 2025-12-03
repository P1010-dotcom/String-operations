#include <stdio.h>
int main() {
    char str1[100], str2[100], copy[100];
    int i, j, length = 0, flag = 0;

 printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);

printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);

 for (i = 0; str1[i] != '\0'; i++) {
        if (str1[i] == '\n')
            str1[i] = '\0';
    }
    for (i = 0; str2[i] != '\0'; i++) {
        if (str2[i] == '\n')
            str2[i] = '\0';
    }
    for (i = 0; str1[i] != '\0'; i++) {
        copy[i] = str1[i];
    }
    copy[i] = '\0';

 printf("\nCopied string: %s", copy);
    for (i = 0; str1[i] != '\0'; i++);
    length = i;
    printf("\nLength of first string: %d", length);
    flag = 0;
    for (i = 0; str1[i] != '\0' || str2[i] != '\0'; i++) {
        if (str1[i] != str2[i]) {
            flag = 1;
            break;
        }
    }

 if (flag == 0)
        printf("\nStrings are equal.");
    else
        printf("\nStrings are not equal.");
    for (i = 0; str1[i] != '\0'; i++);
    for (j = 0; str2[j] != '\0'; j++) {
        str1[i + j] = str2[j];
    }
    str1[i + j] = '\0';

 printf("\nAfter concatenation: %s\n", str1);

 return 0;
}
