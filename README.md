# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char text[100];
    int shift, i;

    printf("Enter text: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter shift: ");
    scanf("%d", &shift);

    // Encryption
    for (i = 0; text[i] != '\0'; i++)
    {
        if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = (text[i] - 'a' + shift) % 26 + 'a';

        else if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = (text[i] - 'A' + shift) % 26 + 'A';
    }

    printf("Encrypted text: %s", text);

    return 0;
}
```

## OUTPUT:
<img width="784" height="290" alt="image" src="https://github.com/user-attachments/assets/ab524c7f-ad14-44b2-9799-8f8f4913afbd" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
