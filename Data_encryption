#include <stdio.h>
#include <string.h>
#include <stdlib.h>
void encrypt(char *message, int key) {
    int i, len = strlen(message);
    char ch;
    for (i = 0; i < len; i++) {
        ch = message[i];
        if (ch >= 'a' && ch <= 'z') {
            ch = ch + key;
            if (ch > 'z') {
                ch = ch - 'z' + 'a' - 1;
            }
            message[i] = ch;
        } else if (ch >= 'A' && ch <= 'Z') {
            ch = ch + key;
            if (ch > 'Z') {
                ch = ch - 'Z' + 'A' - 1;
            }
            message[i] = ch;
        }
    }
}

void decrypt(char *message, int key) {
    int i, len = strlen(message);
    char ch;
    for (i = 0; i < len; i++) {
        ch = message[i];
        if (ch >= 'a' && ch <= 'z') {
            ch = ch - key;
            if (ch < 'a') {
                ch = ch + 'z' - 'a' + 1;
            }
            message[i] = ch;
        } else if (ch >= 'A' && ch <= 'Z') {
            ch = ch - key;
            if (ch < 'A') {
                ch = ch + 'Z' - 'A' + 1;
            }
            message[i] = ch;
        }
    }
}

int main() {
	system("color 02");
    char message[100];
    int key;
    printf("Enter the message: ");
    scanf("%[^\n]s", message);
    printf("Enter the key: ");
    scanf("%d", &key);
    encrypt(message, key);
    printf("Encrypted message: %s\n", message);
    decrypt(message, key);
    printf("Decrypted message: %s\n", message);
    return 0;
}
