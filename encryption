#include <cs50.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#include <math.h>
#include <stdlib.h>

int main(int argc, string argv[])
{
    //confirm number of arguments
    if (argc != 2)
    {
        printf("Usage: ./caesar key\n");
        return 1;
    }

    for (int i = 0; argv[1][i]; i++)
    {
        // check if any of the characters of the command-line argument is not a decimal digit, this includes the negative sign ;-)
        if (!isdigit((unsigned char) argv[1][i]))
        {
            printf("Usage: ./caesar key\n");
            return 1;
        }
    }

//convert string digit(s) to integer
    int key = atoi(argv[1]);

//prompt user for text.
    string p = get_string("Plaintext: ");
    printf("ciphertext: ");

    for (int i = 0, n = strlen(p); i < n; i++)
    {   
//if uppercased
        if (isupper(p[i]))
        {   
//convert ascii to alphabetical index. Remember each ascii char has corresponding number.
            //eg. char letter = 'a' is actually int 97
            //printf("%i", 97 - letter) = 0
            printf("%c", (((p[i] + key) - 65) % 26) + 65);
        }
        // if lowercased
        else if (islower(p[i]))
        {
            printf("%c", (((p[i] + key) - 97) % 26) + 97);
        }
        //if not upper nor lower, just print copy of char
        else
        {
            printf("%c", p[i]);
        }
    }
    printf("\n");
    return 0;
}


