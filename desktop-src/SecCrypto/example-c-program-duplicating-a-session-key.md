---
description: Im folgenden Beispiel wird ein zufälliger Sitzungsschlüssel erstellt, der Schlüssel dupliziert, einige zusätzliche Parameter für den ursprünglichen Schlüssel festgelegt und sowohl der ursprüngliche als auch der doppelte Schlüssel zerstört.
ms.assetid: e57274cf-42d3-445b-97f1-dd574010290f
title: 'Beispiel-C-Programm: Duplizieren eines Sitzungsschlüssels'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38934d399a6a38f14e551e79d4e1f877dbadf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959630"
---
# <a name="example-c-program-duplicating-a-session-key"></a>Beispiel-C-Programm: Duplizieren eines Sitzungsschlüssels

Im folgenden Beispiel wird ein zufälliger [*Sitzungsschlüssel*](../secgloss/s-gly.md)erstellt, der Schlüssel dupliziert, einige zusätzliche Parameter für den ursprünglichen Schlüssel festgelegt und sowohl der ursprüngliche als auch der doppelte Schlüssel zerstört. Dieses Beispiel veranschaulicht die Verwendung von [**cryptduplicatekey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) und zugehöriger Funktionen.

In diesem Beispiel werden die folgenden Aufgaben und kryptoapi-Funktionen veranschaulicht:

-   Zugreifen auf einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) mithilfe von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
-   Erstellen eines Sitzungsschlüssels mithilfe von [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).
-   Duplizieren des mit [**cryptduplicatekey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey)erstellten Schlüssels.
-   Verwenden von [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , um den Schlüssel Generierungsprozess auf zwei verschiedene Arten zu ändern.
-   Auffüllen eines Puffers mit zufälligen Bytes mithilfe von " [**cryptgenrandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom)".
-   Zerstören der Schlüssel mithilfe von [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).
-   Freigeben des CSP mit [**cryptreleasecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).

In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet. Der Code für diese Funktion ist im Beispiel enthalten. Der Code für dieses und andere Hilfsfunktionen ist auch unter [universell Funktionen](general-purpose-functions.md)aufgeführt.


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Begin main.

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV   hCryptProv;
HCRYPTKEY    hOriginalKey;
HCRYPTKEY    hDuplicateKey;
DWORD        dwMode;
BYTE         pbData[16];

//-------------------------------------------------------------------
// Begin processing.

printf("This program creates a session key and duplicates \n");
printf("that key. Next, parameters are added to the original \n");
printf("key. Finally, both keys are destroyed. \n\n");

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(    
   &hCryptProv,
   NULL,
   NULL,
   PROV_RSA_FULL,
   0)) 
{    
    printf("CryptAcquireContext succeeded. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext!\n");
}
//-------------------------------------------------------------------
// Generate a key.
if (CryptGenKey(
     hCryptProv, 
     CALG_RC4, 
     0, 
     &hOriginalKey))
{
   printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR - CryptGenKey.");
}
//-------------------------------------------------------------------
// Duplicate the key.

if (CryptDuplicateKey(
     hOriginalKey, 
     NULL, 
     0, 
     &hDuplicateKey))
{
   printf("The session key has been duplicated. \n");
}
else
{
   MyHandleError("ERROR - CryptDuplicateKey");
}
//-------------------------------------------------------------------
// Set additional parameters on the original key.
// First, set the cipher mode.

dwMode = CRYPT_MODE_ECB;
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_MODE, 
   (BYTE*)&dwMode, 
   0)) 
{
     printf("Key Parameters set. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
// Generate a random initialization vector.
if(CryptGenRandom(
   hCryptProv, 
   8, 
   pbData)) 
{
     printf("Random sequence generated. \n");
}
else
{
     MyHandleError("Error during CryptGenRandom.");
}
//-------------------------------------------------------------------
// Set the initialization vector.
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_IV, 
   pbData, 
   0)) 
{
     printf("Parameter set with random sequence as "
         "initialization vector. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
//-------------------------------------------------------------------
// Clean up.

if (hOriginalKey)
    if (!CryptDestroyKey(hOriginalKey))
        MyHandleError("Failed CryptDestroyKey\n");

if (hDuplicateKey)
    if (!CryptDestroyKey(hDuplicateKey))
            MyHandleError("Failed CryptDestroyKey\n");

if(hCryptProv)
    if (!CryptReleaseContext(hCryptProv, 0))
        MyHandleError("Failed CryptReleaseContext\n");

printf("\nThe program ran to completion without error. \n");

} // End of main.

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 
