<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3767b36f-fca3-43c2-b239-8b2c9ee9e175" /># EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
#include <stdio.h>
#include <ctype.h>  
int main() {
    char text[100];
    int key, i;
    
    
    printf("Enter the plain text: ");
    fgets(text, sizeof(text), stdin);
    
    
    printf("Enter the key value: ");
    scanf("%d", &key);
    
   
    for (i = 0; text[i] != '\0'; i++) {
        char ch = text[i];
        
        if (isalpha(ch)) { 
            char base = (ch >= 'a' && ch <= 'z') ? 'a' : 'A';
            
            if (key >= 0)
                text[i] = (ch - base + key) % 26 + base;  
            else
                text[i] = (ch - base + (26 + key % 26)) % 26 + base;
        }
    }
    
    
    printf("Cipher Text: %s\n", text);
    
    return 0;
}


## OUTPUT:
<img width="1920" height="1024" alt="Screenshot (299)" src="https://github.com/user-attachments/assets/4cb5144a-d58a-448d-9162-3348ead3f9c6" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
