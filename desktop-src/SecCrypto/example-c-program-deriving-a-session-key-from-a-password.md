---
description: Im folgenden Beispiel wird das Erstellen eines kryptografischen Sitzungsschlüssels aus dem Hash eines Kennworts sowie die Verwendung der CryptDeriveKey-Funktion und verwandter Funktionen veranschaulicht.
ms.assetid: f4748725-2a47-487c-b18c-7b27112d1090
title: 'C-Beispielprogramm: Ableiten eines Sitzungsschlüssels aus einem Kennwort'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33b43e69b9db2f77e04bad2f8941e6fc0c1bf4e30e5f1d0ff7a5e3bac5ce06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007838"
---
# <a name="example-c-program-deriving-a-session-key-from-a-password"></a>C-Beispielprogramm: Ableiten eines Sitzungsschlüssels aus einem Kennwort

Im folgenden Beispiel wird das Erstellen eines [*kryptografischen Sitzungsschlüssels*](../secgloss/s-gly.md) aus dem [*Hash*](../secgloss/h-gly.md) eines Kennworts sowie die Verwendung der [**CryptDeriveKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) und verwandter Funktionen veranschaulicht.

In diesem Beispiel werden die folgenden Aufgaben und CryptoAPI-Funktionen veranschaulicht:

-   Aufrufen von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines Handles für den Standard-CSP und den [*Standardschlüsselcontainer*](../secgloss/k-gly.md).
-   Verwenden von [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) zum Erstellen eines leeren Hashobjekts.
-   Hashing des Kennworttexts mithilfe von [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).
-   Ableiten eines Sitzungsschlüssels aus dem Hashkennwort mithilfe von [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).
-   Zerstören des Hashs und des Kennworts.
-   Verwenden von [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) zum Freigeben des CSP.

In diesem Beispiel wird die Funktion [**MyHandleError verwendet.**](myhandleerror.md) Code für diese Funktion ist im Beispiel enthalten.

Code für diese und andere Hilfsfunktionen ist auch unter [Universell Functions](general-purpose-functions.md)aufgeführt.


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <string.h>
#include <conio.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);
void GetConsoleInput(char*, UINT);
#define PASSWORD_LENGTH 512

void main()
{
    //----------------------------------------------------------------
    // Copyright (C) Microsoft.  All rights reserved.
    // Declare and initialize variables.

    HCRYPTPROV hCryptProv;
    HCRYPTKEY hKey;
    HCRYPTHASH hHash;
    CHAR szPassword[PASSWORD_LENGTH] = "";
    DWORD dwLength;

    //----------------------------------------------------------------
    // Get the password from the user.

    fprintf(stderr,"Enter a password to be used to create a key:");

    // Get a password while printing only asterisks to the screen.
    GetConsoleInput(szPassword, PASSWORD_LENGTH);
    printf("The password has been stored.\n");
    dwLength = (DWORD) strlen(szPassword);

    //----------------------------------------------------------------
    // Acquire a cryptographic provider context handle.

    if(CryptAcquireContext(
       &hCryptProv,
       NULL,
       NULL,
       PROV_RSA_FULL,
       0))
    {
        printf("A context has been acquired. \n");
    }
    else
    {
         MyHandleError("Error during CryptAcquireContext!");
    }
    //----------------------------------------------------------------
    // Create an empty hash object.

    if(CryptCreateHash(
       hCryptProv,
       CALG_MD5,
       0,
       0,
       &hHash))
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptCreateHash!");
    }
    //----------------------------------------------------------------
    // Hash the password string.

    if(CryptHashData(
       hHash,
       (BYTE *)szPassword,
       dwLength,
       0))
    {
         printf("The password has been hashed. \n");
    }
    else
    {
         MyHandleError("Error during CryptHashData!");
    }
    //----------------------------------------------------------------
    // Create a session key based on the hash of the password.

    if(CryptDeriveKey(
       hCryptProv,
       CALG_RC2,
       hHash,
       CRYPT_EXPORTABLE,
       &hKey))
    {
        printf("The key has been derived. \n");
    }
    else
    {
        MyHandleError("Error during CryptDeriveKey!");
    }
    //----------------------------------------------------------------
    // Use hKey as appropriate to encrypt or decrypt a message.

    //----------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
       if(!(CryptDestroyHash(hHash)))
           MyHandleError("Error during CryptDestroyHash");
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
            MyHandleError("Error during CryptDestroyKey");
    }

    // Release the provider handle.
    if(hCryptProv)
    {
       if(!(CryptReleaseContext(hCryptProv, 0)))
           MyHandleError("Error during CryptReleaseContext");
    }
    printf("The program to derive a key completed without error. \n");
} // end main

//--------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit
// the program.
// For most applications, replace this function with one
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}

//--------------------------------------------------------------------
// The GetConsoleInput function gets an array of characters from the
// keyboard, while printing only asterisks to the screen.

void GetConsoleInput(char* strInput,
                    UINT  intMaxChars)
{
    char ch;
    char minChar = ' ';
    minChar++;

    ch = (char)_getch();
    while (ch != '\r')
    {
        if (ch == '\b' && strlen(strInput) > 0)
        {
            strInput[strlen(strInput)-1]   = '\0';
            printf("\b \b");
        }
        else if ((ch >= minChar) && (strlen(strInput) < intMaxChars))
        {
            strInput[strlen(strInput)+1] = '\0';
            strInput[strlen(strInput)]   = ch;
            _putch('*');
        }
        ch = (char)_getch();
    }
    _putch('\n');
}

```



 

 
